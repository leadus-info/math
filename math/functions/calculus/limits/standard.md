---
title: 極限
description: "「限りなく近づく」とはどういうことか"
difficulty: 2
tags: [math,operations,limits]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数の操作
    href: /math/functions/calculus/index.html
  - text: 極限
    href: /math/functions/calculus/limits/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 極限
「$1$ を $10$ で割ると $0.1$、$100$ で割ると $0.01$、$1000$ で割ると $0.001$……
どんどん $0$ に近づくけど、$0$ にはならない。」

このような「限りなく近づくけど届かない」現象を扱う道具が**極限**です。

## このページで扱うこと
- 「限りなく近づく」のイメージ
- 数列の極限（$n$ を大きくしていく）
- 関数の極限（$x$ をある値に近づける）

## 前提知識
- [四則演算](../../../numbers/arithmetic/standard.md)
- [分数](../../../numbers/fractions/standard.md)

---

## 「限りなく近づく」とは？

$\frac{1}{n}$ という数列を考えます。

| $n$ | $\frac{1}{n}$ |
|-----|----------------|
| $1$ | $1$ |
| $10$ | $0.1$ |
| $100$ | $0.01$ |
| $1000$ | $0.001$ |
| $10000$ | $0.0001$ |

$n$ を大きくするほど $\frac{1}{n}$ は $0$ に近づいていきます。
「$n$ を限りなく大きくしたとき、$\frac{1}{n}$ は $0$ に限りなく近づく」ことを

$$\lim_{n \to \infty} \frac{1}{n} = 0$$

と書きます。$\infty$（無限大）は「どこまでも大きくなる」という意味の記号です。

---

## 数列の極限

数列が「ある値に限りなく近づく」とき、その値を**極限値**といいます。

$$\lim_{n \to \infty} \frac{1}{n} = 0 \quad \text{（$0$ に近づく）}$$
$$\lim_{n \to \infty} \frac{n}{n+1} = 1 \quad \text{（$1$ に近づく）}$$

近づく先が決まらない（どんどん大きくなる）場合は**発散**といいます。

$$\lim_{n \to \infty} n^2 = \infty \quad \text{（発散）}$$

---

## 関数の極限

関数でも「$x$ をある値に近づけたとき、$f(x)$ はどこへ向かうか」を考えます。

$f(x) = 2x + 1$ で $x$ を $3$ に近づけると？

| $x$ | $f(x) = 2x + 1$ |
|-----|-----------------|
| $2.9$ | $6.8$ |
| $2.99$ | $6.98$ |
| $3.001$ | $7.002$ |
| $3.0001$ | $7.0002$ |

$x$ が $3$ に近づくほど $f(x)$ は $7$ に近づきます。

$$\lim_{x \to 3} (2x + 1) = 7$$

---

## 極限の計算

足し算・掛け算などと同じように、極限も分配できます。

$\lim f(x) = L$、$\lim g(x) = M$ のとき：

$$\lim (f + g) = L + M, \quad \lim (f \times g) = L \times M$$

---

## 関連ページ

- [微分](../derivatives/standard.md) — 極限を使った変化率
- [積分](../integrals/standard.md) — 極限を使った面積
- [数列](../../../functions/sequences/standard.md)
- [極限（発展）](../limits/advanced.md) — より詳しく学ぶ
