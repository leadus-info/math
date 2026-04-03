---
title: 円
description: "中心から等距離にある点の集まり"
difficulty: 1
tags: [math,geometry,circle]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 幾何
    href: /math/geometry/index.html
  - text: 円
    href: /math/geometry/circle/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---





# 円
$1$ つの点（中心）から同じ距離にある点をすべて集めた図形が**円**です。
三角関数の定義にも使われます。

## このページで扱うこと
- 円の方程式
- 円周・面積・弧長
- 円と直線の関係

## 前提知識
- [点](../point/standard.md)
- [直線](../line/standard.md)

---

## 円の方程式

中心 $(a, b)$、半径 $r$ の円：

$$(x - a)^2 + (y - b)^2 = r^2$$

これは「中心からの距離が $r$」という距離の式 $\sqrt{(x-a)^2+(y-b)^2} = r$ を $2$ 乗したものです。

---

## 円周と面積

$$\text{円周} = 2\pi r, \qquad \text{面積} = \pi r^2$$

$\pi = 3.14159\ldots$（円周率）は無理数で、分数では表せません。

---

## 弧長と扇形の面積

中心角が $\theta$（ラジアン）のとき：

$$\text{弧長} = r\theta, \qquad \text{扇形の面積} = \frac{1}{2}r^2\theta$$

---

## 円と直線の位置関係

中心から直線までの距離 $d$ と半径 $r$ を比べます：

| $d$ と $r$ の関係 | 直線との関係 |
|------------------|-------------|
| $d < r$ | $2$ 点で交わる |
| $d = r$ | $1$ 点で接する（接線） |
| $d > r$ | 交わらない |

---

## 単位円

中心が原点、半径 $1$ の円を**単位円**といいます。
$x^2 + y^2 = 1$

この円の上の点が三角関数 $(\cos\theta, \sin\theta)$ の定義になっています。

---

## 関連ページ

- [三角関数](../../functions/trigonometric/standard.md)
- [三角形](../triangle/standard.md)
- [円（発展）](../circle/advanced.md) — より詳しく学ぶ
