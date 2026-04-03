---
title: 直線
description: "2点を結んで伸ばした線"
difficulty: 1
tags: [math,geometry,line]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 幾何
    href: /math/geometry/index.html
  - text: 直線
    href: /math/geometry/line/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---





# 直線
$2$ 点を結んで両方向に無限に伸ばしたものが**直線**です。
$y = ax + b$ という一次方程式と一対一に対応します。

## このページで扱うこと
- 直線の方程式の書き方
- 傾き・切片の意味
- $2$ 直線の関係（平行・垂直・交点）

## 前提知識
- [点](../point/standard.md)
- [一次関数](../../functions/linear/standard.md)

---

## 直線の方程式

| 場面 | 式 |
|------|----|
| 傾き $a$、$y$ 切片 $b$ | $y = ax + b$ |
| 点 $(x_1,y_1)$ と傾き $a$ | $y - y_1 = a(x - x_1)$ |
| 縦の直線 | $x = k$ |

---

## 傾き

$2$ 点 $(x_1,y_1)$、$(x_2,y_2)$ を通る直線の傾き：

$$a = \frac{y_2 - y_1}{x_2 - x_1} = \frac{\text{縦の変化}}{\text{横の変化}}$$

---

## $2$ 直線の関係

$$\text{平行} \iff \text{傾きが等しい（}a_1 = a_2\text{）かつ切片が違う}$$
$$\text{垂直} \iff a_1 \times a_2 = -1$$

---

## 点と直線の距離

点 $(x_0, y_0)$ から直線 $ax + by + c = 0$ までの距離：

$$d = \frac{|ax_0 + by_0 + c|}{\sqrt{a^2 + b^2}}$$

---

## 関連ページ

- [点](../point/standard.md)
- [三角形](../triangle/standard.md)
- [直線（発展）](../line/advanced.md) — より詳しく学ぶ
