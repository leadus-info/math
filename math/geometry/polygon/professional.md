---
title: 多角形
description: "多面体・オイラー標数・タイリング理論"
tags: [math,geometry,polygon]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 多角形
    path: /math/geometry/polygon/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 多角形
    path: /math/geometry/polygon/introduction.md
  - title: 集合
    path: /math/math-language/sets/introduction.md
---

## オイラーの多面体定理

三次元の多面体を平面に投影して得られる連結平面グラフについて：

$$V - E + F = 2$$

$V$：頂点数、$E$：辺数、$F$：面数（外側の無限面を含む）

これは**オイラー標数**と呼ばれる位相的不変量です。\
球面 $S^2$ と同相な多面体ではすべて $V - E + F = 2$ が成り立ちます。

**例**：立方体 $V = 8$、$E = 12$、$F = 6$ → $8 - 12 + 6 = 2$ ✓

---

## 正多面体が5種類しかない証明

各頂点に集まる面の数を $k$、各面が $n$ 角形とすると：\
$nF = 2E$（各辺は2面に共有）、$kV = 2E$（各辺は2頂点に共有）。

オイラーの式に代入：

$$\frac{2E}{k} - E + \frac{2E}{n} = 2 \implies \frac{1}{k} + \frac{1}{n} = \frac{1}{2} + \frac{1}{E} > \frac{1}{2}$$

$k \geq 3$、$n \geq 3$ の整数解は $(k, n) \in \{(3,3),(3,4),(4,3),(3,5),(5,3)\}$ の5通りのみ。

| $(k, n)$ | 多面体 |
|----------|--------|
| $(3, 3)$ | 正四面体 |
| $(3, 4)$ | 立方体 |
| $(4, 3)$ | 正八面体 |
| $(3, 5)$ | 正十二面体 |
| $(5, 3)$ | 正二十面体 |

---

## 曲面のオイラー標数

多面体定理をより一般の曲面に拡張できます。

| 曲面 | $\chi = V - E + F$ |
|------|--------------------|
| 球面 $S^2$ | $2$ |
| トーラス $T^2$ | $0$ |
| 種数 $g$ の曲面 | $2 - 2g$ |

種数（穴の数）$g$ はトポロジー的不変量です。

**参考文献**：Cromwell, P. R. (1997). *Polyhedra*. Cambridge University Press.

---

## 関連ページ

- [多角形](standard.md)
- [点（専門）](../point/professional.md)
