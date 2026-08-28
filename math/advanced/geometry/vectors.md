---
title: ベクトル
description: "向きと大きさを持つベクトルの和・差・実数倍の演算と、位置ベクトル・成分表示、内積の定義と垂直性の判定、位置ベクトルを使って三角形の重心や図形の性質を証明する応用を扱う"
goal: "平面上のベクトルの演算・内積を理解し、図形の性質を証明する道具として使えるようになる"
tags: [math, geometry, vectors]
stage: advanced
subject: 幾何
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 応用編
    path: ../index.md
  - title: ベクトル
    path: vectors.md
requires:
  - title: 点
    path: point.md
  - title: 三角形
    path: triangles.md
---

## 向きと大きさを持つ量

「東へ3km」と「北へ3km」は、同じ3kmでも意味が違います。移動には距離（大きさ）だけでなく向きも関わります。このように、**大きさ**と**向き**をあわせ持つ量を**ベクトル**といい、矢印（有向線分）で表します。矢印の位置は問わず、向きと長さが同じならすべて同じベクトルとみなします。

ベクトル $\vec{a}$ の大きさは $|\vec{a}|$ と書きます。

---

## 和・差・実数倍

2つのベクトル $\vec{a}$、$\vec{b}$ の和 $\vec{a}+\vec{b}$ は、$\vec{a}$ の終点に $\vec{b}$ の始点をつないでできる矢印です（平行四辺形の対角線としても表せます）。この矢印は $\vec{a}$ の始点から $\vec{b}$ の終点への矢印になります。実数倍 $k\vec{a}$ は、向きはそのまま（$k<0$ なら逆向き）で長さを $|k|$ 倍したベクトルです。特に $k=-1$ のとき、$-\vec{a}$ は $\vec{a}$ と大きさが同じで向きが反対のベクトルを表します。同様に $-\vec{b}$ は $\vec{b}$ の逆向きのベクトルです。差 $\vec{a}-\vec{b}$ は $\vec{a}+(-\vec{b})$、つまり $\vec{a}$ に $\vec{b}$ の逆向きベクトルを加えたものとして定義されます。

これらの演算は、数の加法・乗法と同じ交換法則・結合法則・分配法則を満たします。

![ベクトルaとbを矢印でつなぎ、和a+bが始点から終点への矢印になることを示す図](vectors/images/vector-addition.svg)

---

## 位置ベクトルと成分表示

平面上に基準の点（原点）$O$ を固定します。一般に $\overrightarrow{PQ}$ は $P$ を始点、$Q$ を終点とするベクトルを表します。任意の点 $A$ の位置は、$O$ を始点とするベクトル $\vec{a}=\overrightarrow{OA}$（**位置ベクトル**）でただ1通りに表せます。

座標平面では、ベクトルを成分 $(x, y)$ で表します。2点 $A(x_1,y_1)$、$B(x_2,y_2)$ に対して、$\overrightarrow{AB}$ の成分は $(x_2-x_1, y_2-y_1)$ です。$\overrightarrow{AB}$ の大きさは $|\overrightarrow{AB}|=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2}$ で求まり、これは点と点の距離の公式と同じです。

---

## 内積

2つのベクトル $\vec{a}$、$\vec{b}$ のなす角を $\theta$ とするとき、**内積**を次のように定めます。

$$\vec{a}\cdot\vec{b} = |\vec{a}||\vec{b}|\cos\theta$$

成分表示 $\vec{a}=(a_1,a_2)$、$\vec{b}=(b_1,b_2)$ では $\vec{a}\cdot\vec{b}=a_1b_1+a_2b_2$ とも計算でき、これは次のように確かめられます。原点を $O$ とし、$\vec{a}=\overrightarrow{OA}$、$\vec{b}=\overrightarrow{OB}$ とします。

まず、余弦定理（[三角形](triangles.md)）を三角形 $OAB$ に適用すると、$|AB|^2=|\vec{a}|^2+|\vec{b}|^2-2|\vec{a}||\vec{b}|\cos\theta$ です。

次に、2点間の距離の公式（[点](point.md)）を適用すると、$|AB|^2=(b_1-a_1)^2+(b_2-a_2)^2$ です。これを展開すると $(b_1-a_1)^2+(b_2-a_2)^2=b_1^2-2a_1b_1+a_1^2+b_2^2-2a_2b_2+a_2^2=(a_1^2+a_2^2)+(b_1^2+b_2^2)-2(a_1b_1+a_2b_2)=|\vec{a}|^2+|\vec{b}|^2-2(a_1b_1+a_2b_2)$ となるので、$|AB|^2=|\vec{a}|^2+|\vec{b}|^2-2(a_1b_1+a_2b_2)$ です。

