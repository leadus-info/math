---
title: 三角形
description: "重心座標・メネラウス・チェバ・非ユークリッド幾何"
goal: "重心座標を使った点の表現・メネラウスとチェバの定理を証明し、双曲幾何での内角の和の違いを説明できるようになる"
tags: [math,geometry,triangle]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 三角形
    path: /math/geometry/euclidean/triangles/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 三角形（標準）
    path: /math/geometry/euclidean/triangles/standard.md
  - title: ベクトル（専門）
    path: /math/linear-algebra/vectors/professional.md
---

## 重心座標

$\triangle ABC$ の点 $P$ を $P = \alpha A + \beta B + \gamma C$（$\alpha + \beta + \gamma = 1$）と表す座標系を**重心座標**といいます。

- $P$ が $\triangle ABC$ の内部 $\iff$ $\alpha, \beta, \gamma > 0$
- 重心 $G$ は $(\frac{1}{3}, \frac{1}{3}, \frac{1}{3})$
- 頂点 $A$ は $(1, 0, 0)$

---

## メネラウスの定理

直線が $\triangle ABC$ の辺 $BC, CA, AB$（または延長）をそれぞれ $D, E, F$ で交わるとき（符号付き比で）：

$$\frac{BD}{DC} \cdot \frac{CE}{EA} \cdot \frac{AF}{FB} = -1$$

**証明**：$A$, $B$, $C$ から直線への垂線の長さの比を使うか、座標系で計算します。

---

## チェバの定理

$\triangle ABC$ の3頂点 $A, B, C$ からそれぞれ対辺（または延長）上の点 $D, E, F$ に向かう線分（チェビアン）が1点で交わる条件：

$$\frac{BD}{DC} \cdot \frac{CE}{EA} \cdot \frac{AF}{FB} = 1$$

**応用**：重心（$D, E, F$ が各辺の中点）、内心（$D, E, F$ が角の二等分線の足）はいずれもチェバの定理を満たします。

---

## 双曲幾何の三角形

双曲平面（曲率 $-1$）では、三角形の内角の和は $180°$ より小さくなります。

$$A + B + C = \pi - \text{面積}(T)$$

（面積の単位は適切にとった場合）

これはガウス・ボネの定理

$$\iint_T K\, dA = 2\pi - (A + B + C)$$

（$K$ はガウス曲率）の特殊ケースです。双曲平面では $K = -1$ 一定なので面積が大きいほど内角の和が小さくなります。

**参考文献**：Coxeter, H. S. M. (1998). *Non-Euclidean Geometry* (6th ed.). Mathematical Association of America.

---

## 関連ページ

- [三角形（標準）](standard.md)
- [直線（専門）](../../coordinate/line/professional.md)
