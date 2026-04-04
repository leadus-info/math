---
title: 円
description: "中心から等距離な点の集合"
tags: [math,geometry,circle]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 幾何
    path: /math/geometry/index.html
  - title: 円
    path: /math/geometry/circle/standard.html
levels:
  - level: 入門
    path: introduction.html
  - level: 標準
  - level: 専門
    path: professional.html
level: 標準
requires:
  - title: 点
    path: /math/geometry/point/introduction
  - title: 直線
    path: /math/geometry/line/introduction
---

## 円の方程式

中心から等距離にある点の集合が円です。

中心 $(a, b)$、半径 $r$ の円は

$$(x - a)^2 + (y - b)^2 = r^2$$

これは「中心 $(a, b)$ からの距離が $r$ の点全体」という定義を式にしたものです。
原点中心のとき $x^2 + y^2 = r^2$。

---

## 円周と面積

$$\text{円周} = 2\pi r, \qquad \text{面積} = \pi r^2$$

$\pi = 3.14159\ldots$ は円周率で、無理数です。

---

## 弧長と扇形

中心角 $\theta$（ラジアン）のとき：

$$\text{弧長} = r\theta, \qquad \text{扇形の面積} = \frac{1}{2}r^2\theta$$

ラジアンとは「弧長 = 半径」となる角度。$360° = 2\pi$ ラジアン、$180° = \pi$ ラジアン。

---

## 円と直線の位置関係

中心 $(a, b)$、半径 $r$ の円と直線の距離を $d$ とすると：

| 条件 | 関係 |
|------|------|
| $d < r$ | 2点で交わる |
| $d = r$ | 1点で接する（接線） |
| $d > r$ | 交わらない |

---

## 接線の方程式

円 $x^2 + y^2 = r^2$ 上の点 $(x_0, y_0)$ での接線：

$$x_0 x + y_0 y = r^2$$

これは「接線は接点での半径と垂直」という事実から導けます。

---

## 単位円と三角関数

半径 1、中心が原点の円（**単位円**）上の点を角度 $\theta$ で表すと $(\cos\theta, \sin\theta)$。

$$\cos^2\theta + \sin^2\theta = 1$$

これは単位円の方程式 $x^2 + y^2 = 1$ そのものです。

---

## 関連ページ

- [三角関数](../../functions/trigonometric/introduction.md)
- [三角形](../triangle/introduction.md)
