---
title: 多角形
description: "内角・外角・対角線・正多角形の面積"
goal: "n角形の内角の和・外角の和・対角線の本数を公式で求め、正多角形の面積を計算できるようになる"
tags: [math,geometry,polygon]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 多角形
    path: /math/geometry/euclidean/polygons/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 多角形（入門）
    path: /math/geometry/euclidean/polygons/introduction.md
  - title: 三角関数（標準）
    path: /math/geometry/trigonometry/standard.md
---

## 内角の和

$n$ 角形の内角の和：$(n-2) \times 180°$

**導出**：1頂点から対角線を引くと $(n-2)$ 個の三角形に分割されます。

| $n$ | 内角の和 | 1つの内角（正多角形） |
|-----|---------|---------------------|
| 3 | $180°$ | $60°$ |
| 4 | $360°$ | $90°$ |
| 5 | $540°$ | $108°$ |
| 6 | $720°$ | $120°$ |
| $n$ | $(n-2) \times 180°$ | $\frac{(n-2) \times 180°}{n}$ |

---

## 外角の和

**定理**：凸多角形の外角の和は $360°$（$n$ に依らず一定）

**証明**：各頂点で「内角 + 外角 $= 180°$」が成り立ちます。$n$ 頂点での合計 $180n°$ から内角の和 $(n-2) \times 180° = 180n° - 360°$ を引くと $360°$。$\square$

---

## 対角線の本数

$n$ 角形の対角線の本数：

$$\frac{n(n-3)}{2}$$

**導出**：$n$ 頂点から2点を選ぶ $\binom{n}{2} = \frac{n(n-1)}{2}$ 通りから、隣接する辺 $n$ 本を引くと $\frac{n(n-1)}{2} - n = \frac{n(n-3)}{2}$。

---

## 正多角形の面積

外接円の半径 $R$、辺の数 $n$ の正多角形の面積：

$$S = \frac{1}{2} n R^2 \sin\frac{2\pi}{n}$$

$n \to \infty$ で $S \to \pi R^2$（円の面積）に収束します。

**例**：正六角形（$n=6$、$R=2$）：$S = \frac{1}{2} \times 6 \times 4 \times \sin 60° = 12 \times \frac{\sqrt{3}}{2} = 6\sqrt{3}$

---

## 関連ページ

- [円（標準）](../circles/standard.md)
- [三角関数（標準）](../../trigonometry/standard.md)
