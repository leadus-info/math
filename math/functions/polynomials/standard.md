---
title: 多項式
description: "べき乗の和で表される関数"
difficulty: 2
tags: [math,functions,polynomials]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 多項式
    href: /math/functions/polynomials/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 多項式
$x^3 - 2x + 1$ のような、$x$ のべき乗の足し合わせで表される関数が**多項式**です。
一次関数・二次関数の自然な拡張です。

## このページで扱うこと
- 多項式の次数と係数
- 根（$y = 0$ になる $x$ の値）
- グラフの大まかな形

## 前提知識
- [二次関数](../quadratic/standard.md)
- [代数](../../math-language/algebra/standard.md)

---

## 多項式とは？

$$f(x) = x^3 - 2x + 1$$

$x^3$、$-2x$、$1$ という各項の和です。

$$f(x) = a_n x^n + a_{n-1}x^{n-1} + \cdots + a_1 x + a_0$$

- **次数**：最も大きいべき乗の数（例：$x^3$ なら $3$ 次）
- **係数**：各項の数の部分（$a_n,\ a_{n-1},\ \ldots$）

---

## 根（零点）

$f(x) = 0$ となる $x$ の値を**根**（または**零点**）といいます。

**因数定理**：$f(\alpha) = 0$ なら $(x - \alpha)$ で割り切れます。

$$f(x) = x^2 - 5x + 6 \text{ で } f(2) = 0 \text{、} f(3) = 0$$
$$\implies f(x) = (x-2)(x-3)$$

---

## 微分・積分

べき乗則を各項に適用します。

$$(x^n)' = nx^{n-1}, \quad \int x^n\,dx = \frac{x^{n+1}}{n+1} + C$$

---

## グラフの概形

- **偶数次・最高次係数が正**：両端が上に向く（$\cup$ 型）
- **奇数次・最高次係数が正**：左端が下、右端が上に向く

根の位置でグラフが $x$ 軸と交わります。

---

## 関連ページ

- [二次関数](../quadratic/standard.md)
- [多項式（発展）](../polynomials/advanced.md) — より詳しく学ぶ
