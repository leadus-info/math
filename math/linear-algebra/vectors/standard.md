---
title: ベクトル
description: "大きさと向きを持つ量"
tags: [math,linear-algebra,vectors]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 線形代数
    path: /math/linear-algebra/index.html
  - title: ベクトル
    path: /math/linear-algebra/vectors/standard.html
levels:
  - level: 入門
    path: introduction.html
  - level: 標準
  - level: 専門
    path: professional.html
level: 標準
requires:
  - title: 点
    path: /math/geometry/point/introduction.html
  - title: 三角関数
    path: /math/functions/trigonometric/introduction.html
---


## ベクトルの定義

大きさと向きの両方を持つ量がベクトルです。

$n$ 次元のベクトルは実数を $n$ 個並べた組で表します。

$$\boldsymbol{a} = (a_1, a_2, \ldots, a_n) \in \mathbb{R}^n$$

2次元の例：$\boldsymbol{a} = (3, 4)$（右に3、上に4という移動を表す）

---

## 基本演算

**足し算**：成分ごとに足します。

$$\boldsymbol{a} + \boldsymbol{b} = (a_1 + b_1,\ a_2 + b_2)$$

**スカラー倍**：すべての成分に定数を掛けます。

$$c\boldsymbol{a} = (ca_1,\ ca_2)$$

$c > 1$ なら同じ向きで長さが伸び、$c < 0$ なら向きが逆になります。

---

## 大きさ（ノルム）

ベクトルの「長さ」を大きさまたは**ノルム**といいます。

$$\|\boldsymbol{a}\| = \sqrt{a_1^2 + a_2^2 + \cdots + a_n^2}$$

例：$\boldsymbol{a} = (3, 4)$ のとき $\|\boldsymbol{a}\| = \sqrt{9 + 16} = 5$

大きさが 1 のベクトルを**単位ベクトル**といい、$\hat{\boldsymbol{a}} = \dfrac{\boldsymbol{a}}{\|\boldsymbol{a}\|}$ で作れます。

---

## 内積

2つのベクトルの「方向の一致具合」を表す量が**内積**です。

$$\boldsymbol{a} \cdot \boldsymbol{b} = a_1 b_1 + a_2 b_2 + \cdots + a_n b_n$$

幾何学的には

$$\boldsymbol{a} \cdot \boldsymbol{b} = \|\boldsymbol{a}\|\|\boldsymbol{b}\|\cos\theta$$

（$\theta$ は2つのベクトルのなす角）。

**直交条件**：$\boldsymbol{a} \cdot \boldsymbol{b} = 0 \Leftrightarrow \boldsymbol{a} \perp \boldsymbol{b}$

例：$(1, 0) \cdot (0, 1) = 0$（$x$ 軸方向と $y$ 軸方向は直交）

---

## 線形独立

ベクトルの組 $\{\boldsymbol{v}_1, \ldots, \boldsymbol{v}_k\}$ が**線形独立**とは、

$$c_1\boldsymbol{v}_1 + c_2\boldsymbol{v}_2 + \cdots + c_k\boldsymbol{v}_k = \boldsymbol{0} \implies c_1 = c_2 = \cdots = c_k = 0$$

が成り立つことです。「どのベクトルも、他のベクトルの組み合わせでは表せない」という意味です。

---

## 関連ページ

- [行列](../matrices/introduction.md) — ベクトルを変換する操作
- [点](../../geometry/point/introduction.md) — 座標とベクトルの関係
