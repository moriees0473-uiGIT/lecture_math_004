---
theme: seriph
# background: https://images.pexels.com/photos/6238050/pexels-photo-6238050.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=1080&w=1920
background: bg.png
class: text-center
# colorSchema options:
# colorSchema: light
colorSchema: dark
highlighter: shiki
lineNumbers: true
drawings:
  persist: false
transition: slide-left
title: 二次方程式の解法
---
# 第４回 二次方程式③

平方完成・解の公式

2026/5/13

---
layout: default
---

# 本日のテーマ

<div class="ml-4 text-3xl space-y-4">
  <div>1. 平方完成：completing the square</div>

$$
x^2 + \color{ff6b6b}b\color{ffffff}x　　 \rightarrow　　 \left( x + \frac{\color{ff6b6b}b}{2} \right)^2 - \left( \frac{\color{ff6b6b}b}{2} \right)^2
$$

  <div>2. 解の公式：quadratic formula</div>

$$
x^2 + (\color{ff6b6b}p\color{ffffff}+\color{6bb6ff}q\color{ffffff})x + \color{ff6b6b}p\color{6bb6ff}q \color{ffffff}= 0　　\rightarrow　　(x+\color{ff6b6b}p\color{ffffff})(x+\color{6bb6ff}q\color{ffffff}) = 0
$$

$$
x^2 + 2\color{ff6b6b}b\color{ffffff}x + \color{ff6b6b}b\color{ffffff}^2 = 0　　\rightarrow　　(x+\color{ff6b6b}b\color{ffffff})^2 = 0
$$

$$
x^2 - 2\color{ff6b6b}b\color{ffffff}x +\color{ff6b6b} b\color{ffffff}^2 = 0　　\rightarrow　　(x-\color{ff6b6b}b\color{ffffff})^2 = 0
$$


</div>

---
layout: default
---

# <ruby>平方完成<rt>へいほう かんせい</rt></ruby>の考え方 <SpeechLine text="completing the square" lang="en-US" />

二次方程式を<ruby>解<rt>と</rt></ruby>いたり、<ruby>関数<rt>かんすう</rt></ruby>のグラフを考えたりする<ruby>際<rt>さい</rt></ruby>に、<ruby>非常<rt>ひじょう</rt></ruby>に<ruby>重要<rt>じゅうよう</rt></ruby>なステップです。
<br>

$$
x^2 + bx \rightarrow \left( x + \frac{b}{2} \right)^2 - \left( \frac{b}{2} \right)^2
$$

<!-- v-click -->
$$\color{#6bb6ff}{x² + bx} $$

<div class="mt-14 flex items-center justify-center gap-4 text-3xl">
  <v-click>

$$ x² + bx \rightarrow $$

  </v-click>
  <v-click>

$$ \left( x + \frac{b}{2} \right)^2 $$

  </v-click>
  <v-click>

$$ \left( x + \frac{b}{2} \right)^2 $$

   </v-click>
  <v-click>

$$ - \left( \frac{b}{2} \right)^2 $$

   </v-click>
</div>

赤（例：強調部分）：#ff6b6b
青（例：bの2乗の部分など）：#6bb6ff
白（式のマイナス記号など、背景が暗い場合）：#ffffff
「Slidevのslides.md の5ページ目（平方完成の考え方）のみを修正したいです。
現在：layout: two-cols で左側が黒くなっている
希望：layout: default に変更して、v-click で→キーステップ実行の水平配置式」

---
layout: default
---

<div class="mt-14 flex items-center justify-center gap-4 text-3xl">
  <v-click class="text-[#ff6b6b]">x² + bx</v-click>
  <v-click class="text-white">→</v-click>
  <v-click>
    <span class="text-[#ff6b6b]">
      (x +
      <span class="mx-1 inline-flex flex-col items-center align-middle leading-none">
        <span class="border-b border-current px-1 text-[0.55em]">b</span>
        <span class="px-1 text-[0.55em]">2</span>
      </span>
      )²
    </span>
    <span class="text-white"> - </span>
    <span class="text-[#6bb6ff]">
      (
      <span class="mx-1 inline-flex flex-col items-center align-middle leading-none">
        <span class="border-b border-current px-1 text-[0.55em]">b</span>
        <span class="px-1 text-[0.55em]">2</span>
      </span>
      )²
    </span>
  </v-click>
</div>

$$
x^2 + bx \rightarrow \left( x + \frac{b}{2} \right)^2 - \left( \frac{b}{2} \right)^2
$$

<p class="mt-8 text-center">平方完成の変形をクリックで順に確認しましょう。</p>

---
layout: default
---

$$
x^2 + (p+q)x + pq = 0
$$

$$
\downarrow
$$

$$
(x+p)(x+q) = 0
$$

よって、

$$
x = -p, -q
$$

::right::

### 例題

$$
x^2 + 5x + 6 = 0
$$

1. かけて **6**、たして **5** になる数
2. **2** と **3** を発見！
3. $(x+2)(x+3) = 0$
4. 解は **$x = -2, -3$**

---
layout: default
---

# 3. 平方根の利用

因数分解が難しい場合、平方の形を作ります。

### 手順：

1. 定数項を右辺に移項する
2. 左辺を $(x+p)^2$ の形にする（平方完成）
3. 両辺の平方根をとる

例：$x^2 = 7 \rightarrow x = \pm\sqrt{7}$

---

# 4. 究極の武器：解の公式

どんな2次方程式でも、これに代入すれば必ず解けます。

$$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

### 判別式 $D = b^2 - 4ac$

* $D > 0$ ： 解は2つ
* $D = 0$ ： 解は1つ（重解）
* $D < 0$ ： 実数の解はない

---
layout: center
class: text-center
---

# 演習問題にチャレンジ！

1. $x^2 - 4 = 0$
2. $x^2 - 6x + 9 = 0$
3. $x^2 + 3x + 1 = 0$

解法のプロセスを紙に書き出してみましょう

---
layout: end
---

ご清聴ありがとうございました！

### 使い方

1. **Slidevのインストール**: まだの場合は、以下のコマンドで環境を作成してください。

```bash
npm init slidev@latest
```

2. **ファイルの作成**: プロジェクトフォルダ内の `slides.md` に上記のコードを貼り付けます。

3. **実行**:

```bash
npm run dev
```