---
title: 多角形
description: "多面体のオイラー公式・正多面体・位相的不変量"
goal: "オイラーの多面体定理を証明し、正多面体が5種類しかない理由とオイラー標数の位相的意味を説明できるようになる"
tags: [math,geometry,polygon]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 多角形
    path: /math/geometry/euclidean/polygons/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 多角形（標準）
    path: /math/geometry/euclidean/polygons/standard.md
  - title: 集合（専門）
    path: /math/foundations/sets/professional.md
---

## オイラーの多面体定理

凸多面体（または球面と同相な多面体）について：

$$V - E + F = 2$$

（$V$：頂点数、$E$：辺数、$F$：面数）

**例**：立方体 $V=8$, $E=12$, $F=6$ → $8-12+6=2$ ✓

この $\chi = V - E + F$ を**オイラー標数**といいます。球面 $S^2$ と同相な多面体ではすべて $\chi = 2$。

**証明の概略**：多面体を平面グラフに投影し、三角形分割してからオイラーの公式（平面連結グラフ：$V-E+F=2$）を利用します。

---

## 正多面体が5種類しかない証明

各面が $n$ 角形、各頂点に $k$ 面が集まるとすると：

$$nF = 2E, \quad kV = 2E$$

（各辺は2面・2頂点に共有）。オイラーの公式を使うと：

$$\frac{2E}{k} - E + \frac{2E}{n} = 2 \implies \frac{1}{k} + \frac{1}{n} = \frac{1}{2} + \frac{1}{E} > \frac{1}{2}$$

$k \geq 3$、$n \geq 3$ の整数解：

| $(k, n)$ | 多面体 | $V, E, F$ |
|----------|--------|-----------|
| $(3,3)$ | 正四面体 | $4,6,4$ |
| $(3,4)$ | 立方体 | $8,12,6$ |
| $(4,3)$ | 正八面体 | $6,12,8$ |
| $(3,5)$ | 正十二面体 | $20,30,12$ |
| $(5,3)$ | 正二十面体 | $12,30,20$ |

---

## オイラー標数の位相的意味

一般の閉曲面では種数 $g$（穴の数）に応じて：

$$\chi = 2 - 2g$$

球面（$g=0$）: $\chi=2$、トーラス（$g=1$）: $\chi=0$、二重トーラス: $\chi=-2$

オイラー標数は曲面を連続的に変形しても変わらない位相不変量です（ガウス＝ボネの定理：$\iint_M K \, dA = 2\pi \chi$）。

**参考文献**：Cromwell, P. R. (1997). *Polyhedra*. Cambridge University Press.

---

## 関連ページ

- [多角形（標準）](standard.md)
- [点（専門）](../../coordinate/point/professional.md)
