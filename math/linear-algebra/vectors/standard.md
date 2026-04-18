---
title: ベクトル
description: "ベクトルの演算・内積・線形独立"
goal: "ベクトルの成分表示・内積の計算と幾何学的意味・線形独立の概念を理解し、基本的な計算ができるようになる"
tags: [math,linear-algebra,vectors]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 線形代数
    path: /math/linear-algebra/index.md
  - title: ベクトル
    path: /math/linear-algebra/vectors/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: ベクトル（入門）
    path: /math/linear-algebra/vectors/introduction.md
  - title: 点（標準）
    path: /math/geometry/point/standard.md
  - title: 乗法・べき乗（標準）
    path: /math/numbers/arithmetic/standard.md
---

## 成分表示

$n$ 次元ベクトルは実数を $n$ 個並べた組で表します。

$$\boldsymbol{a} = (a_1, a_2, \ldots, a_n) \in \mathbb{R}^n$$

**加法**：

$$\boldsymbol{a} + \boldsymbol{b} = (a_1+b_1, a_2+b_2, \ldots, a_n+b_n)$$

**スカラー倍**：

$$c\boldsymbol{a} = (ca_1, ca_2, \ldots, ca_n)$$

---

## ノルム（大きさ）

$$\|\boldsymbol{a}\| = \sqrt{a_1^2 + a_2^2 + \cdots + a_n^2}$$

**例**：$\boldsymbol{a} = (3, 4)$ のとき $\|\boldsymbol{a}\| = \sqrt{9+16} = 5$

大きさが1のベクトルを**単位ベクトル**といいます。$\hat{\boldsymbol{a}} = \frac{\boldsymbol{a}}{\|\boldsymbol{a}\|}$

---

## 内積

$$\boldsymbol{a} \cdot \boldsymbol{b} = a_1 b_1 + a_2 b_2 + \cdots + a_n b_n$$

**幾何学的意味**：

$$\boldsymbol{a} \cdot \boldsymbol{b} = \|\boldsymbol{a}\| \|\boldsymbol{b}\| \cos\theta$$

（$\theta$ は2ベクトルのなす角）

**直交条件**：$\boldsymbol{a} \cdot \boldsymbol{b} = 0 \iff \boldsymbol{a} \perp \boldsymbol{b}$

**例**：$\boldsymbol{a} = (1, 2)$、$\boldsymbol{b} = (3, -1)$ のとき $\boldsymbol{a} \cdot \boldsymbol{b} = 3 - 2 = 1$

---

## 線形独立

ベクトルの組 $\{\boldsymbol{v}_1, \ldots, \boldsymbol{v}_k\}$ が**線形独立**とは：

$$c_1\boldsymbol{v}_1 + \cdots + c_k\boldsymbol{v}_k = \boldsymbol{0} \implies c_1 = \cdots = c_k = 0$$

「どのベクトルも他のベクトルの組み合わせでは表せない」という意味です。

**例**：$(1, 0)$ と $(0, 1)$ は線形独立（$x$ 軸方向と $y$ 軸方向）。$(1, 2)$ と $(2, 4)$ は線形従属（$(2,4) = 2(1,2)$）。

$\mathbb{R}^n$ では、線形独立なベクトルは最大 $n$ 個です。

---

## 関連ページ

- [行列（標準）](../matrices/standard.md)
- [点（標準）](../../geometry/point/standard.md)
