---
title: 極限
description: "限りなく近づくとはどういうことか"
tags: [math,operations,limits]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数の操作
    href: /math/functions/calculus/index.html
  - text: 極限
    href: /math/functions/calculus/limits/standard.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
  - level: professional
    url: professional.html
level: standard
requires:
  - title: 乗法・べき乗
    url: professional.md
  - title: 分数
    url: professional.md
---









# 極限
「どんどん近づいていくと、最終的にどこに向かうのか」——これが**極限**です。
微分も積分も、極限という考え方の上に成り立っています。

## このページで扱うこと
- 極限の直感的な意味
- 数列の極限
- 関数の極限と計算規則

---

## 数列の極限

$\dfrac{1}{n}$ を $n = 1, 2, 3, \ldots$ と大きくしていくと：

$$1,\ 0.5,\ 0.333\ldots,\ 0.25,\ \ldots$$

どんどん 0 に近づきます。「$n$ を限りなく大きくしたとき 0 に近づく」と言い、

$$\lim_{n \to \infty} \frac{1}{n} = 0$$

と書きます。

---

## 関数の極限

$x$ を 2 に近づけたとき $f(x) = 3x + 1$ はどこへ向かうか？

| $x$ | $f(x)$ |
|-----|--------|
| $1.9$ | $6.7$ |
| $1.99$ | $6.97$ |
| $2.001$ | $7.003$ |
| $2.0001$ | $7.0003$ |

7 に近づいていきます。

$$\lim_{x \to 2}(3x + 1) = 7$$

---

## 極限の計算規則

$\lim f = L$、$\lim g = M$ のとき：

$$\lim (f + g) = L + M$$
$$\lim (f \times g) = L \times M$$
$$\lim \frac{f}{g} = \frac{L}{M} \quad (M \neq 0)$$

---

## よく使う極限

$$\lim_{n \to \infty} r^n = 0 \quad (|r| < 1 \text{ のとき})$$

例：$0.9^n$ は $n$ が大きくなるほど 0 に近づきます。

---

## 関連ページ

- [微分](professional.md)
- [積分](professional.md)
- [数列](professional.md)
- [極限（専門）](professional.md) — $\varepsilon$-$\delta$ 論法
