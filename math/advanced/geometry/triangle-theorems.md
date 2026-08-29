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
  - title: 三角比
    path: trigonometry.md
---

## 角の二等分線と辺の比

三角形 $ABC$ の角 $A$ の二等分線が、対辺 $BC$ と交わる点を $D$ とすると、次の関係が成り立ちます。

$$BD:DC = AB:AC$$

![角Aの二等分線ADが対辺BCをBD:DC=AB:ACに内分することを示す図。証明で用いる補助線として、頂点Cを通りADに平行な直線を引き、直線ABとの交点をEとしている](triangle-theorems/images/angle-bisector.svg)

**証明**：頂点 $C$ を通り $AD$ に平行な直線を引き、直線 $AB$ との交点を $E$ とします（上図）。

$AD \parallel EC$ より、$\angle BAD = \angle AEC$（同位角の関係）が成り立ちます。同じく $AD \parallel EC$ より、$\angle DAC = \angle ACE$（錯角の関係）が成り立ちます。仮定より $\angle BAD = \angle DAC$ なので、これら2つの等式とあわせると $\angle AEC = \angle ACE$ が得られます。

よって三角形 $ACE$ は2つの底角が等しい二等辺三角形であり、$AC=AE$ が成り立ちます。

三角形 $BEC$ において、辺 $BE$、$BC$ 上の点 $A$、$D$ が $AD \parallel EC$ を満たすので、[相似](../../intermediate/geometry/similarity.md)で見た「平行線と線分の比」の関係より $BA:BE = BD:BC$ が成り立ちます。

> [!NOTE]
> $BA:BE=BD:BC$ の変形に使う一般の性質：$a:b=c:d$ が成り立つとき、$a:(b-a)=c:(d-c)$ も成り立ちます（$a=bk$、$c=dk$（$k$は比の値）とおくと $b-a=b(1-k)$、$d-c=d(1-k)$ となり、$a:(b-a)=bk:b(1-k)=k:(1-k)$、$c:(d-c)=dk:d(1-k)=k:(1-k)$ で一致するため）。

$a=BA,\ b=BE,\ c=BD,\ d=BC$ として適用すると、$DC=BC-BD$、$AE=BE-BA$ を用いて $BA:AE = BD:DC$ が得られます。

$AE=AC$ とあわせて $BD:DC = AB:AC$ が得られます。$\square$

---

## チェバの定理

三角形 $ABC$ の内部の1点 $P$ を通る3本の直線 $AP$、$BP$、$CP$ が、それぞれ辺 $BC$、$CA$、$AB$ と点 $D$、$E$、$F$ で交わるとき、

$$\frac{BD}{DC}\cdot\frac{CE}{EA}\cdot\frac{AF}{FB} = 1$$

が成り立ちます。これを**チェバの定理**といいます。

![三角形ABCの内部の点Pを通る3本の直線AP、BP、CPが対辺と交わり、比の積が1になることを示す図](triangle-theorems/images/ceva-theorem.svg)

**証明**：三角形 $XYZ$ の面積を $[\triangle XYZ]$ と表します。

三角形の面積は[三角形](triangles.md)で見た $S=\frac12\times\text{底辺}\times\text{高さ}$ で求まるので、$D$ は辺 $BC$ 上、$P$ は線分 $AD$ 上にあることから、頂点 $A$ を共有し底辺 $BD$、$DC$ が同一直線上にあり高さが等しい三角形 $ABD$、$ACD$ の面積比は底辺の比に等しく、$[\triangle ABD]:[\triangle ACD] = BD:DC$ が成り立ちます。同様に頂点 $P$ を共有する三角形 $PBD$、$PCD$ についても $[\triangle PBD]:[\triangle PCD] = BD:DC$ が成り立ちます。

$P$ が線分 $AD$ 上にあることから、線分 $BP$ は三角形 $ABD$ を三角形 $ABP$ と $PBD$ に、線分 $CP$ は三角形 $ACD$ を三角形 $ACP$ と $PCD$ に分割するので、$[\triangle ABP] = [\triangle ABD]-[\triangle PBD]$、$[\triangle ACP]=[\triangle ACD]-[\triangle PCD]$ となります。

> [!NOTE]
> 面積比の引き算に使う一般の性質：$a:b=c:d$ が成り立つとき、$a:b=(a-c):(b-d)$ も成り立ちます（$a=bk,c=dk$ とおくと $a-c=(b-d)k$ となるため）。

$a=[\triangle ABD],\ b=[\triangle ACD],\ c=[\triangle PBD],\ d=[\triangle PCD]$ としてこの性質を適用すると

$$BD:DC = [\triangle ABD]:[\triangle ACD] = ([\triangle ABD]-[\triangle PBD]):([\triangle ACD]-[\triangle PCD]) = [\triangle ABP]:[\triangle CAP]$$

が得られます（$[\triangle ACP]$ を $[\triangle CAP]$ と表記しています。3つの式を辺々掛け合わせた際に約分できるよう、分母・分子の順序をそろえるためです）。

全く同様に、頂点 $B$、$C$ を通る2本の直線についても、$A,B,C$ を $B,C,A$ に、対応して $D,E,F$ を $E,F,D$ に読み替え、$P$ はそのまま（3直線すべての交点であるため不変）とすれば全く同じ議論で

$$CE:EA = [\triangle BCP]:[\triangle ABP], \qquad AF:FB = [\triangle CAP]:[\triangle BCP]$$

が成り立つので、3つの式を辺々掛け合わせると

