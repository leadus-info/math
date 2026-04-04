---
title: 円
description: "反転幾何・リーマン球面・複素平面上の円"
tags: [math,geometry,circle]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 幾何
    path: /math/geometry/index.html
  - title: 円
    path: /math/geometry/circle/professional.html
levels:
  - level: 入門
    path: introduction.html
  - level: 標準
    path: standard.html
  - level: 専門
level: 専門
requires:
  - title: 円
    path: /math/geometry/circle/introduction
  - title: 複素数
    path: /math/numbers/complex-numbers/introduction
  - title: 直線（専門）
    path: ../line/professional.md
---

## このページで扱うこと

反転幾何・リーマン球面・メビウス変換を扱います。

- 反転（円反転）とその性質
- リーマン球面（複素射影直線）
- メビウス変換による円の変換

---

## 反転

基準円 $|z| = r$ についての反転:

$$z \mapsto \frac{r^2}{\bar{z}}$$

円と直線を保存（円・直線族が不変）。共形写像の一種。

---

## リーマン球面

複素平面 $\mathbb{C}$ に無限遠点 $\infty$ を加えた $\hat{\mathbb{C}} = \mathbb{C} \cup \{\infty\}$。  
球面 $S^2$ と立体射影で同一視されます。

---

## メビウス変換

$$f(z) = \frac{az+b}{cz+d}\quad (ad-bc \neq 0)$$

$\hat{\mathbb{C}}$ 上の全単射共形写像。円・直線を円・直線に写します。

---

## 関連ページ

- [円](introduction.md)
- [複素関数](introduction.md)
- [点（専門）](../point/professional.md)
