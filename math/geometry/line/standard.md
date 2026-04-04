---
title: 直線
description: "直線の方程式と位置関係"
tags: [math,geometry,line]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 幾何
    url: /math/geometry/index.html
  - title: 直線
    url: /math/geometry/line/standard.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
  - level: professional
    url: professional.html
level: standard
requires:
  - title: 点
    url: /math/geometry/point/introduction
  - title: 一次関数
    url: /math/functions/linear/introduction
---


> この記事は [入門](introduction.md) の続きです。先に入門を読むことを推奨します。

2 点を結んで両方向に無限に延ばしたものが**直線**です。

## このページで扱うこと
- 直線の方程式の書き方
- 平行・垂直の条件
- 点と直線の距離

---

## 直線の方程式

| 場面 | 式 |
|------|----|
| 傾き $a$、$y$ 切片 $b$ | $y = ax + b$ |
| 点 $(x_1, y_1)$ と傾き $a$ | $y - y_1 = a(x - x_1)$ |
| 縦線 | $x = k$ |

---

## 傾き

$$a = \frac{y_2 - y_1}{x_2 - x_1}$$

---

## 平行・垂直の条件

$$\text{平行} \iff a_1 = a_2 \quad (\text{切片は異なる})$$
$$\text{垂直} \iff a_1 \times a_2 = -1$$

---

## 点と直線の距離

点 $(x_0, y_0)$ から直線 $ax + by + c = 0$ までの距離：

$$d = \frac{|ax_0 + by_0 + c|}{\sqrt{a^2 + b^2}}$$

---

## 関連ページ

- [点](professional.md)
- [三角形](professional.md)
- [直線（専門）](professional.md)
