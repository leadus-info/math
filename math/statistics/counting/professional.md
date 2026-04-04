---
title: 場合の数
description: "母関数・包除原理・ラムゼー理論"
tags: [math,statistics,counting]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 統計・確率
    href: /math/statistics/index.html
  - text: 場合の数
    href: /math/statistics/counting/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: 場合の数
    url: \1/introduction.md
  - title: 数列（専門）
    url: ../../functions/sequences/professional.md
  - title: 集合（専門）
    url: ../../math-language/sets/professional.md
---










# 場合の数（発展）
母関数・包除原理・ラムゼー理論を扱います。

## このページで扱うこと
- 普通母関数・指数母関数
- 包除原理とメビウス関数
- ラムゼー数の概要

---

## 普通母関数

数列 $\{a_n\}$ に対して $G(x) = \sum a_n x^n$。

**例**: カタラン数 $C_n$ の母関数 $G(x) = \dfrac{1-\sqrt{1-4x}}{2x}$

---

## 包除原理

$$|A_1 \cup \cdots \cup A_n| = \sum|A_i| - \sum|A_i \cap A_j| + \cdots$$

**応用**: 撹乱順列の個数 $D_n = n!\sum_{k=0}^n \frac{(-1)^k}{k!} \approx n!/e$

---

## ラムゼー数

$R(m, n)$: 任意のグラフが $m$ クリークまたは $n$ 独立集合を含む最小頂点数。

$R(3,3) = 6$（6人いれば3人の知人か3人の他人が必ず存在）

---

## 関連ページ

- [場合の数](introduction.md)
- [確率（専門）](../probability/professional.md)
- [自然数（専門）](../../numbers/natural-numbers/professional.md)
