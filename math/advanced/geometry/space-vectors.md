---
title: 空間座標とベクトル
description: "空間内の点をx,y,z座標で表す方法と、空間ベクトルの成分表示・和差・実数倍の演算、内積の定義と垂直性の判定、正四面体の辺の垂直性を示す応用を平面ベクトルの拡張として扱う"
goal: "空間座標の意味を理解し、空間ベクトルの成分・内積を平面からの拡張として使えるようになる"
tags: [math, geometry, vectors]
stage: advanced
subject: 幾何
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 応用編
    path: ../index.md
  - title: 空間座標とベクトル
    path: space-vectors.md
requires:
  - title: ベクトル
    path: vectors.md
---

## 空間座標

平面上の点の位置を2本の数直線（$x$軸、$y$軸）で表したように、空間内の点の位置は、原点で互いに垂直な3本の数直線（$x$軸、$y$軸、$z$軸）を使って、3つの数の組 $(x,y,z)$ で表せます。

---

## 空間ベクトルの成分と演算

空間ベクトルも、平面のベクトルと同じように成分で表せます。

$$\vec{a} = (a_1, a_2, a_3)$$

和・差・実数倍は、成分ごとに計算する点も平面のときと同じです。

$$\vec{a}+\vec{b} = (a_1+b_1,\ a_2+b_2,\ a_3+b_3)$$

大きさは、三平方の定理を2回使う形で求まります。

$$|\vec{a}| = \sqrt{a_1^2+a_2^2+a_3^2}$$

---

## 空間ベクトルの内積

内積も平面と同じ考え方で定義されます。

$$\vec{a}\cdot\vec{b} = |\vec{a}||\vec{b}|\cos\theta = a_1b_1+a_2b_2+a_3b_3$$

$\vec{a}\cdot\vec{b}=0$ が垂直を意味することも変わりません。

**例題**：正四面体 $OABC$（すべての辺の長さが等しい四面体）で、辺 $OA$ と辺 $BC$ が垂直であることを示す。$\overrightarrow{OA}=\vec{a}$、$\overrightarrow{OB}=\vec{b}$、$\overrightarrow{OC}=\vec{c}$（$|\vec{a}|=|\vec{b}|=|\vec{c}|=1$）とします。正四面体はどの面も正三角形なので、例えば三角形$OAB$は正三角形で$\angle AOB=60°$。したがって $\vec{a}\cdot\vec{b}=|\vec{a}||\vec{b}|\cos60°=1\times1\times\dfrac12=\dfrac12$ となり、同じ理由で$\vec{a}$、$\vec{b}$、$\vec{c}$のどの2つの内積も$\dfrac12$になります。これを使うと、

$$\overrightarrow{OA}\cdot\overrightarrow{BC} = \vec{a}\cdot(\vec{c}-\vec{b}) = \vec{a}\cdot\vec{c}-\vec{a}\cdot\vec{b} = \frac12-\frac12=0$$

よって $OA \perp BC$ が示せます。座標を使わずに、正四面体の対称性から直接この結論を導けるのがベクトルの強みです。

![正四面体OABCで辺OAと辺BCを太線で示し、この2辺が垂直であることを表す図](space-vectors/images/tetrahedron-perpendicular-edges.svg)

---

## まとめ

空間座標は、平面の座標を3本目の軸に拡張したものです。空間ベクトルの成分表示・演算・内積は、いずれも平面のベクトルの自然な拡張として理解でき、空間図形の垂直性などの性質を座標に頼らず証明する道具になります。

---

## 関連ページ

- [空間図形](../../intermediate/geometry/solids.md)
