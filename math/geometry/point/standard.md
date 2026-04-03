---
title: 点
description: "場所を表す最も基本的なもの"
difficulty: 1
tags: [math,geometry,point]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 幾何
    href: /math/geometry/index.html
  - text: 点
    href: /math/geometry/point/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 点
「場所」だけを持ち、大きさを持たないものが**点**です。
座標を使うと「右に $3$、上に $2$」という場所を $(3, 2)$ と数で表せます。

## このページで扱うこと
- 座標平面の仕組み
- $2$ 点間の距離
- 中点・内分点

## 前提知識
- [乗法・べき乗](../../numbers/arithmetic/standard.md) — 平方根の計算

---

## 座標平面

横の線が $x$ 軸、縦の線が $y$ 軸。
交わる点が**原点** $O = (0, 0)$ です。

点 $P$ の位置を $(x, y)$ で表します。
- $x$：原点から右向きの距離（左は負）
- $y$：原点から上向きの距離（下は負）

---

## $2$ 点間の距離

$A(1, 1)$ と $B(4, 5)$ の距離は？

右に $3$、上に $4$ 進むので、ピタゴラスの定理より

$$|AB| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5$$

一般に：

$$|AB| = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$

---

## 中点

$A(x_1, y_1)$ と $B(x_2, y_2)$ の真ん中の点：

$$M = \left(\frac{x_1 + x_2}{2},\ \frac{y_1 + y_2}{2}\right)$$

---

## 内分点

$A$ と $B$ を $m : n$ に分ける点：

$$P = \left(\frac{nx_1 + mx_2}{m+n},\ \frac{ny_1 + my_2}{m+n}\right)$$

---

## 関連ページ

- [直線](../line/standard.md)
- [ベクトル](../../linear-algebra/vectors/standard.md)
- [点（発展）](../point/advanced.md) — より詳しく学ぶ
