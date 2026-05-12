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
  <div class="flex items-center gap-2">
    1. <ruby>平方完成<rt>へいほう かんせい</rt></ruby>：
    <SpeechLine text="completing the square" lang="en-US" />
  </div>
  <div class="ml-6 text-2xl text-gray-400">
    <ruby>二次方程式<rt>にじ　　ほうていしき</rt></ruby>を<ruby>解<rt>と</rt></ruby>いたり、<ruby>関数<rt>かんすう</rt></ruby>のグラフを考えたりする<ruby>際<rt>さい</rt></ruby>に、<ruby>非常<rt>ひじょう</rt></ruby>に<ruby>重要<rt>じゅうよう</rt></ruby>なステップです。
  </div>

$$
x^2 + \color{ff6b6b}b\color{ffffff}x+\color{6bb6ff}c　　 \color{ffffff}\rightarrow　　 \left( x + \frac{\color{ff6b6b}b}{2} \right)^2 - \left( \frac{\color{ff6b6b}b}{2} \right)^2+\color{6bb6ff}c
$$

  <div class="flex items-center gap-2">
    2. <ruby>解の公式<rt>かい　こうしき</rt></ruby>：
    <SpeechLine text="quadratic formula" lang="en-US" />
  </div>

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
layout: two-cols-header
---

<div class="flex items-center gap-4  text-4xl -mt-10">
  例：

$$ \large x^2 + \color{ff6b6b}6\color{ffffff}x+\color{6bb6ff}5\color{ffffff} = 0 $$

</div>

::left::
<div class="-mt-40"> 
  <v-click>

$$　\color{808080}\Rightarrow \color{ffffff}\left( x + \frac{\color{ff6b6b}6}{2} \right)^2 - \left( \frac{\color{ff6b6b}6}{2} \right)^2+\color{6bb6ff}5\color{ffffff} = 0 $$

  </v-click>
  <v-click>

$$ \color{808080}\Rightarrow \color{ffffff}\left( x + \color{ff6b6b}3\color{ffffff}\right)^2  - \left(\color{ff6b6b}3\color{ffffff}\right)^2 + \color{6bb6ff}5\color{ffffff} = 0 $$

   </v-click>
  <v-click>

$$ \color{808080}\Rightarrow \color{ffffff}\left( x + \color{ff6b6b}3\color{ffffff}\right)^2  - \color{ff6b6b}9\color{ffffff} + \color{6bb6ff}5\color{ffffff} = 0 $$

   </v-click>
  <v-click>

$$ \color{808080}\Rightarrow \color{ffffff}\left( x + \color{ff6b6b}3\color{ffffff}\right)^2  = 4 $$

   </v-click>

</div>

::right::
<div class="-mt-40"> 
  <v-click>

$$ \color{808080}\Rightarrow \color{ffffff}\left( x + \color{ff6b6b}3\color{ffffff}\right)  = \pm\sqrt{4} $$

  </v-click>
  <v-click>

$$ \color{808080}\Rightarrow \color{ffffff}\left( x + \color{ff6b6b}3\color{ffffff}\right)  = \pm2 $$

  </v-click>
  <v-click>

$$ \color{808080}\Rightarrow  \color{ffffff}x  = \pm2 -\color{ff6b6b}3\color{ffffff} $$

  </v-click>
  <v-click>
    <div class="ml-10">よって</div>
  </v-click>

  <v-click>

$$ \color{808080}\Rightarrow  \color{ffffff}x  = -1, -5 $$

  </v-click>

</div>
<div class="flex items-center justify-center gap-4 text-3xl -mt-10">

</div>

---
layout: two-cols-header
---

<div class="flex items-center gap-4  text-4xl -mt-10">
  例：

$$ \large ax^2 + \color{ff6b6b}b\color{ffffff}x+\color{6bb6ff}c\color{ffffff} = 0 　　(a \neq 0)$$

</div>

::left::
<div class="-mt-10"> 
  <v-click>

$$　\color{808080}\Rightarrow \color{ffffff}x^2 + \frac{\color{ff6b6b}b}{a}x + \frac{\color{6bb6ff}c}{a} = 0 $$

  </v-click>
  <v-click>

$$　\color{808080}\Rightarrow \color{ffffff}\left( x + \frac{\color{ff6b6b}b}{2a} \right)^2 - \left( \frac{\color{ff6b6b}b}{2a} \right)^2+\frac{\color{6bb6ff}c}{a}  = 0 $$

  </v-click>
  <v-click>

$$　\color{808080}\Rightarrow \color{ffffff}\left( x + \frac{\color{ff6b6b}b}{2a} \right)^2 = \left( \frac{\color{ff6b6b}b}{2a} \right)^2 - \frac{\color{6bb6ff}c}{a} $$

  </v-click>
  <v-click>

$$　\color{808080}\Rightarrow \color{ffffff}\left( x + \frac{\color{ff6b6b}b}{2a} \right)^2 = \left( \frac{\color{ff6b6b}b^2}{4a^2} \right) - \frac{\color{6bb6ff}c}{a} $$

  </v-click>
</div>

::right::
<div class="-mt-10"> 
  <v-click>

