---
theme: seriph
background: https://images.pexels.com/photos/6238050/pexels-photo-6238050.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=1080&w=1920
# background: /bg.png
class: text-center
# colorSchema options:
colorSchema: light
# colorSchema: dark
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

  <!-- 
  <div class="ml-6 text-2xl text-gray-400">
    <ruby>二次方程式<rt>にじ　　ほうていしき</rt></ruby>を<ruby>解<rt>と</rt></ruby>いたり、<ruby>関数<rt>かんすう</rt></ruby>のグラフを考えたりする<ruby>際<rt>さい</rt></ruby>に、<ruby>非常<rt>ひじょう</rt></ruby>に<ruby>重要<rt>じゅうよう</rt></ruby>なステップです。
  </div>
-->

$$
x^2 + \color{ff6b6b}b\color{black}x+\color{6bb6ff}c　　 \color{black}\rightarrow　　 \left( x + \frac{\color{ff6b6b}b}{2} \right)^2 - \left( \frac{\color{ff6b6b}b}{2} \right)^2+\color{6bb6ff}c
$$

  <div class="flex items-center gap-2">
    2. <ruby>解の公式<rt>かい　こうしき</rt></ruby>：
    <SpeechLine text="quadratic formula" lang="en-US" />
  </div>

$$
x^2 + (\color{ff6b6b}p\color{black}+\color{6bb6ff}q\color{black})x + \color{ff6b6b}p\color{6bb6ff}q \color{black}= 0　　\rightarrow　　(x+\color{ff6b6b}p\color{black})(x+\color{6bb6ff}q\color{black}) = 0
$$

$$
x^2 + 2\color{ff6b6b}b\color{black}x + \color{ff6b6b}b\color{black}^2 = 0　　\rightarrow　　(x+\color{ff6b6b}b\color{black})^2 = 0
$$

$$black
x^2 - 2\color{ff6b6b}b\color{black}x +\color{ff6b6b} b\color{black}^2 = 0　　\rightarrow　　(x-\color{ff6b6b}b\color{black})^2 = 0
$$

</div>

---
layout: default
---

# 平方根の利用

<ruby>因数分解<rt>いんすうぶんかい</rt></ruby>が<ruby>難<rt>むずか</rt></ruby>しい場合、<ruby>平方<rt>へいほう</rt></ruby>の<ruby>形<rt>かたち</rt></ruby>を<ruby>作<rt>つく</rt></ruby>ります。

$$
x^2 + \color{ff6b6b}b\color{black}x+\color{6bb6ff}c \color{black} = 0　 \color{ffffblackff}\rightarrow　　 \left( x + \frac{\color{ff6b6b}b}{2} \right)^2 - \left( \frac{\color{ff6b6b}b}{2} \right)^2+\color{6bb6ff}c \color{black} = 0
$$

### <ruby>手順<rt>てじゅん</rt></ruby>：
<br>

  1. <ruby>定数項<rt>ていすうこう</rt></ruby>を<ruby>右辺<rt>うへん</rt></ruby>に<ruby>移項<rt>いこう</rt></ruby>する
 
  2. <ruby>左辺<rt>さへん</rt></ruby>を $(x+p)^2$ の<ruby>形<rt>かたち</rt></ruby>にする（<ruby>平方完成<rt>へいほうかんせい</rt></ruby>）→　<ruby>四角<rt>しかく</rt></ruby>にする

  3. <ruby>両辺<rt>りょうへん</rt></ruby>の<ruby>平方根<rt>へいほうこん</rt></ruby>をとる

---
layout: two-cols-header
---

<div class="flex items-center gap-4  text-4xl -mt-10">
  例：

$$ \large x^2 + \color{ff6b6b}{6x}+\color{6bb6ff}5\color{black} = 0 $$
</div>

::left::
<div class="-mt-40"> 
  <v-click>

$$　\color{808080}\Rightarrow \color{black}\left( x + \frac{\color{ff6b6b}6}{2} \right)^2 - \left( \frac{\color{ff6b6b}6}{2} \right)^2+\color{6bb6ff}5\color{black} = 0 $$

  </v-click>
  <v-click>

$$ \color{808080}\Rightarrow \color{black}\left( x + \color{ff6b6b}3\color{black}\right)^2  - \left(\color{ff6b6b}3\color{black}\right)^2 + \color{6bb6ff}5\color{black} = 0 $$

   </v-click>
  <v-click>

