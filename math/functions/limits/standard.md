---
title: 極限
description: "限りなく近づくとはどういうことか"
tags: [math,operations,limits]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 関数の操作
    url: /math/functions/index.html
  - title: 極限
    url: /math/functions/limits/standard.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
  - level: professional
    url: professional.html
level: standard
requires:
  - title: 乗法・べき乗
    url: /math/numbers/arithmetic/introduction
  - title: 分数
    url: /math/numbers/fractions/introduction
---


「限りなく近づくとどこへ向かうか」——これが極限です。
微分も積分も、この概念の上に成り立っています。

## 数列の極限

$n$ を大きくしていくにつれて $\dfrac{1}{n}$ がどう変化するか見てみます。

$$\frac{1}{1} = 1, \quad \frac{1}{2} = 0.5, \quad \frac{1}{10} = 0.1, \quad \frac{1}{100} = 0.01, \quad \ldots$$

$n$ が大きくなるほど $\dfrac{1}{n}$ は 0 に近づきます。
「$n$ を限りなく大きくしたとき $\dfrac{1}{n}$ は 0 に収束する」といい、

$$\lim_{n \to \infty} \frac{1}{n} = 0$$

と書きます。

一般に、数列 $\{a_n\}$ が値 $L$ に収束するとは、$n$ を大きくしたとき $a_n$ が $L$ に限りなく近づくことです。
収束先がない場合（$n^2$ のように限りなく大きくなる場合など）を**発散**といいます。

---

## 関数の極限

$x$ を 2 に近づけたとき、$f(x) = 3x + 1$ はどこへ向かうか？

| $x$ | $f(x)$ |
|-----|--------|
| $1.9$ | $6.7$ |
| $1.99$ | $6.97$ |
| $2.001$ | $7.003$ |
| $2.0001$ | $7.0003$ |

$x$ が 2 に近づくほど $f(x)$ は 7 に近づきます。これを

$$\lim_{x \to 2}(3x + 1) = 7$$

と書きます。注意：「$x$ を**2に近づける**」であって「$x = 2$ を代入する」ではありません。
近づく過程が重要です（$x = 2$ で定義されていない関数でも極限が存在することがあります）。

---

## 極限の計算規則

$\lim_{x \to a} f(x) = L$、$\lim_{x \to a} g(x) = M$ のとき：

$$\lim_{x \to a} (f + g)(x) = L + M$$
$$\lim_{x \to a} (f \cdot g)(x) = L \cdot M$$
$$\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{L}{M} \quad (M \neq 0)$$

つまり、極限と四則演算は交換できます。

---

## よく使う極限

$$\lim_{n \to \infty} r^n = 0 \quad (|r| < 1 \text{ のとき})$$

例：$0.9^n$ は $n$ が大きくなるほど 0 に近づきます。$0.9^{10} \approx 0.35$、$0.9^{100} \approx 0.000027$。

---

## 片側極限

$x$ を左から近づける場合と右から近づける場合で区別することがあります。

- 右側極限：$\lim_{x \to a^+} f(x)$（$x > a$ の側から近づける）
- 左側極限：$\lim_{x \to a^-} f(x)$（$x < a$ の側から近づける）

両側極限 $\lim_{x \to a} f(x)$ が存在するのは、左右の極限が等しい場合に限ります。

---

## 関連ページ

- [微分](../derivatives/introduction.md) — 極限を使った変化率の定義
- [積分](../integrals/introduction.md) — 極限を使った面積の定義
- [数列](../sequences/introduction.md)
