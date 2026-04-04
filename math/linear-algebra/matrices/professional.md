---
title: 行列
description: "スペクトル定理・特異値分解・リー代数"
tags: [math,linear-algebra,matrices]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 線形代数
    path: /math/linear-algebra/index.html
  - title: 行列
    path: /math/linear-algebra/matrices/professional.html
levels:
  - level: 入門
    path: introduction.html
  - level: 標準
    path: standard.html
  - level: 専門
level: 専門
requires:
  - title: 行列
    path: /math/linear-algebra/matrices/introduction.html
  - title: ベクトル（専門）
    path: ../vectors/professional.md
  - title: 複素数
    path: /math/numbers/complex-numbers/introduction.html
---


## このページで扱うこと

スペクトル定理・特異値分解・リー代数を扱います。

- スペクトル定理（対称行列の対角化）
- 特異値分解（SVD）
- 行列のリー群・リー代数

---

## スペクトル定理

実対称行列は直交行列で対角化可能:

$$A = Q\Lambda Q^\top,\quad Q^\top Q = I$$

すべての固有値は実数。

---

## 特異値分解（SVD）

任意の $m \times n$ 行列 $A$ は:

$$A = U\Sigma V^\top$$

$U$: $m\times m$ 直交, $\Sigma$: 対角（特異値）, $V$: $n\times n$ 直交

データ圧縮・次元削減・擬似逆行列に応用。

---

## リー群とリー代数

行列のなす群（例: $GL(n)$, $SO(n)$, $SU(n)$）を**リー群**といいます。

接空間（単位元での接線空間）が**リー代数**（交換子積 $[A,B]=AB-BA$）。

---

## 関連ページ

- [行列](introduction.md)
- [ベクトル（専門）](../vectors/professional.md)
- [複素数（専門）](../../numbers/complex-numbers/professional.md)
