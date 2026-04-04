---
title: 点
description: "距離空間・位相空間・多様体上の点"
tags: [math,geometry,point]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 幾何
    path: /math/geometry/index.html
  - title: 点
    path: /math/geometry/point/professional.html
levels:
  - level: 入門
    path: introduction.html
  - level: 標準
    path: standard.html
  - level: 専門
level: 専門
requires:
  - title: 点
    path: /math/geometry/point/introduction
  - title: 集合（専門）
    path: ../../math-language/sets/professional.md
  - title: 極限（専門）
    path: ../../functions/limits/professional.md
---




> この記事は [標準](standard.md) の続きです。先に標準を読むことを推奨します。

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
