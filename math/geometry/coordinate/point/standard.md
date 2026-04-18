---
title: 点
description: "座標・距離公式・内分点"
goal: "2点間の距離公式・中点・内分点の公式を導出し、座標平面上の図形問題に応用できるようになる"
tags: [math,geometry,point]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 点
    path: /math/geometry/coordinate/point/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 点（入門）
    path: /math/geometry/coordinate/point/introduction.md
  - title: 負数（標準）
    path: /math/numbers/integers/standard.md
  - title: 乗法・べき乗（標準）
    path: /math/numbers/arithmetic/standard.md
---

## 座標平面

縦軸（$y$ 軸）と横軸（$x$ 軸）が交わる点を**原点** $O(0, 0)$ とし、点の位置を $(x, y)$ で表します。

$x$ 軸は右が正、$y$ 軸は上が正。4つの領域を**象限**といいます（右上が第1象限、反時計回りに第2, 3, 4象限）。

---

## 2点間の距離

点 $A(x_1, y_1)$ と $B(x_2, y_2)$ の距離は、三平方の定理から：

$$|AB| = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$

**導出**：$A$ から $B$ へ「横 $|x_2 - x_1|$、縦 $|y_2 - y_1|$」進む直角三角形の斜辺が $|AB|$ です。

**例**：$A(1, 2)$, $B(4, 6)$ の距離 $= \sqrt{(4-1)^2+(6-2)^2} = \sqrt{9+16} = 5$

---

## 中点

線分 $AB$ の中点 $M$ の座標：

$$M = \left(\frac{x_1+x_2}{2}, \frac{y_1+y_2}{2}\right)$$

---

## 内分点・外分点

線分 $AB$ を $m : n$ に**内分**する点 $P$（$A$ と $B$ の間に位置）：

$$P = \left(\frac{nx_1+mx_2}{m+n}, \frac{ny_1+my_2}{m+n}\right)$$

**例**：$A(0,0)$, $B(6,9)$ を $2:1$ に内分する点：$\left(\frac{1\cdot0+2\cdot6}{3}, \frac{1\cdot0+2\cdot9}{3}\right) = (4, 6)$

中点は $m=n=1$ の特別な場合です。

---

## 三角形の重心

3頂点 $A(x_1,y_1)$, $B(x_2,y_2)$, $C(x_3,y_3)$ の重心 $G$：

$$G = \left(\frac{x_1+x_2+x_3}{3}, \frac{y_1+y_2+y_3}{3}\right)$$

**例題**：$A(1,2)$, $B(5,4)$, $C(3,9)$ の重心は $\left(\frac{9}{3}, \frac{15}{3}\right) = (3, 5)$。

---

## 関連ページ

- [直線（標準）](../line/standard.md)
- [ベクトル（標準）](../../../linear-algebra/vectors/standard.md)
