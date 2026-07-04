---
title: 三角形の性質の応用
description: "角の二等分線と辺の比、チェバの定理・メネラウスの定理"
goal: "角の二等分線と辺の比の関係を理解し、チェバの定理・メネラウスの定理を使えるようになる"
tags: [math, geometry, triangle]
stage: 応用編
subject: 幾何
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 応用編
    path: /math/advanced/index.md
  - title: 三角形の性質の応用
    path: /math/advanced/geometry/triangle-theorems.md
requires:
  - title: 三角形
    path: triangles.md
  - title: 相似
    path: /math/intermediate/geometry/similarity.md
---

## 角の二等分線と辺の比

三角形 $ABC$ の頂角 $A$ の二等分線が、対辺 $BC$ と交わる点を $D$ とすると、次の関係が成り立ちます。

$$BD:DC = AB:AC$$

**証明の概略**：頂点 $C$ を通り $AD$ に平行な直線を引き、直線 $AB$ との交点を $E$ とします。平行線の性質（中級編）から $\angle BAD = \angle AEC$、$\angle DAC = \angle ACE$ となり、$\angle BAD=\angle DAC$（仮定）とあわせて $\angle AEC = \angle ACE$、よって三角形 $ACE$ は $AC=AE$ の二等辺三角形になります。$AD \parallel EC$ から平行線と線分の比（中級編）を使うと $BD:DC = AB:AE = AB:AC$ が得られます。

---

## チェバの定理

三角形 $ABC$ の内部の1点 $P$ を通る3本の直線 $AP$、$BP$、$CP$ が、対辺（の延長）とそれぞれ点 $D$、$E$、$F$ で交わるとき、

$$\frac{BD}{DC}\cdot\frac{CE}{EA}\cdot\frac{AF}{FB} = 1$$

が成り立ちます。これを**チェバの定理**といいます。三角形 $ABD$ と $ACD$ の面積比などを利用して証明できます（3つの小三角形の面積比を辺の比に対応させ、掛け合わせるとちょうど打ち消し合う）。

---

## メネラウスの定理

三角形 $ABC$ の3辺（またはその延長）が1本の直線と、それぞれ点 $D$、$E$、$F$ で交わるとき、

$$\frac{BD}{DC}\cdot\frac{CE}{EA}\cdot\frac{AF}{FB} = 1$$

チェバの定理と同じ形の式になりますが、点 $P$ が三角形の内部にあるか、直線が三角形の外を通るかという状況が異なります。相似な三角形の組を見つけることで証明できます。

---

## 定理の逆

チェバの定理・メネラウスの定理は、いずれも逆が成り立つことが知られています。つまり、3つの比の積が1になることが確かめられれば、3直線が1点で交わる（または3点が1直線上にある）ことが示せます。これは「3本の中線が1点（重心）で交わること」のような性質を証明する際にも使えます。

---

## まとめ

角の二等分線は対辺を、両側の辺の長さの比に内分します。チェバの定理は三角形の内部の1点から出る3本の線が満たす比の関係、メネラウスの定理は三角形の辺（の延長）を1本の直線が横切るときに満たす比の関係で、どちらも同じ形の式で表されます。

---

## 関連ページ

- [三角形（応用編）](triangles.md)
- [相似（中級編）](/math/intermediate/geometry/similarity.md)
- [円の性質（応用編）](circle-theorems.md)
