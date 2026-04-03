---
title: 三角形（専門）
description: "重心座標・三角形の幾何学的定理・双曲幾何"
difficulty: 5
tags: [math,geometry,triangle,professional]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 幾何
    href: /math/geometry/index.html
  - text: 三角形（専門）
    href: /math/geometry/triangle/professional.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
    href: advanced.html
  - text: 専門
---







# 三角形（発展）
重心座標・メネラウスの定理・チェバの定理・双曲幾何を扱います。

## このページで扱うこと
- 重心座標系
- メネラウスの定理・チェバの定理
- 非ユークリッド幾何（双曲幾何の三角形）

## 前提知識
- [三角形](../triangle/standard.md)
- [ベクトル](../../linear-algebra/vectors/standard.md)

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

- [三角形](../triangle/standard.md)
- [直線（専門）](../line/professional.md)
- [点（専門）](../point/professional.md)
