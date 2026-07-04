---
title: 多項式
description: "べき乗の和で表される関数"
goal: "多項式の基本的なアイデアと必要性を日常的な例を使って説明できるようになる"
tags: [math,algebra,polynomials]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/analysis/index.md
  - title: 多項式
    path: /math/algebra/polynomials/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 二次関数
    path: /math/specific-functions/quadratic/introduction.md
  - title: 代数
    path: /math/algebra/expressions/introduction.md
---

## 一次・二次の先へ

一次関数 $y = 2x + 1$ は「$x$ を1乗した式」です。二次関数 $y = x^2 - 3x + 2$ は「$x$ を2乗まで含む式」です。

では $y = x^3 - 2x^2 + x - 5$ のような、3乗を含む式は？

$$y = 3x^4 - x^3 + 2x - 7$$

のような4乗は？ このように「$x$ のべき乗の足し合わせ」で書ける関数をまとめて**多項式（関数）**といいます。

---

## 根——グラフが $x$ 軸と交わる点

一次関数のグラフは1点で $x$ 軸と交わります。二次関数のグラフは2点、1点、または0点で交わります。

一般に、$n$ 次の多項式のグラフは最大 $n$ 点で $x$ 軸と交わります。グラフが $x$ 軸と交わる点の $x$ 座標（$y = 0$ になる $x$ の値）を**根**（または零点）といいます。

---

## 表で形を見る

$f(x) = x^3 - 3x$ の値を計算してみましょう。

| $x$ | $-2$ | $-1$ | $0$ | $1$ | $2$ |
|-----|------|------|-----|-----|-----|
| $f(x)$ | $-2$ | $2$ | $0$ | $-2$ | $2$ |

$x = -1, 0, 1$ 付近で値が上がったり下がったりしていることがわかります。3次の多項式は山あり谷ありの形になります。

---

## あらゆる関数の「積み木」

$\sin x$ や $e^x$ のような複雑な関数も、多項式で近似できます。コンピュータが三角関数や指数関数を計算するとき、内部では多項式の計算に変換して処理しています。

---

## まとめ

多項式は「$x$ のべき乗の足し合わせ」で書ける関数の総称です。一次関数・二次関数はその特別な場合です。$n$ 次多項式は最大 $n$ 個の根を持ち、グラフは山と谷が $n-1$ 個まで現れます。

---

## 関連ページ

- [二次関数（入門）](../../specific-functions/quadratic/introduction.md)
- [代数（入門）](../expressions/introduction.md)
