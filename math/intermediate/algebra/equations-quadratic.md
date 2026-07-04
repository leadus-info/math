---
title: 二次方程式
description: "因数分解・平方完成・解の公式で2次の方程式を解く"
goal: "二次方程式を因数分解・平方完成・解の公式で解き、判別式から解の個数を説明できるようになる"
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
  - title: 展開・因数分解
    path: expressions-expansion-factoring.md
  - title: 平方根
    path: /math/intermediate/numbers/arithmetic-square-root.md
---

## 因数分解で解く

$$ax^2 + bx + c = 0 \quad (a \neq 0)$$

因数分解できる場合は、それぞれの因数が0になる値を探します。

**例**：$x^2 - 5x + 6 = 0$。展開・因数分解（中級編）の方法で因数分解すると $(x-2)(x-3) = 0$。よって $x = 2$ または $x = 3$。

---

## 平方完成で解く

因数分解できない場合でも、式を $(x+p)^2 = q$ の形に変形できれば、平方根を使って解けます。この変形を**平方完成**といいます。

**例題**：$x^2 + 4x - 3 = 0$ を平方完成で解く。

定数項を右辺に移項します。

$$x^2 + 4x = 3$$

左辺を $(x+p)^2$ の形にするため、$x$ の係数4の半分の2乗（$2^2=4$）を両辺に足します。

$$x^2 + 4x + 4 = 3 + 4 \implies (x+2)^2 = 7$$

両辺の平方根をとると、

$$x + 2 = \pm\sqrt{7} \implies x = -2 \pm \sqrt{7}$$

---

## 解の公式

平方完成は、$ax^2+bx+c=0$ の形のまま一般に行うことで、公式として使えるようにできます。因数分解できない場合や、平方完成の計算が面倒な場合は、この**解の公式**を使うと素早く解けます。

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

**例**：$x^2 - 5x + 6 = 0$ に代入すると $x = \dfrac{5 \pm \sqrt{25 - 24}}{2} = \dfrac{5 \pm 1}{2}$ より $x = 3$ または $x = 2$。上の因数分解の結果と一致します。

---

## 判別式と解の個数

$b^2 - 4ac$ の符号によって、解の個数が変わります。正なら異なる2つの実数解、0なら1つの実数解（重解）、負なら実数の解はありません。

---

## まとめ

二次方程式は、因数分解できればそれぞれの因数から解が求まります。因数分解できない場合は、平方完成で $(x+p)^2=q$ の形に変形して平方根をとるか、同じ考え方を一般化した解の公式を使って解けます。判別式 $b^2-4ac$ の符号から、実数解の個数がわかります。

---

## 関連ページ

- [連立方程式（中級編）](equations-simultaneous.md)
- [二次関数（応用編）](/math/advanced/specific-functions/quadratic.md)
