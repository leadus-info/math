---
title: 点
description: "位置だけを持つ幾何の基本要素"
goal: "座標の意味と2点間の距離・中点を直感的に理解できるようになる"
tags: [math,geometry,point]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 点
    path: /math/geometry/point/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 自然数（入門）
    path: /math/numbers/natural-numbers/introduction.md
---

## 「場所」だけを持つもの

鉛筆で紙に打った小さな点。数学ではこれをさらに理想化して、「大きさが全くなく、場所だけがある」ものを**点**と呼びます。

---

## 座標——数で場所を表す

「校舎から北に50m、東に30m」のように、出発点と方向と距離で場所を表せます。数学では2本の数直線を使います。

横の数直線（$x$ 軸）と縦の数直線（$y$ 軸）を直角に交差させ、交点を原点 $O$ とします。すると、平面上のどんな点も $(x, y)$ という数のペアで表せます。

- $(3, 4)$：右に3、上に4
- $(-2, 0)$：左に2、上下は0

これが**座標**のアイデアです。

---

## 2点の距離

$(0, 0)$ と $(3, 4)$ の距離はいくらでしょう？

右に3、上に4進む直角三角形を考えます。斜辺が2点間の距離で、三平方の定理より：

$$\sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5$$

---

## 中点

$(0, 0)$ と $(4, 6)$ のちょうど真ん中の点は？ 横座標の平均、縦座標の平均をとれば求まります。

$$\left(\frac{0+4}{2},\ \frac{0+6}{2}\right) = (2, 3)$$

---

## まとめ

点は「場所だけを持ち、大きさを持たない」数学の基本単位です。座標を使うことで、幾何学の問題を数の計算で解くことができます。2点間の距離は三平方の定理、中点は座標の平均で求められます。

---

## 関連ページ

- [直線（入門）](../line/introduction.md)
- [ベクトル（入門）](../../linear-algebra/vectors/introduction.md)