$$　\color{808080}\Rightarrow \color{ffffff}\left( x + \frac{\color{ff6b6b}b}{2a} \right)^2 = \left( \frac{\color{ff6b6b}b\color{ffffff}^2 - 4a\color{6bb6ff}c}{4a^2} \right) $$

  </v-click>
  <v-click>

$$　\color{808080}\Rightarrow \color{ffffff} x + \frac{\color{ff6b6b}b}{2a} = \frac{\pm\sqrt{\color{ff6b6b}b\color{ffffff}^2 - 4a\color{6bb6ff}c}}{2a} $$

  </v-click>
  <v-click>
    <div class="ml-10">よって</div>
  </v-click>

  <v-click>

$$　\color{808080}\Rightarrow \color{ffffff} x = \frac{-\color{ff6b6b}b\color{ffffff}\pm\sqrt{\color{ff6b6b}b\color{ffffff}^2 - 4a\color{6bb6ff}c}}{2a} $$

  </v-click>


</div>

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
layout: default
---

# 小テスト(1/10)

<br>
<div class="ml-30 text-3xl space-y-4">
  次の二次方程式の解を選択肢から１つ選びなさい。 
</div>
<br>

$$ \huge x^2 = 0　$$

<br><br>
<span class="choice-label ml-40">ア</span><span class="choice-item">解なし</span>　<span class="choice-label ml-5">イ</span><span class="choice-item">０</span>　<span class="choice-label ml-5">ウ</span>　$\large±\sqrt{0}$　<span class="choice-label ml-5">エ</span>　$\large±0$

<div class="ml-85 text-3xl" style="color:yellow"> 
  <v-click>
    ＜正解＞　イ
  </v-click>
</div>

---
layout: default
---

# 小テスト(2/10)

<br>
<div class="ml-30 text-3xl space-y-4">
  次の二次方程式の解を選択肢から１つ選びなさい。 
</div>
<br>

$$ \huge x^2 = 256　$$

<br><br>
<span class="choice-label ml-40">ア</span><span class="choice-item">解なし</span>　<span class="choice-label ml-5">イ</span><span class="choice-item">０</span>　<span class="choice-label ml-5">ウ</span>　$\large±\sqrt{16}$　<span class="choice-label ml-5">エ</span>　$\large±16$

<div class="ml-85 text-3xl" style="color:yellow"> 
  <v-click>
    ＜正解＞　エ
  </v-click>
</div>


---
layout: default
---

# 小テスト(3/10)

<br>
<div class="ml-30 text-3xl space-y-4">
  次の二次方程式の解を選択肢から１つ選びなさい。 
</div>
<br>

$$ \huge x^2 + 16 = 0　$$

<br><br>
<span class="choice-label ml-40">ア</span><span class="choice-item">解なし</span>　<span class="choice-label ml-5">イ</span><span class="choice-item">０</span>　<span class="choice-label ml-5">ウ</span>　$\large±\sqrt{4}$　<span class="choice-label ml-5">エ</span>　$\large±4$

<div class="ml-85 text-3xl" style="color:yellow"> 
  <v-click>
    ＜正解＞　ア
  </v-click>
</div>

---
layout: default
---

# 小テスト(4/10)

<br>
<div class="ml-30 text-3xl space-y-4">
  次の二次方程式の解を選択肢から１つ選びなさい。 
</div>
<br>

$$ \huge x^2 + 3x = 0　$$

<br><br>
<span class="choice-label ml-20">ア</span><span class="choice-item">解なし</span>　<span class="choice-label ml-5">イ</span><span class="choice-item">０, ３</span>　<span class="choice-label ml-5">ウ</span> <span class="choice-item">０, ー３</span>　<span class="choice-label ml-5">エ</span> <span class="choice-item">０, ±３</span>

<div class="ml-85 text-3xl" style="color:yellow"> 
  <v-click>
    ＜正解＞　ウ
  </v-click>
</div>

---
layout: default
---

# 小テスト(5/10)

<br>
<div class="ml-30 text-3xl space-y-4">
  次の二次方程式の解を選択肢から１つ選びなさい。 
</div>
<br>

$$ \huge (x-3)(x+1) = 0　$$

<br><br>
<span class="choice-label ml-10">ア</span><span class="choice-item">１, ３</span>　<span class="choice-label ml-5">イ</span><span class="choice-item">ー１, ３</span>　<span class="choice-label ml-5">ウ</span> <span class="choice-item">ー１, ３</span>　<span class="choice-label ml-5">エ</span> <span class="choice-item">ー１, ー３</span>

<div class="ml-85 text-3xl" style="color:yellow"> 
  <v-click>
    ＜正解＞　イ
  </v-click>
</div>

---
layout: default
---

# 小テスト(6/10)

<br>
<div class="ml-30 text-3xl space-y-4">
  次の二次方程式の解を選択肢から１つ選びなさい。 
</div>
<br>

$$ \huge x^2+4x+4 = 0　$$

<br><br>
<span class="choice-label ml-40">ア</span><span class="choice-item">０</span>　<span class="choice-label ml-5">イ</span><span class="choice-item">２</span>　<span class="choice-label ml-5">ウ</span> <span class="choice-item">ー２</span>　<span class="choice-label ml-5">エ</span> <span class="choice-item">２, ー２</span>

<div class="ml-85 text-3xl" style="color:yellow"> 
  <v-click>
    ＜正解＞　ウ
  </v-click>
</div>

