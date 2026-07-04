---
title: 二次方程式
description: "因数分解と解の公式で2次の方程式を解く"
goal: "二次方程式を因数分解と解の公式で解き、判別式から解の個数を説明できるようになる"
tags: [math, algebra, equations]
stage: 中級編
subject: 代数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 中級編
    path: /math/intermediate/index.md
  - title: 二次方程式
    path: /math/intermediate/algebra/equations-quadratic.md
requires:
  - title: 一次方程式
    path: equations-linear.md
  - title: 代数
    path: expressions.md
---

## 因数分解で解く

$$ax^2 + bx + c = 0 \quad (a \neq 0)$$

因数分解できる場合は、それぞれの因数が0になる値を探します。

**例**：$x^2 - 5x + 6 = 0$。代数（中級編）の方法で因数分解すると $(x-2)(x-3) = 0$。よって $x = 2$ または $x = 3$。

---

## 解の公式

因数分解が難しい場合は、**解の公式**を使います。

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

**例**：$x^2 - 5x + 6 = 0$ に代入すると $x = \dfrac{5 \pm \sqrt{25 - 24}}{2} = \dfrac{5 \pm 1}{2}$ より $x = 3$ または $x = 2$。上の因数分解の結果と一致します。

---

## 判別式と解の個数

$b^2 - 4ac$ の符号によって、解の個数が変わります。正なら異なる2つの実数解、0なら1つの実数解（重解）、負なら実数の解はありません。

---

## まとめ

二次方程式は、因数分解できればそれぞれの因数から解が求まり、因数分解が難しい場合は解の公式で解けます。判別式 $b^2-4ac$ の符号から、実数解の個数がわかります。

---

## 関連ページ

- [連立方程式（中級編）](equations-simultaneous.md)
- [二次関数（応用編）](/math/advanced/specific-functions/quadratic.md)
