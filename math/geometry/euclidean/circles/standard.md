---
title: 円
description: "円の方程式・弧長・接線・単位円"
goal: "円の方程式を書き、円と直線の位置関係・接線の方程式を求め、単位円と三角関数の関係を説明できるようになる"
tags: [math,geometry,circle]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 円
    path: /math/geometry/euclidean/circles/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 円（入門）
    path: /math/geometry/euclidean/circles/introduction.md
  - title: 点（標準）
    path: /math/geometry/coordinate/point/standard.md
  - title: 三角関数（標準）
    path: /math/geometry/trigonometry/standard.md
---

## 円の方程式

中心 $(a, b)$、半径 $r$ の円は「中心からの距離が $r$ の点の集合」なので：

$$(x - a)^2 + (y - b)^2 = r^2$$

原点中心のとき $x^2 + y^2 = r^2$。

**例**：中心 $(1, -2)$、半径 $3$ の円：$(x-1)^2 + (y+2)^2 = 9$

---

## 弧長と扇形の面積

中心角 $\theta$（ラジアン）のとき：

$$\text{弧長} = r\theta, \quad \text{扇形の面積} = \frac{1}{2}r^2\theta$$

ラジアンは「弧長 $=$ 半径」となる角度（$360° = 2\pi$ ラジアン）。

---

## 円と直線の位置関係

中心から直線までの距離を $d$、半径を $r$ とすると：

| 条件 | 関係 |
|------|------|
| $d < r$ | 2点で交わる |
| $d = r$ | 1点で接する（接線） |
| $d > r$ | 交わらない |

---

## 接線の方程式

円 $x^2 + y^2 = r^2$ 上の点 $(x_0, y_0)$ での接線：

$$x_0 x + y_0 y = r^2$$

この公式は「接線は接点での半径と垂直」から導けます。接点でのベクトル $(x_0, y_0)$ と接線方向 $(x-x_0, y-y_0)$ の内積が $0$。

**例**：$x^2 + y^2 = 25$ 上の点 $(3, 4)$ での接線：$3x + 4y = 25$

---

## 単位円と三角関数

半径 $1$、中心が原点の円を**単位円**といいます。

角度 $\theta$ の点の座標を $(\cos\theta, \sin\theta)$ と定義すると、単位円の方程式 $x^2 + y^2 = 1$ から：

$$\cos^2\theta + \sin^2\theta = 1$$

が直ちに従います。これが三角関数の最重要公式の幾何学的な意味です。

---

## 関連ページ

- [三角関数（標準）](../../trigonometry/standard.md)
- [三角形（標準）](../triangles/standard.md)