$$ \color{808080}\Rightarrow \color{black}\left( x + \color{ff6b6b}3\color{black}\right)^2  - \color{ff6b6b}9\color{black} + \color{6bb6ff}5\color{black} = 0 $$

   </v-click>
  <v-click>

$$ \color{808080}\Rightarrow \color{black}\left( x + \color{ff6b6b}3\color{black}\right)^2  = 4 $$

   </v-click>

</div>

::right::
<div class="-mt-40"> 
  <v-click>

$$ \color{808080}\Rightarrow \color{black}\left( x + \color{ff6b6b}3\color{black}\right)  = \pm\sqrt{4} $$

  </v-click>
  <v-click>

$$ \color{808080}\Rightarrow \color{black}\left( x + \color{ff6b6b}3\color{black}\right)  = \pm2 $$

  </v-click>
  <v-click>

$$ \color{808080}\Rightarrow  \color{black}x  = \pm2 -\color{ff6b6b}3\color{black} $$

  </v-click>
  <v-click>
    <div class="ml-10">よって</div>
  </v-click>

  <v-click>

$$ \color{808080}\Rightarrow  \color{black}x  = -1, -5 $$

  </v-click>

</div>
<div class="flex items-center justify-center gap-4 text-3xl -mt-10">

</div>

---
layout: two-cols-header
---

<div class="flex items-center gap-4  text-4xl -mt-10">
  例：

$$ \large ax^2 + \color{ff6b6b}b\color{black}x+\color{6bb6ff}c\color{black} = 0 　　(a \neq 0)$$

</div>

::left::
<div class="-mt-10"> 
  <v-click>

$$　\color{808080}\Rightarrow \color{black}x^2 + \frac{\color{ff6b6b}b}{a}x + \frac{\color{6bb6ff}c}{a} = 0 $$

  </v-click>
  <v-click>

$$　\color{808080}\Rightarrow \color{black}\left( x + \frac{\color{ff6b6b}b}{2a} \right)^2 - \left( \frac{\color{ff6b6b}b}{2a} \right)^2+\frac{\color{6bb6ff}c}{a}  = 0 $$

  </v-click>
  <v-click>

$$　\color{808080}\Rightarrow \color{black}\left( x + \frac{\color{ff6b6b}b}{2a} \right)^2 = \left( \frac{\color{ff6b6b}b}{2a} \right)^2 - \frac{\color{6bb6ff}c}{a} $$

  </v-click>
  <v-click>

$$　\color{808080}\Rightarrow \color{black}\left( x + \frac{\color{ff6b6b}b}{2a} \right)^2 = \left( \frac{\color{ff6b6b}b^2}{4a^2} \right) - \frac{\color{6bb6ff}c}{a} $$

  </v-click>
</div>

::right::
<div class="-mt-10"> 
  <v-click>

$$　\color{808080}\Rightarrow \color{black}\left( x + \frac{\color{ff6b6b}b}{2a} \right)^2 = \left( \frac{\color{ff6b6b}b\color{black}^2 - 4a\color{6bb6ff}c}{4a^2} \right) $$

  </v-click>
  <v-click>

$$　\color{808080}\Rightarrow \color{black} x + \frac{\color{ff6b6b}b}{2a} = \frac{\pm\sqrt{\color{ff6b6b}b\color{black}^2 - 4a\color{6bb6ff}c}}{2a} $$

  </v-click>
  <v-click>
    <div class="ml-10">よって</div>
  </v-click>

  <v-click>

$$　\color{808080}\Rightarrow \color{black} x = \frac{-\color{ff6b6b}b\color{black}\pm\sqrt{\color{ff6b6b}b\color{black}^2 - 4a\color{6bb6ff}c}}{2a} $$

  </v-click>


</div>

---

# 究極の武器：解の公式

どんな<ruby>二次方程式<rt>にじ　ほうていしき</rt></ruby>でも、これに<ruby>代入<rt>だいにゅう</rt></ruby>すれば<ruby>必<rt>かなら</rt></ruby>ず<ruby>解<rt>と</rt></ruby>けます。

$$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

### 判別式 $D = b^2 - 4ac$

* $D > 0$ ： <ruby>解<rt>かい</rt></ruby>は2つ
* $D = 0$ ： <ruby>解<rt>かい</rt></ruby>は1つ（<ruby>重解<rt>じゅうかい</rt></ruby>）
* $D < 0$ ： <ruby>実数<rt>じっすう</rt></ruby>の<ruby>解<rt>かい</rt></ruby>はない


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

