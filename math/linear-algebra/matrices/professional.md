---
title: 行列（専門）
description: "スペクトル定理・特異値分解・リー代数"
difficulty: 6
tags: [math,linear-algebra,matrices,professional]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 線形代数
    href: /math/linear-algebra/index.html
  - text: 行列（専門）
    href: /math/linear-algebra/matrices/professional.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
    href: advanced.html
  - text: 専門
---








# 行列（発展）
スペクトル定理・特異値分解・リー代数を扱います。

## このページで扱うこと
- スペクトル定理（対称行列の対角化）
- 特異値分解（SVD）
- 行列のリー群・リー代数

## 前提知識
- [行列](../matrices/standard.md)
- [ベクトル（専門）](../vectors/professional.md)
- [複素数](../../numbers/complex-numbers/standard.md)

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

- [行列](../matrices/standard.md)
- [ベクトル（専門）](../vectors/professional.md)
- [複素数（専門）](../../numbers/complex-numbers/professional.md)
