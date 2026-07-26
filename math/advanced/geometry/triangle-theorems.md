---
title: 三角形の性質の応用
description: "三角形の角の二等分線が対辺を辺の比に内分する性質と、3本の線が1点で交わる条件を表すチェバの定理、1直線が3辺を横切る条件を表すメネラウスの定理、それぞれの逆を扱う"
goal: "角の二等分線と辺の比の関係を理解し、チェバの定理・メネラウスの定理を導出・説明し、使えるようになる"
tags: [math, geometry, triangle]
stage: advanced
subject: 幾何
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 応用編
    path: ../index.md
  - title: 三角形の性質の応用
    path: triangle-theorems.md
requires:
  - title: 三角形
    path: triangles.md
  - title: 相似
    path: ../../intermediate/geometry/similarity.md
---

## 角の二等分線と辺の比

三角形 $ABC$ の頂角 $A$ の二等分線が、対辺 $BC$ と交わる点を $D$ とすると、次の関係が成り立ちます。

$$BD:DC = AB:AC$$

**証明の概略**：頂点 $C$ を通り $AD$ に平行な直線を引き、直線 $AB$ との交点を $E$ とします。平行線の性質（中級編）から $\angle BAD = \angle AEC$、$\angle DAC = \angle ACE$ となり、$\angle BAD=\angle DAC$（仮定）とあわせて $\angle AEC = \angle ACE$、よって三角形 $ACE$ は $AC=AE$ の二等辺三角形になります。$AD \parallel EC$ から平行線と線分の比（中級編）を使うと $BD:DC = AB:AE = AB:AC$ が得られます。

![頂角Aの二等分線ADが対辺BCをBD:DC=AB:ACに内分することを示す図](triangle-theorems/images/angle-bisector.svg)

---

## チェバの定理

三角形 $ABC$ の内部の1点 $P$ を通る3本の直線 $AP$、$BP$、$CP$ が、対辺（の延長）とそれぞれ点 $D$、$E$、$F$ で交わるとき、

$$\frac{BD}{DC}\cdot\frac{CE}{EA}\cdot\frac{AF}{FB} = 1$$

が成り立ちます。これを**チェバの定理**といいます。三角形 $ABD$ と $ACD$ の面積比などを利用して証明できます（3つの小三角形の面積比を辺の比に対応させ、掛け合わせるとちょうど打ち消し合う）。

![三角形ABCの内部の点Pを通る3本の直線AD、BE、CFが対辺と交わり、比の積が1になることを示す図](triangle-theorems/images/ceva-theorem.svg)

**例題**：点$D$、$E$が辺$BC$、$CA$上にあり、$BD:DC=2:1$、$CE:EA=3:2$のとき、線分$AD$と$BE$の交点を通り頂点$C$を通る直線が辺$AB$と交わる点$F$について、$AF:FB$を求める。チェバの定理より $\dfrac{BD}{DC}\cdot\dfrac{CE}{EA}\cdot\dfrac{AF}{FB}=1$ なので、$\dfrac{2}{1}\cdot\dfrac{3}{2}\cdot\dfrac{AF}{FB}=1$、$3\cdot\dfrac{AF}{FB}=1$、$AF:FB=1:3$。

---

## メネラウスの定理

三角形 $ABC$ の3辺（またはその延長）が1本の直線と、それぞれ点 $D$、$E$、$F$ で交わるとき、

$$\frac{BD}{DC}\cdot\frac{CE}{EA}\cdot\frac{AF}{FB} = 1$$

チェバの定理と同じ形の式になりますが、点 $P$ が三角形の内部にあるか、直線が三角形の外を通るかという状況が異なります。相似な三角形の組を見つけることで証明できます。

**例題**：辺$BC$の延長上の点$D$について$BD:DC=3:1$（$D$は$C$の外側）、辺$CA$上の点$E$について$CE:EA=1:2$のとき、直線$DE$が辺$AB$（の延長）と交わる点$F$について、$AF:FB$を求める。メネラウスの定理より $\dfrac{BD}{DC}\cdot\dfrac{CE}{EA}\cdot\dfrac{AF}{FB}=1$ なので、$\dfrac{3}{1}\cdot\dfrac{1}{2}\cdot\dfrac{AF}{FB}=1$、$\dfrac{3}{2}\cdot\dfrac{AF}{FB}=1$、$AF:FB=2:3$。

---

## 定理の逆

チェバの定理・メネラウスの定理は、いずれも逆が成り立つことが知られています。つまり、3つの比の積が1になることが確かめられれば、3直線が1点で交わる（または3点が1直線上にある）ことが示せます。これは「3本の中線が1点（重心）で交わること」のような性質を証明する際にも使えます。

---

## まとめ

角の二等分線は対辺を、両側の辺の長さの比に内分します。チェバの定理は三角形の内部の1点から出る3本の線が満たす比の関係、メネラウスの定理は三角形の辺（の延長）を1本の直線が横切るときに満たす比の関係で、どちらも同じ形の式で表されます。

---

## 関連ページ

- [円の性質（応用編）](circle-theorems.md)
