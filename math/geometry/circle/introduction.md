---
title: 円
description: "1点から等距離にある点の集まり"
goal: "円の定義・円周・面積・円周率の意味を説明できるようになる"
tags: [math,geometry,circle]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 円
    path: /math/geometry/circle/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 点（入門）
    path: /math/geometry/point/introduction.md
---

## 円とは

「1点から等しい距離にある点を全部集めた」図形が**円**です。その1点が**中心**、等しい距離が**半径**です。

コンパスで描くとき、針を固定した点が中心、針と鉛筆の間の距離が半径——まさにこの定義通りです。

---

## 円周率 $\pi$

どんな大きさの円でも、「円周（外周の長さ）÷ 直径」は常に同じ値になります。これが**円周率** $\pi = 3.14159\ldots$ です。

$$\text{円周} = 2\pi r, \quad \text{面積} = \pi r^2$$

$\pi$ は割り切れない数（無理数）で、小数点以下は永遠に続きます。

---

## 接線

円の外から引いた「ちょうど1点だけで触れる直線」が**接線**です。接線は接点で半径と垂直になります。この性質は様々な計算に使われます。

---

## 単位円と角度

半径1の円（**単位円**）は特に重要です。単位円上の点の座標は $(\cos\theta, \sin\theta)$ と書けます（$\theta$ は角度）。

$$\cos^2\theta + \sin^2\theta = 1$$

これは単位円の方程式 $x^2 + y^2 = 1$ そのものです。

---

## まとめ

円は「中心から等距離にある点の集合」です。円周率 $\pi$ によって円周・面積が計算でき、接線は半径と垂直になります。単位円は三角関数の定義と直接結びついており、数学全体で重要な役割を果たします。

---

## 関連ページ

- [三角関数（入門）](../../functions/trigonometric/introduction.md)
- [三角形（入門）](../triangle/introduction.md)
