---
title: ベクトル
description: "大きさと向きを持つ量"
tags: [math,linear-algebra,vectors]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 線形代数
    href: /math/linear-algebra/index.html
  - text: ベクトル
    href: /math/linear-algebra/vectors/standard.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
  - level: professional
    url: professional.html
level: standard
requires:
  - title: 点
    url: professional.md
  - title: 三角関数
    url: professional.md
---









# ベクトル
風の強さと向き、力の大きさと方向——「大きさ」と「向き」の両方を持つ量を**ベクトル**といいます。

## このページで扱うこと
- ベクトルの書き方と基本演算
- 大きさ（ノルム）と単位ベクトル
- 内積と角度・直交

---

## ベクトルとは

矢印で表します。長さが「大きさ」、矢の向きが「方向」です。

2 次元：$\boldsymbol{a} = (a_1, a_2)$

---

## 基本演算

**足し算**：成分ごとに足します。

$$\boldsymbol{a} + \boldsymbol{b} = (a_1 + b_1,\ a_2 + b_2)$$

**スカラー倍**：全成分に掛けます。

$$c\boldsymbol{a} = (ca_1,\ ca_2)$$

---

## 大きさ（ノルム）

$$\|\boldsymbol{a}\| = \sqrt{a_1^2 + a_2^2}$$

大きさが 1 の**単位ベクトル**：$\hat{\boldsymbol{a}} = \dfrac{\boldsymbol{a}}{\|\boldsymbol{a}\|}$

---

## 内積

$$\boldsymbol{a} \cdot \boldsymbol{b} = a_1 b_1 + a_2 b_2 = \|\boldsymbol{a}\|\|\boldsymbol{b}\|\cos\theta$$

$$\boldsymbol{a} \cdot \boldsymbol{b} = 0 \iff \text{直交（垂直）}$$

---

## 関連ページ

- [行列](professional.md)
- [点](professional.md)
- [ベクトル（専門）](professional.md)
