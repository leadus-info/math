---
title: 三角形
description: "3本の辺で囲まれた最もシンプルな図形"
difficulty: 1
tags: [math,geometry,triangle]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 幾何
    href: /math/geometry/index.html
  - text: 三角形
    href: /math/geometry/triangle/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---





# 三角形
$3$ 本の直線で囲まれた図形が**三角形**です。
すべての多角形はこれに分解できます。

## このページで扱うこと
- 内角の和
- 面積の求め方
- 正弦定理・余弦定理

## 前提知識
- [点](../point/standard.md)
- [三角関数](../../functions/trigonometric/standard.md)

---

## 内角の和は $180°$

どんな三角形でも $3$ つの角の和は $180°$ です。

$$\alpha + \beta + \gamma = 180°$$

これは「三角形の外角は、隣り合わない $2$ つの内角の和」とも言えます。

---

## 面積

$$S = \frac{1}{2} \times \text{底辺} \times \text{高さ}$$

$2$ 辺とその間の角がわかるとき：

$$S = \frac{1}{2} ab \sin C$$

$3$ 辺がわかるとき（**ヘロンの公式**）：

$$s = \frac{a+b+c}{2}, \quad S = \sqrt{s(s-a)(s-b)(s-c)}$$

---

## 正弦定理

外接円の半径を $R$ とすると：

$$\frac{a}{\sin A} = \frac{b}{\sin B} = \frac{c}{\sin C} = 2R$$

「辺の長さ ÷ 対角の $\sin$」はどの組み合わせでも一定です。

---

## 余弦定理

$$a^2 = b^2 + c^2 - 2bc\cos A$$

$A = 90°$ のとき $\cos 90° = 0$ → ピタゴラスの定理になります。

---

## 関連ページ

- [円](../circle/standard.md) — 外接円・内接円
- [三角関数](../../functions/trigonometric/standard.md)
- [三角形（発展）](../triangle/advanced.md) — より詳しく学ぶ
