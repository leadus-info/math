---
title: 場合の数
description: "何通りあるかを数える"
tags: [math,statistics,counting]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 統計・確率
    path: /math/statistics/index.html
  - title: 場合の数
    path: /math/statistics/counting/standard.html
levels:
  - level: introduction
    path: introduction.html
  - level: standard
  - level: professional
    path: professional.html
level: standard
requires:
  - title: 自然数
    path: /math/numbers/natural-numbers/introduction
  - title: 四則演算
    path: professional.md
---



「何通りあるか」を数えるのが場合の数です。
確率の計算の基礎になります。

## 基本原理

**積の法則**：操作 A が $m$ 通り、操作 B が $n$ 通りあるとき、AとBの組み合わせは $mn$ 通り。

例：3種類の服と4本のズボンの組み合わせは $3 \times 4 = 12$ 通り。

**和の法則**：互いに排反（同時には起きない）な事象 A と B について、A が $m$ 通り、B が $n$ 通りなら合計 $m + n$ 通り。

---

## 階乗

$$n! = n \times (n-1) \times \cdots \times 2 \times 1$$

$$0! = 1, \quad 1! = 1, \quad 5! = 120$$

---

## 順列

$n$ 個の異なるものから $r$ 個を**順番を区別して**並べる場合の数。

$$_nP_r = \frac{n!}{(n-r)!} = n(n-1)\cdots(n-r+1)$$

例：5人から3人を選んで1・2・3位を決める：$_5P_3 = 5 \times 4 \times 3 = 60$

---

## 組み合わせ

$n$ 個の異なるものから $r$ 個を**順番を区別せず**選ぶ場合の数。

$$\binom{n}{r} = \frac{n!}{r!(n-r)!} = \frac{_nP_r}{r!}$$

例：5人から3人のチームを作る：$\binom{5}{3} = \dfrac{60}{6} = 10$

順列を $r!$ で割るのは、$r$ 個の選択物の並べ方（$r!$ 通り）が同一視されるためです。

---

## 二項定理

$(a + b)^n$ を展開すると

$$(a + b)^n = \sum_{k=0}^n \binom{n}{k} a^{n-k} b^k$$

例：$(a + b)^3 = a^3 + 3a^2b + 3ab^2 + b^3$（係数 1, 3, 3, 1 は $\binom{3}{0}, \binom{3}{1}, \binom{3}{2}, \binom{3}{3}$）

---

## 関連ページ

- [確率](../probability/introduction.md)
