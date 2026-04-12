---
title: 多項式
description: "べき乗の和で表される関数"
tags: [math,functions,polynomials]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/functions/index.md
  - title: 多項式
    path: /math/functions/polynomials/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 二次関数
    path: /math/functions/quadratic/introduction.md
  - title: 代数
    path: /math/math-language/algebra/introduction.md
---

## 一次・二次の先にある関数

$y = x$ は直線、$y = x^2$ は放物線。\
では $y = x^3$ や $y = x^4 - 3x^2 + 1$ はどんな形？

こうした「$x$ のべき乗の足し合わせ」で書ける関数が**多項式**です。

---

## 具体的に見てみる

$f(x) = x^3 - 3x$ を $x = -2, -1, 0, 1, 2$ で計算してみます。

| $x$ | $f(x)$ |
|-----|--------|
| $-2$ | $-8+6=-2$ |
| $-1$ | $-1+3=2$ |
| $0$ | $0$ |
| $1$ | $1-3=-2$ |
| $2$ | $8-6=2$ |

山があり谷がある、波のような形になります。\
次数が高いほど、こうした山谷の数が増えられます。

---

## あらゆる関数の近似

$\sin x$ や $\sqrt{x}$ のような複雑な関数も、\
多項式で近似できます。

たとえば $\sin x \approx x - \frac{x^3}{6}$（$x$ が小さいとき）。

コンピュータが三角関数や対数を計算するとき、\
内部では多項式の足し算に変換しています。

---

## 関連ページ

- [二次関数](../quadratic/introduction.md)
- [複素数](../../numbers/complex-numbers/introduction.md) — 多項式の根はすべて複素数の範囲に存在する
