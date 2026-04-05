---
title: 直線
description: "直線の方程式と位置関係"
tags: [math,geometry,line]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 直線
    path: /math/geometry/line/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 点
    path: /math/geometry/point/introduction.md
  - title: 一次関数
    path: /math/functions/linear/introduction.md
---

## 直線の方程式

2点を通る直線はただ一本に決まります。\
その直線を代数的に表したものが**直線の方程式**です。

**傾き切片形式**（最も基本的な形）：

$$y = ax + b$$

- $a$：**傾き**（$x$ が 1 増えると $y$ が $a$ 増える）
- $b$：**$y$ 切片**（$x = 0$ のときの $y$ の値）

**点傾き形式**（点と傾きから直線を書く）：

$$y - y_1 = a(x - x_1)$$

点 $(x_1, y_1)$ を通り、傾き $a$ の直線。

**2点から傾きを求める**：

$$a = \frac{y_2 - y_1}{x_2 - x_1}$$

ただし $x_1 = x_2$（垂直線）のとき傾きは定義されず、$x = k$ と表します。

**例題**：点 $(1, 3)$ と $(3, 7)$ を通る直線の方程式を求めます。\
傾き $= \frac{7-3}{3-1} = 2$\
$y - 3 = 2(x - 1)$ より $y = 2x + 1$。

---

## 平行・垂直の条件

**平行**：2直線 $y = a_1 x + b_1$ と $y = a_2 x + b_2$ が平行\
$\iff a_1 = a_2$（かつ $b_1 \neq b_2$）

傾きが同じ直線は交わらず、常に等距離を保ちます。

**垂直**：2直線が垂直\
$\iff a_1 \times a_2 = -1$

**なぜ積が $-1$ になるのか？**\
傾き $a$ の直線に垂直な方向に進むと、右に 1 進むたびに $-\frac{1}{a}$ 下がります。\
これが垂直な直線の傾きです。

**例**：傾き $3$ の直線に垂直な直線の傾きは $-\frac{1}{3}$。

---

## 点と直線の距離

点 $(x_0, y_0)$ から直線 $ax + by + c = 0$ までの（垂直）距離：

$$d = \frac{|ax_0 + by_0 + c|}{\sqrt{a^2 + b^2}}$$

**導出の考え方**：点から直線に垂線を下ろし、その長さをベクトルの射影で計算します。

**例題**：点 $(2, 3)$ から直線 $3x - 4y + 1 = 0$ までの距離：

$$d = \frac{|3 \cdot 2 - 4 \cdot 3 + 1|}{\sqrt{9 + 16}} = \frac{|6 - 12 + 1|}{5} = \frac{5}{5} = 1$$

---

## 関連ページ

- [点](../point/introduction.md)
- [三角形](../triangle/introduction.md)
