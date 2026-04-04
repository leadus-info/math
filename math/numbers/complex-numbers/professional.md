---
title: 複素数
description: "代数閉体・四元数・クリフォード代数"
tags: [math,complex-numbers,complex-numbers]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数
    href: /math/numbers/index.html
  - text: 複素数
    href: /math/numbers/complex-numbers/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: 複素数
    url: \1/introduction.md
  - title: 行列（専門）
    url: ../../linear-algebra/matrices/professional.md
  - title: 四則演算（専門）
    url: ../arithmetic/professional.md
---










# 複素数（発展）
代数的閉包性・四元数・クリフォード代数を扱います。

## このページで扱うこと
- $\mathbb{C}$ が代数的閉体である意味
- 四元数 $\mathbb{H}$ と3次元回転
- クリフォード代数の概要

---

## $\mathbb{C}$ の代数的閉包性

任意の複素係数多項式は $\mathbb{C}$ 内に根を持つ（代数学の基本定理）。

$\mathbb{R}$ の代数的閉包が $\mathbb{C}$。

---

## 四元数 $\mathbb{H}$

$$\mathbb{H} = \{a+bi+cj+dk : i^2=j^2=k^2=ijk=-1\}$$

非可換体。3次元空間の回転を $q\mathbf{v}q^{-1}$（$|q|=1$）で表現します。

コンピュータグラフィクス・ロボット工学での姿勢表現に使用。

---

## クリフォード代数

ベクトル空間 $V$ と二次形式 $Q$ から構成される代数。  
$n=1$: $\mathbb{C}$、$n=2$: $\mathbb{H}$、スピノルの数学的基盤。

---

## 関連ページ

- [複素数](introduction.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
- [四則演算（専門）](../arithmetic/professional.md)
