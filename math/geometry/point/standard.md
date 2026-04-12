---
title: 点
description: "位置を表す最も基本的な要素"
tags: [math,geometry,point]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 点
    path: /math/geometry/point/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 四則演算
    path: professional.md
  - title: 負数
    path: /math/numbers/negative-numbers/introduction.md
---

## 座標平面

縦軸（$y$ 軸）と横軸（$x$ 軸）が原点 $O(0, 0)$ で交わる平面が**座標平面**です。\
点の位置を $(x, y)$ という数のペアで表します。

各軸の向き：$x$ 軸は右が正、$y$ 軸は上が正。

---

## 2点間の距離

点 $A(x_1, y_1)$ と $B(x_2, y_2)$ の距離は、三平方の定理から求まります。

$$|AB| = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$

**導出**：$A$ から $x$ 軸方向に $|x_2 - x_1|$、$y$ 軸方向に $|y_2 - y_1|$ 進んで $B$ に至る直角三角形を考えます。\
斜辺の長さが $|AB|$ です。

**例**：$A(1, 2)$、$B(4, 6)$ の距離 $= \sqrt{9 + 16} = 5$

---

## 中点と内分点

**中点**：線分 $AB$ の真ん中の点

$$M = \left(\frac{x_1 + x_2}{2},\ \frac{y_1 + y_2}{2}\right)$$

**内分点**：線分 $AB$ を $m : n$ に内分する点（内側の点）

$$P = \left(\frac{nx_1 + mx_2}{m + n},\ \frac{ny_1 + my_2}{m + n}\right)$$

中点は $m = n = 1$ の特別な場合です。

**例**：$A(0, 0)$、$B(6, 9)$ を $2 : 1$ に内分する点：

$$P = \left(\frac{1 \cdot 0 + 2 \cdot 6}{3},\ \frac{1 \cdot 0 + 2 \cdot 9}{3}\right) = (4, 6)$$

---

## 座標と図形

座標を使うことで、図形の性質を計算で確認できます。

**例**：三角形の重心\
3頂点 $A(x_1, y_1)$、$B(x_2, y_2)$、$C(x_3, y_3)$ の重心：

$$G = \left(\frac{x_1+x_2+x_3}{3},\ \frac{y_1+y_2+y_3}{3}\right)$$

これは3本の中線の交点に一致します。

---

## 関連ページ

- [直線](../line/introduction.md)
- [ベクトル](../../linear-algebra/vectors/introduction.md)