両者を比較すると $|\vec{a}||\vec{b}|\cos\theta=a_1b_1+a_2b_2$、つまり $\vec{a}\cdot\vec{b}=a_1b_1+a_2b_2$ が得られます。

内積の基本性質：

$$\vec{a}\cdot\vec{a}=|\vec{a}|^2, \quad \vec{a}\cdot\vec{b}=\vec{b}\cdot\vec{a}, \quad (k\vec{a})\cdot\vec{b}=k(\vec{a}\cdot\vec{b}), \quad \vec{a}\cdot(\vec{b}+\vec{c})=\vec{a}\cdot\vec{b}+\vec{a}\cdot\vec{c}$$

分配法則 $\vec{a}\cdot(\vec{b}+\vec{c})=\vec{a}\cdot\vec{b}+\vec{a}\cdot\vec{c}$ は、$\vec{c}=(c_1,c_2)$ として成分表示を使うと $\vec{a}\cdot(\vec{b}+\vec{c})=a_1(b_1+c_1)+a_2(b_2+c_2)=(a_1b_1+a_2b_2)+(a_1c_1+a_2c_2)=\vec{a}\cdot\vec{b}+\vec{a}\cdot\vec{c}$ と確かめられます。

特に、$\vec{a}\cdot\vec{b}=0$ は $\vec{a}$ と $\vec{b}$ が垂直であることを意味します（$\theta=90°$ で $\cos\theta=0$）。

---

## 図形の性質への応用

ベクトルを使うと、三角形などの図形の性質を、座標を使わずに形式的な計算だけで証明できます。

**例題**：三角形 $ABC$ の3本の中線が1点で交わることを、位置ベクトルを使って示す。

頂点の位置ベクトルを $\vec{a},\vec{b},\vec{c}$ とし、$G=\dfrac{\vec{a}+\vec{b}+\vec{c}}{3}$ とおきます。辺$BC$の中点を$M$とすると、$M$の位置ベクトルは $\dfrac{\vec{b}+\vec{c}}{2}$ です。

中線$AM$上の点は $\vec{a}+t\left(\dfrac{\vec{b}+\vec{c}}{2}-\vec{a}\right)$（$0\leq t\leq1$）と表せます。中線は、頂点から対辺の中点までの線分を$A$側から$2:1$に内分する点（重心）を通ることが知られています（[点](point.md)を参照）。この点は$A$から$M$までの$\dfrac23$の位置に当たるので、$G$が中線$AM$上のその点に一致するかを確かめるため、$t=\dfrac23$ を代入すると、

$$\vec{a}+\frac23\left(\frac{\vec{b}+\vec{c}}{2}-\vec{a}\right) = \vec{a}+\frac{\vec{b}+\vec{c}}{3}-\frac23\vec{a} = \frac{\vec{a}+\vec{b}+\vec{c}}{3} = G$$

となり、$G$は中線$AM$上（$A$から$M$までの$\dfrac23$の位置）にあることが確かめられます。頂点$B$、$C$から引いた中線についても、$\vec{a},\vec{b},\vec{c}$を入れ替えるだけで同じ計算ができるので、$G$は3本の中線すべての上にあり、1点で交わることが示せます。$\square$

内積を使うと、図形の性質も証明できます。例えば「ひし形の対角線は垂直に交わる」ことは、頂点を$O,A,A+B,B$（$O$を基準とした位置ベクトルをそれぞれ$\vec 0,\vec a,\vec a+\vec b,\vec b$とし、$|\vec a|=|\vec b|$）とすると、対角線のベクトルが$\vec a+\vec b$と$\vec a-\vec b$になり、$(\vec a+\vec b)\cdot(\vec a-\vec b)=|\vec a|^2-|\vec b|^2=0$ から確かめられます。同様に「三角形の3本の垂線は1点で交わる」ことも内積を使って示せます。

---

## まとめ

ベクトルは向きと大きさを持つ量で、和・差・実数倍の演算ができます。内積 $\vec{a}\cdot\vec{b}=|\vec{a}||\vec{b}|\cos\theta$ は2つのベクトルの角度の情報を数値化したもので、0になることが垂直の判定に使えます。位置ベクトルを使うと、図形の性質を座標によらず形式的に証明できます。

---

## 関連ページ

- [空間座標とベクトル](space-vectors.md)
