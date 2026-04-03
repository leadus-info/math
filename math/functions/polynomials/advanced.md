---
title: 多項式（発展）
description: "べき乗の和で表される関数（発展）"
difficulty: 3
tags: [math,functions,polynomials,advanced]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 多項式（発展）
    href: /math/functions/polynomials/advanced.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
  - text: 専門
    href: professional.html
---







# 多項式
$x^2 + 3x - 2$ のように $x$ のべき乗の和で書ける関数が**多項式**です。
一次関数・二次関数を一般化したものです。

## このページで扱うこと
- 多項式の次数と係数
- 根と因数の関係
- 微分・積分・グラフの概形

## 前提知識
- [二次関数](professional.md)
- [代数](professional.md)
- [微分](professional.md)

---

## 定義

$$f(x) = a_n x^n + \cdots + a_1 x + a_0 \quad (a_n \neq 0)$$

$n$ が**次数**です。

---

## 根と因数定理

$f(\alpha) = 0$ となる $\alpha$ を**根**（零点）といいます。

$$f(\alpha) = 0 \iff f(x) = (x - \alpha) \cdot g(x)$$

**例**：$f(x) = x^2 - 5x + 6$

$f(2) = 0$、$f(3) = 0$ なので：

$$f(x) = (x-2)(x-3)$$

---

## 微分・積分

$$\frac{d}{dx}x^n = nx^{n-1}, \qquad \int x^n\,dx = \frac{x^{n+1}}{n+1} + C$$

---

## グラフの概形

- 次数が偶数・最高次係数が正 → 両端が上（$\cup$ 型）
- 次数が奇数・最高次係数が正 → 左下・右上に伸びる

根の場所でグラフが $x$ 軸と交わります。

---

## 関連ページ

- [二次関数](professional.md)
- [複素数](professional.md)
- [多項式（専門）](professional.md)
