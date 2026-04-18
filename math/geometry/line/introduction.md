---
title: 直線
description: "2点を通る無限に伸びる図形"
goal: "直線の傾きの意味と直線の式の基本形を理解できるようになる"
tags: [math,geometry,line]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 直線
    path: /math/geometry/line/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 点（入門）
    path: /math/geometry/point/introduction.md
---

## 2点を決めると直線が決まる

2つの点を定めると、その2点を通る直線はただ1本に決まります。さらに両方向に限りなく伸ばしたものが**直線**です。

---

## 傾き——急さを数値で表す

坂道の「急さ」を数値で表す方法を考えましょう。「右に1進んだとき、どれだけ上がるか」を測ります。

- 右に1進んで上に2上がる → 傾き $2$（急な上り坂）
- 右に1進んでも上下しない → 傾き $0$（水平）
- 右に1進んで下に1下がる → 傾き $-1$（下り坂）

傾きが大きいほどグラフは急で、負なら右下がりです。

---

## 直線の式

傾き $2$ で $y$ 軸と点 $(0, 1)$ で交わる直線を式で書くと：

$$y = 2x + 1$$

$x = 0$ を入れると $y = 1$（$y$ 軸との交点）、$x = 1$ を入れると $y = 3$（もう1点）。この2点を結んで伸ばすとこの直線になります。

---

## 平行と垂直

傾きが同じ2直線は**平行**です（どこまで伸ばしても交わらない）。

垂直な2直線では、傾きの積が $-1$ になります。傾き $2$ の直線に垂直な直線の傾きは $-\frac{1}{2}$ です。

---

## まとめ

直線は「2点を通り、両方向に無限に伸びる」図形です。傾きと切片の2つで完全に決まり、平行・垂直の条件も傾きで判定できます。直線の方程式は幾何の問題を代数的に解く橋渡しになります。

---

## 関連ページ

- [点（入門）](../point/introduction.md)
- [一次関数（入門）](../../functions/linear/introduction.md)
- [三角形（入門）](../triangle/introduction.md)
