<script setup lang="ts">
import { computed, ref } from 'vue'
import AnnotatedText from './AnnotatedText.vue'

type SpeechLang = 'ja-JP' | 'en-US'
const props = withDefaults(defineProps<{
  text?: string // 表示テキスト
  read?: string // 読み上げ専用テキスト（未指定時は text を読む）
  lang?: SpeechLang // 読み上げ言語
  speaker?: boolean // スピーカーアイコン表示
  rate?: number // 読み上げ速度（未指定時は言語別デフォルト）
}>(), {
  text: '',
  read: '',
  lang: 'ja-JP',
  speaker: true,
  rate: undefined
})

const resolvedRead = ref('')
const updateResolvedRead = (value: string) => {
  resolvedRead.value = value
}

const readText = computed(() => (props.read || resolvedRead.value || '').trim())
const speechRate = computed(() => {
  if (typeof props.rate === 'number') return props.rate
  return props.lang === 'ja-JP' ? 0.82 : 0.85
})

const getVoicesReady = async () => {
  if (typeof window === 'undefined' || !('speechSynthesis' in window) || !('SpeechSynthesisUtterance' in window)) {
    return [] as SpeechSynthesisVoice[]
  }

  const initialVoices = window.speechSynthesis.getVoices()
  if (initialVoices.length > 0) return initialVoices

  // 初回は音声一覧が空のことがあるため、イベント到着を短時間待つ
  const loadedVoices = await new Promise<SpeechSynthesisVoice[]>((resolve) => {
    const timer = window.setTimeout(() => {
      resolve(window.speechSynthesis.getVoices())
    }, 500)

    const onVoicesChanged = () => {
      window.clearTimeout(timer)
      resolve(window.speechSynthesis.getVoices())
    }

    window.speechSynthesis.addEventListener('voiceschanged', onVoicesChanged, { once: true })
  })

  return loadedVoices
}

const pickPreferredVoice = (voices: SpeechSynthesisVoice[], lang: SpeechLang) => {
  if (lang === 'ja-JP') {
    const japaneseVoices = voices.filter((voice) => voice.lang.toLowerCase().startsWith('ja'))
    const preferredFemaleNames = ['aya', 'sayaka', 'haruka', 'akari', 'nanami']
    for (const name of preferredFemaleNames) {
      const match = japaneseVoices.find((voice) => voice.name.toLowerCase().includes(name))
      if (match) return match
    }
    return japaneseVoices[0]
  }

  const englishVoices = voices.filter((voice) => voice.lang.toLowerCase().startsWith('en'))
  const preferredFemaleNames = ['jenny', 'aria', 'zira', 'ava', 'emma', 'samantha']
  for (const name of preferredFemaleNames) {
    const match = englishVoices.find((voice) => voice.name.toLowerCase().includes(name))
    if (match) return match
  }
  return englishVoices[0]
}

const speak = async () => {
  const text = readText.value
  const lang = props.lang
  if (typeof window === 'undefined' || !text) return
  if (!('speechSynthesis' in window) || !('SpeechSynthesisUtterance' in window)) return

  window.speechSynthesis.cancel()

  const utterance = new SpeechSynthesisUtterance(text)
  utterance.lang = lang
  utterance.rate = speechRate.value

  const voices = await getVoicesReady()
  const targetVoice = pickPreferredVoice(voices, lang)

  if (targetVoice) {
    utterance.voice = targetVoice
  }

  window.speechSynthesis.speak(utterance)
}

const speakerLabel = computed(() => props.lang === 'ja-JP' ? '読み上げる' : 'Read aloud')
</script>

<template>
  <div class="speech-line">
    <AnnotatedText
      class="speech-line-text"
      :text="text"
      @resolved-read="updateResolvedRead"
    />
    <button
      v-if="speaker && readText"
      type="button"
      class="speech-line-button"
      :aria-label="speakerLabel"
      @click="speak"
    >
      🔉
    </button>
  </div>
</template>

<style scoped>
.speech-line {
  margin: 0.6rem 0;
  display: flex;
  align-items: flex-start;
  gap: 10px;
}

.speech-line-text {
  font-size: 1.8rem;
}

.speech-line-button {
  background: none;
  border: none;
  padding: 0;
  cursor: pointer;
  font-size: 1.2rem;
  line-height: 1;
  margin-top: 0.95em;
}

.speech-line-button:hover {
  opacity: 0.7;
}
</style>