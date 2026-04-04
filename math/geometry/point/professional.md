---
title: 点
description: "距離空間・位相空間・多様体上の点"
tags: [math,geometry,point]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 幾何
    href: /math/geometry/index.html
  - text: 点
    href: /math/geometry/point/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: 点
    url: \1/introduction.md
  - title: 集合（専門）
    url: ../../math-language/sets/professional.md
  - title: 極限（専門）
    url: ../../functions/calculus/limits/professional.md
---










# 点（発展）
距離空間・位相空間・多様体を扱います。

## このページで扱うこと
- 距離空間の公理と例
- 位相空間（開集合による定式化）
- 多様体の定義の概要

---

## 距離空間

集合 $X$ と距離関数 $d: X \times X \to [0,\infty)$ の組。

**公理**: 非負性, 対称性, 三角不等式 $d(x,z) \leq d(x,y)+d(y,z)$

---

## 位相空間

開集合族 $\mathcal{T}$ によって位相を定義——距離なしで連続性を定式化。

$$\mathcal{T} \text{ は } \emptyset, X \text{ を含み、有限交叉・任意合併について閉じる}$$

---

## 多様体

局所的に $\mathbb{R}^n$ と同相な位相空間。  
曲面（$n=2$）, 時空（$n=4$）, 位相群など。

---

## 関連ページ

- [点](introduction.md)
- [集合（専門）](../../math-language/sets/professional.md)
- [ベクトル（専門）](../../linear-algebra/vectors/professional.md)
