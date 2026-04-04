---
title: ベクトル
description: "内積空間・ヒルベルト空間・双対空間"
tags: [math,linear-algebra,vectors]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 線形代数
    url: /math/linear-algebra/index.html
  - title: ベクトル
    url: /math/linear-algebra/vectors/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: ベクトル
    url: \1/introduction.md
  - title: 極限（専門）
    url: ../../functions/limits/professional.md
  - title: 積分（専門）
    url: ../../functions/integrals/professional.md
---



内積空間・ヒルベルト空間・双対空間を扱います。

## このページで扱うこと
- 内積空間の公理とグラム・シュミット直交化
- ヒルベルト空間と完備性
- 双対空間とリース表現定理

---

## 内積空間

$\langle \cdot, \cdot \rangle: V \times V \to \mathbb{F}$ が線形性・対称性・正定値性を満たす。

**コーシー・シュワルツ**: $|\langle u, v\rangle| \leq \|u\|\|v\|$

---

## グラム・シュミット直交化

線形独立なベクトル列 $\{v_1, \ldots, v_n\}$ から正規直交基底を構成:

$$u_k = v_k - \sum_{j<k}\langle v_k, e_j\rangle e_j,\quad e_k = u_k/\|u_k\|$$

---

## ヒルベルト空間

完備な内積空間。$L^2([0,1])$、$\ell^2$ など。

フーリエ級数はヒルベルト空間 $L^2$ での正規直交展開。

---

## 双対空間とリース表現定理

ヒルベルト空間 $H$ 上の有界線形汎関数 $f$ に対し、一意の $u \in H$ が存在して:

$$f(v) = \langle v, u\rangle\quad \forall v \in H$$

---

## 関連ページ

- [ベクトル](introduction.md)
- [行列（専門）](../matrices/professional.md)
- [三角関数（専門）](../../functions/trigonometric/professional.md)
