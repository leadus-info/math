---
title: ベクトル
description: "大きさと向きを持つ量"
difficulty: 2
tags: [math,linear-algebra,vectors]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 線形代数
    href: /math/linear-algebra/index.html
  - text: ベクトル
    href: /math/linear-algebra/vectors/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---





# ベクトル
「北へ $5$ km」のように、**大きさ**と**向き**の両方を持つ量が**ベクトル**です。
温度や重さのような「大きさだけの量（スカラー）」とは違います。

## このページで扱うこと
- ベクトルの書き方と図示
- 足し算・スカラー倍
- 内積と角度

## 前提知識
- [点](../../geometry/point/standard.md)
- [三角関数](../../functions/trigonometric/standard.md)

---

## ベクトルとは？

矢印で表します。

- 矢印の**長さ**：大きさ（速さ、距離など）
- 矢印の**向き**：方向

$2$ 次元のベクトル $\boldsymbol{a} = (3, 4)$：
「右に $3$、上に $4$」という移動を表します。

---

## 足し算

$$\boldsymbol{a} + \boldsymbol{b} = (a_1 + b_1,\ a_2 + b_2)$$

矢印を頭から尻につなぐイメージです。

---

## スカラー倍

$$2\boldsymbol{a} = (2a_1,\ 2a_2)$$

同じ向きで $2$ 倍の長さになります。
$-1$ 倍にすると逆向きになります。

---

## 大きさ（ノルム）

$$\|\boldsymbol{a}\| = \sqrt{a_1^2 + a_2^2}$$

**例**：$\boldsymbol{a} = (3, 4)$ なら $\|\boldsymbol{a}\| = \sqrt{9+16} = 5$

---

## 内積

$$\boldsymbol{a} \cdot \boldsymbol{b} = a_1 b_1 + a_2 b_2 = \|\boldsymbol{a}\|\|\boldsymbol{b}\|\cos\theta$$

$\theta$ は $2$ つのベクトルのなす角です。

- **垂直**（$\theta = 90°$）なら $\cos 90° = 0$ → 内積 $= 0$
- **同じ向き**（$\theta = 0°$）なら 内積が最大

---

## 関連ページ

- [行列](../matrices/standard.md)
- [点](../../geometry/point/standard.md)
- [ベクトル（発展）](../vectors/advanced.md) — より詳しく学ぶ
