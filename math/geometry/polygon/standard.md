---
title: 多角形
description: "n 辺で囲まれた図形の一般論"
tags: [math,geometry,polygon]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 多角形
    path: /math/geometry/polygon/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 三角形
    path: /math/geometry/triangle/introduction.md
  - title: 四角形
    path: /math/geometry/quadrilateral/introduction.md
  - title: 三角関数
    path: /math/functions/trigonometric/introduction.md
---

## 多角形の定義

$n$ 本の直線で囲まれた図形が **$n$ 角形**（多角形）です。

$n \geq 3$ であり、$n = 3$（三角形）、$n = 4$（四角形）が基本的な例です。

---

## 内角の和

**定理**：凸 $n$ 角形の内角の和は $(n-2) \times 180°$

**証明**：$n$ 角形を 1 つの頂点から対角線で引くと $(n-2)$ 個の三角形に分割されます。\
それぞれの三角形の内角の和が $180°$ なので、合計は $(n-2) \times 180°$。

| $n$ | 内角の和 |
|-----|---------|
| 3 | $180°$ |
| 4 | $360°$ |
| 5 | $540°$ |
| 6 | $720°$ |

---

## 外角の和

**定理**：任意の凸多角形の外角の和は $360°$

**証明**：各頂点で「内角 + 外角 $= 180°$」が成り立ちます。\
$n$ 個の頂点での合計は $180n°$。内角の和 $(n-2) \times 180°$ を引くと $360°$。

---

## 対角線の本数

$n$ 角形の対角線の本数：

$$\frac{n(n-3)}{2}$$

**導出**：$n$ 個の頂点から 2 点を選ぶ組み合わせ $\binom{n}{2}$ から、隣接する $n$ 辺を引きます。\
$\frac{n(n-1)}{2} - n = \frac{n(n-3)}{2}$

---

## 正多角形

すべての辺が等長で、すべての内角が等しい多角形が**正多角形**です。

**1つの内角の大きさ**：

$$\frac{(n-2) \times 180°}{n}$$

**外接円の半径 $R$ と面積**：

$$S = \frac{1}{2}nR^2\sin\frac{2\pi}{n}$$

$n \to \infty$ でこの式は $\pi R^2$（円の面積）に収束します——これは多角形が円に近づくことを反映しています。

---

## 関連ページ

- [三角形](../triangle/introduction.md)
- [四角形](../quadrilateral/introduction.md)
- [円](../circle/introduction.md)
