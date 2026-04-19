---
title: 等号・等式
description: "等号の性質と方程式の解法"
goal: "等号の性質を正確に述べ、一次方程式・二次方程式・連立方程式を解けるようになる"
tags: [math,algebra,equations]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 代数
    path: /math/algebra/index.md
  - title: 等号・等式
    path: /math/algebra/equations/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 等号・等式（入門）
    path: /math/algebra/equations/introduction.md
  - title: 自然数（標準）
    path: /math/numbers/natural-numbers/standard.md
  - title: 負数（標準）
    path: /math/numbers/integers/standard.md
---

## 等号の性質

等号 $=$ は次の三つの性質を持ちます。

**反射律**：$a = a$（どんな数も自分自身と等しい）

**対称律**：$a = b$ ならば $b = a$（左右を入れ替えても等しい）

**推移律**：$a = b$ かつ $b = c$ ならば $a = c$（等しいもの同士をつなげられる）

これらの性質を合わせて、等号は**同値関係**であるといいます。

---

## 等式の変形

等号・等式（入門）で見た「両辺に同じ操作をしても等号は保たれる」を正確に述べます。

$$a = b \implies a + c = b + c$$
$$a = b \implies a \times c = b \times c$$

ただし、乗法では $c = 0$ の場合に注意が必要です。$0 \times a = 0 \times b = 0$ は $a \neq b$ でも成り立つので、$c = 0$ を掛けると情報が失われます。

---

## 一次方程式

未知数 $x$ が1次の方程式です。

$$2x + 3 = 7$$

両辺から3を引きます。$2x = 4$。両辺を2で割ります。$x = 2$。

確かめ：$2 \times 2 + 3 = 7$ ✓

一般に $ax + b = c$（$a \neq 0$）の解は $x = \frac{c - b}{a}$ です。

---

## 二次方程式

$$ax^2 + bx + c = 0 \quad (a \neq 0)$$

**解の公式**：

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

これは**平方完成**から導かれます。$a\left(x + \frac{b}{2a}\right)^2 = \frac{b^2 - 4ac}{4a}$ と変形し、両辺を $a$ で割って平方根を取ります。

**判別式** $D = b^2 - 4ac$ で実数解の個数が決まります。$D > 0$ なら異なる2つの実数解、$D = 0$ なら重解（1つ）、$D < 0$ なら実数解なし。

**例**：$x^2 - 5x + 6 = 0$。$D = 25 - 24 = 1 > 0$。$x = \frac{5 \pm 1}{2}$ より $x = 3$ または $x = 2$。因数分解でも $(x-2)(x-3) = 0$ と確認できます。

---

## 連立方程式

複数の等式を同時に満たす未知数の組を求めます。

**例**：

$$\begin{cases} 2x + y = 5 \\ x - y = 1 \end{cases}$$

2式を加算すると $3x = 6$、よって $x = 2$。代入すると $y = 5 - 4 = 1$。解は $(x, y) = (2, 1)$ です。

---

## 関連ページ

- [不等号・不等式（標準）](../inequalities/standard.md)
- [代数（標準）](../expressions/standard.md)