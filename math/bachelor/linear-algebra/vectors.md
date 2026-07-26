---
title: ベクトル
description: "大きさと向きを持つベクトルを成分表示で扱い、ノルム・内積の幾何学的意味と線形独立の概念を理解したうえで、多項式や行列も含む一般のベクトル空間の定義へとつなげる"
goal: "ベクトルを成分表示で扱い、内積の幾何学的意味と線形独立の概念を理解して、一般のベクトル空間の定義につなげられるようになる"
tags: [math, linear-algebra, vectors]
stage: bachelor
subject: 線形代数
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: ベクトル
    path: vectors.md
requires:
  - title: 空間座標とベクトル
    path: ../../advanced/geometry/space-vectors.md
  - title: 環と体
    path: ../algebra/abstract-rings-fields.md
---

## 大きさだけでは足りない

「時速60kmで進む」という情報だけでは、どこに向かっているかわかりません。「北向きに時速60kmで進む」——**方向**があって初めて移動が定まります。このように「大きさ」と「向き」の両方を持つ量を**ベクトル**といいます。力・速度・変位などがベクトルです。

---

## 成分表示と基本演算

$n$ 次元ベクトルは実数を $n$ 個並べた組で表します。

$$\boldsymbol{a} = (a_1, a_2, \ldots, a_n) \in \mathbb{R}^n$$

**加法**：$\boldsymbol{a} + \boldsymbol{b} = (a_1+b_1, \ldots, a_n+b_n)$

**スカラー倍**：$c\boldsymbol{a} = (ca_1, \ldots, ca_n)$

幾何学的には、矢印の先から次の矢印をつないで足し算を表せます。

---

## ノルムと内積

$$\|\boldsymbol{a}\| = \sqrt{a_1^2 + \cdots + a_n^2}$$

大きさが1のベクトルを**単位ベクトル**といい、$\hat{\boldsymbol{a}} = \boldsymbol{a}/\|\boldsymbol{a}\|$ で得られます。

**内積**：

$$\boldsymbol{a} \cdot \boldsymbol{b} = a_1 b_1 + \cdots + a_n b_n = \|\boldsymbol{a}\| \|\boldsymbol{b}\| \cos\theta$$

（$\theta$ は2ベクトルのなす角）。「どれだけ同じ向きを向いているか」を数値化したもので、$\boldsymbol{a} \cdot \boldsymbol{b} = 0 \iff \boldsymbol{a} \perp \boldsymbol{b}$（直交）です。

**成分での定義と$\|\boldsymbol{a}\|\|\boldsymbol{b}\|\cos\theta$が一致することの確認**：$\boldsymbol{a}$、$\boldsymbol{b}$、$\boldsymbol{a}-\boldsymbol{b}$を3辺とする三角形に余弦定理を適用すると、$\|\boldsymbol{a}-\boldsymbol{b}\|^2=\|\boldsymbol{a}\|^2+\|\boldsymbol{b}\|^2-2\|\boldsymbol{a}\|\|\boldsymbol{b}\|\cos\theta$。左辺を成分で展開すると $\|\boldsymbol{a}-\boldsymbol{b}\|^2=\sum_i(a_i-b_i)^2=\sum_i a_i^2-2\sum_i a_ib_i+\sum_i b_i^2=\|\boldsymbol{a}\|^2-2(a_1b_1+\cdots+a_nb_n)+\|\boldsymbol{b}\|^2$。両者を比較すると $-2(a_1b_1+\cdots+a_nb_n)=-2\|\boldsymbol{a}\|\|\boldsymbol{b}\|\cos\theta$、すなわち $a_1b_1+\cdots+a_nb_n=\|\boldsymbol{a}\|\|\boldsymbol{b}\|\cos\theta$ が確かめられます。

**例**：$\boldsymbol{a} = (1, 2)$、$\boldsymbol{b} = (3, -1)$ のとき $\boldsymbol{a} \cdot \boldsymbol{b} = 3 - 2 = 1$

---

## 線形独立

ベクトルの組 $\{\boldsymbol{v}_1, \ldots, \boldsymbol{v}_k\}$ が**線形独立**であるとは、

$$c_1\boldsymbol{v}_1 + \cdots + c_k\boldsymbol{v}_k = \boldsymbol{0} \implies c_1 = \cdots = c_k = 0$$

が成り立つことです。「どのベクトルも他のベクトルの組み合わせでは表せない」という意味で、$\mathbb{R}^n$ では線形独立なベクトルは最大 $n$ 個です。

**例**：$(1, 0)$ と $(0, 1)$ は線形独立。$(1, 2)$ と $(2, 4)$ は線形従属（$(2,4) = 2(1,2)$）。

---

## 一般のベクトル空間

ここまでの $\mathbb{R}^n$ の議論は、より一般的な**ベクトル空間**（線形空間）の特別な場合です。

**定義**：体 $F$ 上のベクトル空間とは、加法とスカラー倍を持つ集合 $V$ であって、次を満たすもの：加法について $V$ は可換群をなし、スカラー倍について $a(bv) = (ab)v$、$1v = v$、分配律 $a(u+v) = au+av$、$(a+b)v = av+bv$ が成り立つ。

多項式全体、行列全体、連続関数全体なども、この意味でベクトル空間になります。線形独立・基底・次元といった概念は、$\mathbb{R}^n$ に限らずこの一般のベクトル空間で定義されます。

---

## まとめ

ベクトルは大きさと向きを持つ量で、成分表示すれば加法・スカラー倍・内積が定義できます。内積は2つのベクトルの方向の一致度を表し、線形独立は「無駄のない」ベクトルの組を特徴づけます。これらの概念は $\mathbb{R}^n$ に限らず、一般のベクトル空間で通用します。

---

## 関連ページ

- [行列（発展編）](matrices.md)
- [線形写像（発展編）](linear-maps.md)
