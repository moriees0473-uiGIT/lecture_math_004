<script setup lang="ts">
import { computed, watch } from 'vue'

type ParseMode = 'display' | 'read'

const props = withDefaults(defineProps<{
	text?: string
}>(), {
	text: ''
})

const emit = defineEmits<{
	(event: 'resolved-read', value: string): void
}>()

const escapeHtml = (text: string) => text
	.replace(/&/g, '&amp;')
	.replace(/</g, '&lt;')
	.replace(/>/g, '&gt;')
	.replace(/"/g, '&quot;')
	.replace(/'/g, '&#39;')

const readTag = 'read{'

const findMatchingBrace = (source: string, startIndex: number) => {
	let depth = 0
	for (let index = startIndex; index < source.length; index++) {
		const char = source[index]
		if (char === '{') depth += 1
		if (char === '}') {
			depth -= 1
			if (depth === 0) return index
		}
	}
	return -1
}

const splitTopLevel = (source: string, delimiter = '|') => {
	let depth = 0
	for (let index = 0; index < source.length; index++) {
		const char = source[index]
		if (char === '{') depth += 1
		else if (char === '}') depth -= 1
		else if (char === delimiter && depth === 0)
			return [source.slice(0, index), source.slice(index + 1)] as const
	}
	return [source, ''] as const
}

const parseInlineText = (source: string, mode: ParseMode): string => {
	let output = ''

	for (let index = 0; index < source.length; index++) {
		if (source.startsWith(readTag, index)) {
			const contentStart = index + readTag.length
			const contentEnd = findMatchingBrace(source, contentStart - 1)
			if (contentEnd !== -1) {
				const content = source.slice(contentStart, contentEnd)
				const [displayPart, readPart] = splitTopLevel(content)
				output += parseInlineText(mode === 'display' ? displayPart : readPart || displayPart, mode)
				index = contentEnd
				continue
			}
		}

		output += escapeHtml(source[index])
	}

	return output
}

const parsedText = computed(() => {
	const source = props.text || ''
	return {
		display: parseInlineText(source, 'display').trim(),
		read: parseInlineText(source, 'read').trim(),
	}
})

const displayHtml = computed(() => parsedText.value.display)

watch(
	() => parsedText.value.read,
	(value) => emit('resolved-read', value),
	{ immediate: true }
)
</script>

<template>
	<p class="annotated-text" v-html="displayHtml"></p>
</template>

<style scoped>
.annotated-text {
	margin: 0;
	font: inherit;
	color: inherit;
	line-height: inherit;
	white-space: pre-line;
}
</style>
