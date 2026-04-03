---
title: 多角形
description: "n 辺で囲まれた図形の一般論"
difficulty: 1
tags: [math,geometry,polygon]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 幾何
    href: /math/geometry/index.html
  - text: 多角形
    href: /math/geometry/polygon/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---




# 多角形
三角形・四角形・五角形……$n$ 本の辺で囲まれた図形を**多角形**といいます。
すべての辺と角が等しいものを**正多角形**といいます。

## このページで扱うこと
- 内角・外角の和
- 対角線の本数
- 正多角形の面積

## 前提知識
- [三角形](../triangle/standard.md)
- [四角形](../quadrilateral/standard.md)

---

## 内角の和

$n$ 角形の内角の和は $(n-2) \times 180°$ です。

| $n$ | 内角の和 |
|-----|---------|
| $3$（三角形） | $180°$ |
| $4$（四角形） | $360°$ |
| $5$（五角形） | $540°$ |
| $6$（六角形） | $720°$ |

**理由**：$n$ 角形は $n-2$ 個の三角形に分割できます。

---

## 外角の和

$n$ に関わらず、凸多角形の外角の和は常に $360°$ です。

---

## 対角線の本数

$$\frac{n(n-3)}{2}$$

$n$ 頂点から $2$ 点を選ぶ $\frac{n(n-1)}{2}$ 通りのうち、辺の $n$ 本を引いたものです。

---

## 正多角形の $1$ つの内角

$$\frac{(n-2) \times 180°}{n}$$

例：正六角形の $1$ 内角 $= \frac{4 \times 180°}{6} = 120°$

---

## 正多角形の面積

外接円の半径を $R$ とすると：

$$S = \frac{1}{2}nR^2\sin\frac{360°}{n}$$

$n$ を大きくすると、正多角形は円に近づき $S \to \pi R^2$（円の面積）。

---

## 関連ページ

- [円](../circle/standard.md)
- [多角形（発展）](../polygon/advanced.md) — より詳しく学ぶ
