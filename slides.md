---
theme: seriph
background: https://images.unsplash.com/photo-1635070041078-e363dbe005cb?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80
class: text-center
# colorSchema options:
# colorSchema: light
colorSchema: dark
highlighter: shiki
lineNumbers: true
drawings:
  persist: false
transition: slide-left
title: 2次方程式の解法
---

# 2次方程式の解法マスターガイド

基礎から解の公式まで

講義を開始する

---
layout: default
---

# 本日のゴール

2次方程式を解くための「3つの武器」を習得しましょう。

1. **因数分解**：最も効率的な「基本の剣」
2. **平方根の考え方**：理屈で攻める「論理の杖」
3. **解の公式**：どんな敵も倒せる「伝説の盾」

---
layout: section
---

# 1. 2次方程式の定義

まずは敵の姿を知る

---

# 2次方程式の一般形

すべての2次方程式は、整理すると以下の形になります。

$$
ax^2 + bx + c = 0
$$

### 重要なルール

* **$a, b, c$** は定数（決まった数字）
* **$a \neq 0$** であること（$a=0$だと1次方程式になってしまうため）

---
layout: two-cols
---

# 2. 因数分解による解法

「かけて$c$、たして$b$」になる2数を見つける方法です。

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