<div class="ml-85 text-3xl" style="color:orange; font-weight:bold;"> 
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

<div class="ml-85 text-3xl" style="color:orange; font-weight: bold; "> 
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

<div class="ml-85 text-3xl" style="color:orange; font-weight: bold; "> 
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

<div class="ml-85 text-3xl" style="color:orange; font-weight: bold; "> 
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
<span class="choice-label ml-10">ア</span><span class="choice-item">１, ３</span>　<span class="choice-label ml-5">イ</span><span class="choice-item">ー１, ３</span>　<span class="choice-label ml-5">ウ</span> <span class="choice-item">１, ー３</span>　<span class="choice-label ml-5">エ</span> <span class="choice-item">ー１, ー３</span>

<div class="ml-85 text-3xl" style="color:orange; font-weight: bold; "> 
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

$$ \huge x^2+2x+1 = 0　$$

<br><br>
<span class="choice-label ml-40">ア</span><span class="choice-item">０</span>　<span class="choice-label ml-5">イ</span><span class="choice-item">１</span>　<span class="choice-label ml-5">ウ</span> <span class="choice-item">ー１</span>　<span class="choice-label ml-5">エ</span> <span class="choice-item">１, ー１</span>

<div class="ml-85 text-3xl" style="color:orange; font-weight: bold; "> 
  <v-click>
    ＜正解＞　ウ
  </v-click>
</div>

---
layout: default
---

# 小テスト(7/10)

<br>
<div class="ml-30 text-3xl space-y-4">
  次の二次方程式の解を選択肢から１つ選びなさい。 
</div>
<br>

$$ \huge x^2+4x+4 = 0　$$

<br><br>
<span class="choice-label ml-40">ア</span><span class="choice-item">０</span>　<span class="choice-label ml-5">イ</span><span class="choice-item">２</span>　<span class="choice-label ml-5">ウ</span> <span class="choice-item">ー２</span>　<span class="choice-label ml-5">エ</span> <span class="choice-item">２, ー２</span>

<div class="ml-85 text-3xl" style="color:orange; font-weight: bold; "> 
  <v-click>
    ＜正解＞　ウ
  </v-click>
</div>

---
layout: default
---

# 小テスト(8/10)

<br>
<div class="ml-30 text-3xl space-y-4">
  次の二次方程式の解を選択肢から１つ選びなさい。 
</div>
<br>

$$ \huge x^2+6x+9 = 0　$$

<br><br>
<span class="choice-label ml-40">ア</span><span class="choice-item">０</span>　<span class="choice-label ml-5">イ</span><span class="choice-item">３</span>　<span class="choice-label ml-5">ウ</span> <span class="choice-item">ー３</span>　<span class="choice-label ml-5">エ</span> <span class="choice-item">３, ー３</span>

<div class="ml-85 text-3xl" style="color:orange; font-weight: bold; "> 
  <v-click>
    ＜正解＞　ウ
  </v-click>
</div>

---
layout: default
---

# 小テスト(9/10)

<br>
<div class="ml-30 text-3xl space-y-4">
  次の二次方程式の解を選択肢から１つ選びなさい。 
</div>
<br>

$$ \huge x^2+2x = 3　$$

<br><br>
<span class="choice-label ml-40">ア</span><span class="choice-item">０</span>　<span class="choice-label ml-5">イ</span><span class="choice-item">１</span>　<span class="choice-label ml-5">ウ</span> <span class="choice-item">ー３</span>　<span class="choice-label ml-5">エ</span> <span class="choice-item">１, ー３</span>

<div class="ml-85 text-3xl" style="color:orange; font-weight: bold; "> 
  <v-click>
    ＜正解＞　エ
  </v-click>
</div>

---
layout: default
---

# 小テスト(10/10)

<br>
<div class="ml-30 text-3xl space-y-4">
  二次方程式の解の<ruby>公式<rt>こうしき</rt></ruby>を答えなさい。 
</div>
<br>

$$ \large ax^2 + \color{ff6b6b}b\color{black}x+\color{6bb6ff}c\color{black} = 0 　　(a \neq 0)$$

<div class="ml-5 text-3xl" style="color:orenge"> 
  <v-click>
    ＜正解＞　

$$　x = \frac{-\color{ff6b6b}b\color{black}\pm\sqrt{\color{ff6b6b}b\color{black}^2 - 4a\color{6bb6ff}c}}{2a} $$

  </v-click>
</div>
