---
title: 三角形
description: "重心座標・三角形の幾何学的定理・双曲幾何"
tags: [math,geometry,triangle]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 幾何
    url: /math/geometry/index.html
  - title: 三角形
    url: /math/geometry/triangle/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: 三角形
    url: /math/geometry/triangle/introduction
  - title: ベクトル
    url: /math/linear-algebra/vectors/introduction
---


> この記事は [標準](standard.md) の続きです。先に標準を読むことを推奨します。

重心座標・メネラウスの定理・チェバの定理・双曲幾何を扱います。

## このページで扱うこと
- 重心座標系
- メネラウスの定理・チェバの定理
- 非ユークリッド幾何（双曲幾何の三角形）

---

## 重心座標

点 $P$ を $P = \alpha A + \beta B + \gamma C$（$\alpha+\beta+\gamma=1$）と表す座標系。

点が三角形の内部にある $\iff$ $\alpha, \beta, \gamma > 0$

---

## メネラウスの定理

直線が三角形 $ABC$ の辺（または延長）を切るとき:

$$\frac{BD}{DC}\cdot\frac{CE}{EA}\cdot\frac{AF}{FB} = -1 \quad \text{（符号付き比）}$$

---

## チェバの定理

三角形の頂点からの cevian が1点で交わる条件:

$$\frac{BD}{DC}\cdot\frac{CE}{EA}\cdot\frac{AF}{FB} = 1$$

---

## 双曲幾何の三角形

双曲平面では内角の和 $< 180°$。面積は角欠損に比例:

$$S = K(\pi - \alpha - \beta - \gamma)\quad (K>0)$$

---

## 関連ページ

- [三角形](introduction.md)
- [直線（専門）](../line/professional.md)
- [点（専門）](../point/professional.md)
