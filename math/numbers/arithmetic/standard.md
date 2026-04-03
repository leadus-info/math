---
title: 乗法・べき乗
description: "掛け算を積み重ねるとべき乗になる"
difficulty: 1
tags: [math,operations,arithmetic]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数
    href: /math/numbers/index.html
  - text: 乗法・べき乗
    href: /math/numbers/arithmetic/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---





# 乗法・べき乗
[自然数](../../numbers/natural-numbers/standard.md)では足し算と掛け算を学びました。
このページでは掛け算をさらに積み重ねた**べき乗**と、その逆操作の**平方根**を扱います。

## このページで扱うこと
- べき乗とは（同じ数を繰り返し掛ける）
- 指数の計算ルール
- 平方根（ルート）

## 前提知識
- [自然数](../../numbers/natural-numbers/standard.md) — 掛け算の基礎
- [分数](../../numbers/fractions/standard.md) — 分数のべき乗

---

## べき乗とは？

$2$ を $3$ 回掛けることを $2^3$ と書きます。

$$2^3 = 2 \times 2 \times 2 = 8$$

$3$ のことを**指数**（または**累乗の指数**）といいます。

$$\underbrace{a \times a \times \cdots \times a}_{n \text{ 回}} = a^n$$

| 式 | 読み方 | 計算 |
|----|--------|------|
| $2^1$ | $2$ の $1$ 乗 | $2$ |
| $2^2$ | $2$ の $2$ 乗（$2$ の二乗） | $4$ |
| $2^3$ | $2$ の $3$ 乗（$2$ の三乗） | $8$ |
| $2^4$ | $2$ の $4$ 乗 | $16$ |
| $2^{10}$ | $2$ の $10$ 乗 | $1024$ |

---

## 特別なべき乗

$$a^1 = a, \qquad a^0 = 1 \quad (a \neq 0)$$

「$0$ 乗は $1$」は最初は不思議に感じますが、
指数の計算ルールから自然に決まります。

---

## 指数の計算ルール

**同じ底を掛けるとき**：指数を足します。

$$2^3 \times 2^4 = \underbrace{2 \times 2 \times 2}_{3} \times \underbrace{2 \times 2 \times 2 \times 2}_{4} = 2^7$$

$$a^m \times a^n = a^{m+n}$$

**べき乗のべき乗**：指数を掛けます。

$$(2^3)^2 = (2 \times 2 \times 2) \times (2 \times 2 \times 2) = 2^6$$

$$(a^m)^n = a^{m \times n}$$

**負の指数**（分数への拡張）：

$$2^{-1} = \frac{1}{2}, \quad 2^{-3} = \frac{1}{2^3} = \frac{1}{8}$$

$$a^{-n} = \frac{1}{a^n}$$

---

## 平方根（ルート）

「$x^2 = 9$ を満たす $x$ は？」——つまりべき乗の逆を求めることがあります。

$3^2 = 9$ なので、答えは $x = 3$ です。
これを $\sqrt{9} = 3$（$9$ の**平方根**は $3$）と書きます。

$$\sqrt{1} = 1, \quad \sqrt{4} = 2, \quad \sqrt{9} = 3, \quad \sqrt{16} = 4, \quad \sqrt{25} = 5$$

$$\sqrt{2} = 1.414\ldots \quad \text{（分数で表せない！）}$$

$\sqrt{2}$ は有限小数でも分数でも表せない数（**無理数**）です。

---

## べき乗で見る小数の仕組み

べき乗を学んだ今、[小数](../../numbers/decimals/standard.md)の仕組みをより簡潔に書き直せます。

$$0.1 = 10^{-1}, \quad 0.01 = 10^{-2}, \quad 0.001 = 10^{-3}$$

なので、

$$3.14 = 3 	imes 10^0 + 1 	imes 10^{-1} + 4 	imes 10^{-2}$$

小数点以下の各桁は「$10$ の負のべき乗」の係数です。
これは $10$ 進数という記数法の構造そのものです。

---

## 関連ページ

- [指数関数](../../functions/exponential/standard.md) — べき乗を関数として見る
- [等号・等式](../../math-language/equations/standard.md)
- [乗法・べき乗（発展）](../arithmetic/advanced.md) — より詳しく学ぶ
