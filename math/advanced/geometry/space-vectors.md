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

$$\vec{a}-\vec{b} = (a_1-b_1,\ a_2-b_2,\ a_3-b_3)$$

$$k\vec{a} = (ka_1,\ ka_2,\ ka_3)$$

大きさは、三平方の定理を2回使う形で求まります。まず $xy$ 平面上で $a_1$、$a_2$ を直角をはさむ2辺とする直角三角形を考えると、その対角線（斜辺）の長さは $\sqrt{a_1^2+a_2^2}$ です。3本の軸は互いに垂直なので、$z$軸は$xy$平面上のどの直線とも垂直です。したがって、この対角線と $a_3$ を直角をはさむ2辺として、もう一度三平方の定理を使うと、

$$|\vec{a}| = \sqrt{\left(\sqrt{a_1^2+a_2^2}\right)^2+a_3^2} = \sqrt{a_1^2+a_2^2+a_3^2}$$

が得られます。

一般に、2点 $A(x_1,y_1,z_1)$、$B(x_2,y_2,z_2)$ の位置ベクトルの差からは $\overrightarrow{AB}=(x_2-x_1,\ y_2-y_1,\ z_2-z_1)$ が得られます。これに先ほど導いた大きさの公式を当てはめると、$|\overrightarrow{AB}|=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2+(z_2-z_1)^2}$ となり、これは2点間の距離の公式になります。

例えば、2点 $A(1,0,2)$、$B(3,4,1)$ に対して $\overrightarrow{AB}=(2,\ 4,\ -1)$ なので、$|\overrightarrow{AB}|=\sqrt{2^2+4^2+(-1)^2}=\sqrt{21}$ です。

---

## 空間ベクトルの内積

内積も平面と同じ考え方で定義されます。

$$\vec{a}\cdot\vec{b} = |\vec{a}||\vec{b}|\cos\theta = a_1b_1+a_2b_2+a_3b_3$$

この2つの式が一致することは、次のように確かめられます。$|\vec{a}-\vec{b}|^2$を余弦定理と成分計算の両方で展開し、比べればよいのです。余弦定理からは、$|\vec{a}-\vec{b}|^2=|\vec{a}|^2+|\vec{b}|^2-2|\vec{a}||\vec{b}|\cos\theta$ です。一方、成分計算からは、$|\vec{a}-\vec{b}|^2=(a_1-b_1)^2+(a_2-b_2)^2+(a_3-b_3)^2=|\vec{a}|^2+|\vec{b}|^2-2(a_1b_1+a_2b_2+a_3b_3)$ です。両者を比較すると、$|\vec{a}||\vec{b}|\cos\theta=a_1b_1+a_2b_2+a_3b_3$、つまり $\vec{a}\cdot\vec{b}=a_1b_1+a_2b_2+a_3b_3$ が導けます。

$\vec{a}\cdot\vec{b}=0$ が垂直を意味することも変わりません。

まず成分を使った具体例で、内積による垂直性の判定を確認してみましょう。$\vec{a}=(1,2,-1)$、$\vec{b}=(3,-1,1)$ とすると、大きさはそれぞれ $|\vec{a}|=\sqrt{1^2+2^2+(-1)^2}=\sqrt6$、$|\vec{b}|=\sqrt{3^2+(-1)^2+1^2}=\sqrt{11}$ です。内積は $\vec{a}\cdot\vec{b}=1\times3+2\times(-1)+(-1)\times1=3-2-1=0$ となるので、$\vec{a}\perp\vec{b}$ であることが分かります。

では次に、成分（座標）を使わずに、ベクトルの性質だけから同様の垂直性を示せることを見てみましょう。

**例題**：正四面体 $OABC$（すべての辺の長さが等しい四面体）で、辺 $OA$ と辺 $BC$ が垂直であることを示す。$\overrightarrow{OA}=\vec{a}$、$\overrightarrow{OB}=\vec{b}$、$\overrightarrow{OC}=\vec{c}$（$|\vec{a}|=|\vec{b}|=|\vec{c}|=1$）とします。

![正四面体OABCで辺OAと辺BCを太線で示し、この2辺が垂直であることを表す図](space-vectors/images/tetrahedron-perpendicular-edges.svg)

正四面体はどの面も正三角形なので、例えば三角形$OAB$は正三角形で$\angle AOB=60°$です。したがって $\vec{a}\cdot\vec{b}=|\vec{a}||\vec{b}|\cos60°=1\times1\times\dfrac12=\dfrac12$ となります。

正四面体の定義（すべての辺の長さが等しい）より、$OA=OC=AC$、$OB=OC=BC$も成り立つので、三角形$OAC$、三角形$OBC$も正三角形です。よって $\angle AOC=\angle BOC=60°$ となり、同じ理由で $\vec{a}\cdot\vec{c}=\vec{b}\cdot\vec{c}=\dfrac12$ が成り立ちます。

これを使うと、位置ベクトルの差の公式$\overrightarrow{PQ}=\vec{q}-\vec{p}$（2点$P$、$Q$の位置ベクトルがそれぞれ$\vec{p}$、$\vec{q}$のとき）より$\overrightarrow{BC}=\overrightarrow{OC}-\overrightarrow{OB}=\vec{c}-\vec{b}$なので、

$$\overrightarrow{OA}\cdot\overrightarrow{BC} = \vec{a}\cdot(\vec{c}-\vec{b}) = \vec{a}\cdot\vec{c}-\vec{a}\cdot\vec{b} = \frac12-\frac12=0$$

よって $OA \perp BC$ が示せます。座標を使わずに、正四面体の定義（辺の長さがすべて等しいこと）だけから直接この結論を導けるのがベクトルの強みです。$\square$

---

## まとめ

空間座標は、平面の座標を3本目の軸に拡張したものです。空間ベクトルの成分表示・演算・内積は、いずれも平面のベクトルの自然な拡張として理解でき、空間図形の垂直性などの性質を座標に頼らず証明する道具になります。

---

## 関連ページ

- [空間図形](../../intermediate/geometry/solids.md)
