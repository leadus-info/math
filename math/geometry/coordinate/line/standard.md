---
title: 直線
description: "直線の方程式・平行・垂直・点と直線の距離"
goal: "直線の方程式を状況に応じた形で書き、平行・垂直条件と点と直線の距離公式を使えるようになる"
tags: [math,geometry,line]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 直線
    path: /math/geometry/coordinate/line/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 直線（入門）
    path: /math/geometry/coordinate/line/introduction.md
  - title: 点（標準）
    path: /math/geometry/coordinate/point/standard.md
---

## 直線の方程式の形

状況に応じた3つの書き方があります。

**傾き切片形式**（最も基本的）：

$$y = ax + b$$

**点傾き形式**（1点と傾きがわかるとき）：

$$y - y_1 = a(x - x_1)$$

**一般形**（垂直な直線も含めて統一的に書けます）：

$$Ax + By + C = 0$$

縦線（垂直線）は $x = k$ で表します。傾きは定義されません。

---

## 2点を通る直線

2点 $(x_1, y_1)$, $(x_2, y_2)$（$x_1 \neq x_2$）を通る直線：

傾き $a = \dfrac{y_2 - y_1}{x_2 - x_1}$ を求め、点傾き形式に代入します。

**例**：$(1, 3)$ と $(3, 7)$ を通る直線。$a = \frac{7-3}{3-1} = 2$。$y - 3 = 2(x-1)$ より $y = 2x + 1$。

---

## 平行・垂直の条件

直線 $l_1: y = a_1 x + b_1$、$l_2: y = a_2 x + b_2$ について：

$$l_1 \parallel l_2 \iff a_1 = a_2 \quad (b_1 \neq b_2)$$
$$l_1 \perp l_2 \iff a_1 a_2 = -1$$

垂直条件の理由：傾き $a_1$ の直線に対して垂直方向のベクトルは方向が $90°$ 回転します。

**例**：傾き $3$ の直線に垂直な直線の傾きは $-\frac{1}{3}$。

---

## 点と直線の距離

点 $(x_0, y_0)$ から直線 $ax + by + c = 0$ までの距離：

$$d = \frac{|ax_0 + by_0 + c|}{\sqrt{a^2 + b^2}}$$

**例題**：点 $(2, 3)$ から直線 $3x - 4y + 1 = 0$ までの距離：

$$d = \frac{|3 \cdot 2 - 4 \cdot 3 + 1|}{\sqrt{9+16}} = \frac{|6-12+1|}{5} = \frac{5}{5} = 1$$

---

## 関連ページ

- [点（標準）](../point/standard.md)
- [三角形（標準）](../../euclidean/triangles/standard.md)
- [直線（専門）](professional.md)