$$\frac{BD}{DC}\cdot\frac{CE}{EA}\cdot\frac{AF}{FB} = \frac{[\triangle ABP]}{[\triangle CAP]}\cdot\frac{[\triangle BCP]}{[\triangle ABP]}\cdot\frac{[\triangle CAP]}{[\triangle BCP]} = 1$$

となり、途中の面積がすべて打ち消し合ってチェバの定理が得られます。$\square$

**例題**：辺$BC$、$CA$上にそれぞれ点$D$、$E$をとり、線分$AD$と$BE$の交点を通り頂点$C$を通る直線が辺$AB$と交わる点を$F$とする。線分$AD$と$BE$の交点が定理の点$P$にあたります。$BD:DC=2:1$、$CE:EA=3:2$のとき、$AF:FB$を求める。チェバの定理より $\dfrac{BD}{DC}\cdot\dfrac{CE}{EA}\cdot\dfrac{AF}{FB}=1$ なので、$\dfrac{2}{1}\cdot\dfrac{3}{2}\cdot\dfrac{AF}{FB}=1$、$3\cdot\dfrac{AF}{FB}=1$、$AF:FB=1:3$。

---

## メネラウスの定理

三角形 $ABC$ の辺 $BC$、$CA$、$AB$（またはその延長）が1本の直線とそれぞれ点 $D$、$E$、$F$ で交わるとき、

$$\frac{BD}{DC}\cdot\frac{CE}{EA}\cdot\frac{AF}{FB} = 1$$

チェバの定理と同じ形の式になりますが、3本の直線が三角形の内部の1点で交わる場合と、1本の直線が三角形の辺（またはその延長）を横切る場合という状況が異なります。

![三角形ABCの辺BCの延長上の点D、辺CA上の点E、辺ABの点Fを通る直線ℓと、頂点A、B、Cから直線ℓへ下ろした垂線の足A'、B'、C'を示す図](triangle-theorems/images/menelaus-theorem.svg)

**証明**：直線 $DEF$ を $\ell$ とし、頂点 $A$、$B$、$C$ から $\ell$ に下ろした垂線の足をそれぞれ $A'$、$B'$、$C'$ とします。$D$ は直線 $BC$ と $\ell$ の交点なので、直角三角形 $BDB'$（直角は $B'$）と直角三角形 $CDC'$（直角は $C'$）を考えます。

$D$ が辺 $BC$ 上にある場合、$B$ と $C$ は点 $D$ を挟んで反対側にあり、$B'$ と $C'$ も同様に反対側にあるため、$\angle BDB'$ と $\angle CDC'$ は対頂角となり等しくなります。$D$ が辺 $BC$ の延長上にある場合（上図）、$B$ と $C$ は点 $D$ から見て同じ側にあり、$B'$ と $C'$ も同じ側にあるため、$\angle BDB'$ と $\angle CDC'$ はそもそも同一の角になり、当然等しくなります。

いずれの場合も角度が等しいので正弦の値も等しく、直角三角形の辺の比としての $\sin$ の定義（[三角比](trigonometry.md)）より $\sin\angle BDB' = \dfrac{BB'}{BD}$、$\sin\angle CDC'=\dfrac{CC'}{CD}$ なので $BD:DC = BB':CC'$ が成り立ちます。全く同様に、$A,B,C$（および対応する垂線の足 $A',B',C'$）を巡回的に $B,C,A$（$B',C',A'$）に読み替えれば $CE:EA = CC':AA'$、$AF:FB = AA':BB'$ が成り立つので、3つの式を辺々掛け合わせると

$$\frac{BD}{DC}\cdot\frac{CE}{EA}\cdot\frac{AF}{FB} = \frac{BB'}{CC'}\cdot\frac{CC'}{AA'}\cdot\frac{AA'}{BB'}=1$$

となり、メネラウスの定理が得られます。$\square$

**例題**：辺$BC$の延長上に点$D$を$BD:DC=3:1$（$D$は$C$の外側）となるようにとり、辺$CA$上に点$E$を$CE:EA=1:2$となるようにとる。直線$DE$が辺$AB$と交わる点を$F$とするとき、$AF:FB$を求める。メネラウスの定理より $\dfrac{BD}{DC}\cdot\dfrac{CE}{EA}\cdot\dfrac{AF}{FB}=1$ なので、$\dfrac{3}{1}\cdot\dfrac{1}{2}\cdot\dfrac{AF}{FB}=1$、$\dfrac{3}{2}\cdot\dfrac{AF}{FB}=1$、$AF:FB=2:3$。

---

## 定理の逆

チェバの定理・メネラウスの定理は、いずれも逆が成り立つことが知られています。チェバの定理の逆は、3点 $D,E,F$ がいずれも辺上にあるか、またはちょうど2点が延長上にある（延長上の点の数が偶数である）とき、3つの比の積が1になれば3直線 $AD$、$BE$、$CF$ は1点で交わる、というものです。メネラウスの定理の逆は、3点 $D,E,F$ のうちちょうど1点のみが延長上にあるか、またはすべてが延長上にある（延長上の点の数が奇数である）とき、3つの比の積が1になれば3点 $D,E,F$ は同一直線上にある、というものです。これは「3本の中線が1点（重心）で交わること」のような性質を証明する際にも使えます。

---

## まとめ

角の二等分線は対辺を、両側の辺の長さの比に内分します。チェバの定理は三角形の内部の1点から出る3本の線が満たす比の関係、メネラウスの定理は三角形の辺（の延長）を1本の直線が横切るときに満たす比の関係で、どちらも同じ形の式で表されます。

---

## 関連ページ

- [円の性質](circle-theorems.md)
