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

平面や空間の矢印としてのベクトルは直感的ですが、多変数のデータや多元連立方程式を扱うには、2次元・3次元だけでは足りません。そこで、成分の個数を $n$ に一般化した $n$ 次元ベクトルを考えます。$n$ 次元ベクトルは実数を $n$ 個並べた組で表します。

$$\boldsymbol{a} = (a_1, a_2, \ldots, a_n) \in \mathbb{R}^n$$

**加法**：$\boldsymbol{a} + \boldsymbol{b} = (a_1+b_1, \ldots, a_n+b_n)$

**スカラー倍**：$c\boldsymbol{a} = (ca_1, \ldots, ca_n)$

幾何学的には、$\boldsymbol{a}$ の始点を原点に置き、$\boldsymbol{b}$ の始点を $\boldsymbol{a}$ の終点に置くと、原点から $\boldsymbol{b}$ の終点までを結んだ矢印が $\boldsymbol{a} + \boldsymbol{b}$ を表します。

---

## ノルムと内積

$$\|\boldsymbol{a}\| = \sqrt{a_1^2 + \cdots + a_n^2}$$

大きさが1のベクトルを**単位ベクトル**といい、$\hat{\boldsymbol{a}} = \boldsymbol{a}/\|\boldsymbol{a}\|$ で得られます（ただし $\boldsymbol{a}=\boldsymbol{0}$ のときは定義されません）。

**内積**：

$$\boldsymbol{a} \cdot \boldsymbol{b} = a_1 b_1 + \cdots + a_n b_n = \|\boldsymbol{a}\| \|\boldsymbol{b}\| \cos\theta$$

（$\theta$ は2ベクトルのなす角）。「どれだけ同じ向きを向いているか」を数値化したもので、$\boldsymbol{a} \cdot \boldsymbol{b} = 0 \iff \boldsymbol{a} \perp \boldsymbol{b}$（直交）です。

**成分での定義と$\|\boldsymbol{a}\|\|\boldsymbol{b}\|\cos\theta$が一致することの確認**：$\boldsymbol{a}$、$\boldsymbol{b}$、$\boldsymbol{a}-\boldsymbol{b}$は始点を共有する2ベクトルとその差であり、$\boldsymbol{a}$と$\boldsymbol{b}$を含む平面に含まれます。そのため、通常の（平面上の）余弦定理がそのまま適用できます。原点を$O$、$\boldsymbol{a}$の終点を$A$、$\boldsymbol{b}$の終点を$B$とします。三角形$OAB$において、辺$OA$の長さは$\|\boldsymbol{a}\|$、辺$OB$の長さは$\|\boldsymbol{b}\|$、辺$AB$の長さは$\|\boldsymbol{a}-\boldsymbol{b}\|$に対応します。

まず、$\boldsymbol{a}$、$\boldsymbol{b}$、$\boldsymbol{a}-\boldsymbol{b}$を3辺とする三角形に余弦定理を適用すると、次が成り立ちます。

$$\|\boldsymbol{a}-\boldsymbol{b}\|^2=\|\boldsymbol{a}\|^2+\|\boldsymbol{b}\|^2-2\|\boldsymbol{a}\|\|\boldsymbol{b}\|\cos\theta$$

次に、$(a_i-b_i)^2$を展開し、和を項ごとに分割すると、左辺は次のようになります。

$$
\begin{aligned}
\|\boldsymbol{a}-\boldsymbol{b}\|^2 &= \sum_i(a_i-b_i)^2 \\
&= \sum_i a_i^2-2\sum_i a_ib_i+\sum_i b_i^2 \\
&= \|\boldsymbol{a}\|^2-2(a_1b_1+\cdots+a_nb_n)+\|\boldsymbol{b}\|^2
\end{aligned}
$$

3行目では$\sum_i a_i^2$、$\sum_i b_i^2$がそれぞれ$\|\boldsymbol{a}\|^2$、$\|\boldsymbol{b}\|^2$に、$\sum_i a_ib_i$が内積の成分表示に対応しています。

両者を比較すると $-2(a_1b_1+\cdots+a_nb_n)=-2\|\boldsymbol{a}\|\|\boldsymbol{b}\|\cos\theta$、すなわち $a_1b_1+\cdots+a_nb_n=\|\boldsymbol{a}\|\|\boldsymbol{b}\|\cos\theta$ が確かめられます。

**例**：$\boldsymbol{a} = (1, 2)$、$\boldsymbol{b} = (3, -1)$ のとき $\boldsymbol{a} \cdot \boldsymbol{b} = 3 - 2 = 1$

---

## 線形独立

ベクトルの組 $\{\boldsymbol{v}_1, \ldots, \boldsymbol{v}_k\}$ が**線形独立**であるとは、

$$c_1\boldsymbol{v}_1 + \cdots + c_k\boldsymbol{v}_k = \boldsymbol{0} \implies c_1 = \cdots = c_k = 0$$

が成り立つことです。この式の左辺のような、ベクトルをスカラー倍して足し合わせた式を**線形結合**といいます。「どのベクトルも他のベクトルの組み合わせでは表せない」という意味です。実際、逆に、係数の1つが0でなければ、その項を移項して該当のベクトルを他のベクトルの組み合わせで表せます。線形独立でないベクトルの組を**線形従属**といいます。$\mathbb{R}^n$ では線形独立なベクトルは最大 $n$ 個です。この事実の背景には、標準基底$\boldsymbol{e}_1,\ldots,\boldsymbol{e}_n$がちょうど$n$個のベクトルからなり、これより多い独立な組は作れないという次元に関する性質があります。厳密な証明は本記事の範囲を超えるため省略します。

**例**：$(1, 0)$ と $(0, 1)$ は線形独立。$(1, 2)$ と $(2, 4)$ は線形従属（$(2,4) = 2(1,2)$）。

---

## 一般のベクトル空間

ここまでの $\mathbb{R}^n$ の議論は、より一般的な**ベクトル空間**（線形空間）の特別な場合です。多項式・行列・連続関数といった一見異なる対象も、この枠組みで統一的に扱えます。共通の理論を一度示せば、個々の対象について加法やスカラー倍の性質を毎回議論し直す必要がなくなります。

**定義**：体 $F$ 上のベクトル空間とは、加法とスカラー倍を持つ集合 $V$ であって、次を満たすものです。

まず、加法について $V$ は**可換群**をなします。可換群とは、次を満たす集合のことです。

- 結合律：$(u+v)+w = u+(v+w)$
- 交換律：$u+v = v+u$
- 単位元の存在：$v+0=v$ を満たす零ベクトル $0 \in V$ が存在する
- 逆元の存在：任意の $v \in V$ に対して $v+(-v)=0$ を満たす $-v \in V$ が存在する

さらに、スカラー倍について次が成り立ちます。

- 結合律：$a(bv) = (ab)v$
- 単位元則：$1v = v$
- 分配律：$a(u+v) = au+av$、$(a+b)v = av+bv$

多項式全体、行列全体、連続関数全体なども、この意味でベクトル空間になります。

例えば、2次以下の多項式全体 $\{c_0 + c_1x + c_2x^2 \mid c_0, c_1, c_2 \in \mathbb{R}\}$ を考えます。

加法は係数ごとの和 $(c_0+c_1x+c_2x^2)+(d_0+d_1x+d_2x^2)=(c_0+d_0)+(c_1+d_1)x+(c_2+d_2)x^2$、スカラー倍は係数への一斉倍 $k(c_0+c_1x+c_2x^2)=(kc_0)+(kc_1)x+(kc_2)x^2$ と定めます。

このとき加法の交換律は、実数の加法が交換律を満たすことから、係数ごとに $c_i+d_i=d_i+c_i$ が成り立つのでそのまま従います。加法については、結合律・単位元（零多項式 $0+0x+0x^2$）・逆元（係数を反転した多項式）も、同様に係数ごとの実数の性質からそのまま従います。スカラー倍についても、結合律・単位元則・分配律が同様に成り立ちます。

線形独立・基底・次元といった概念は、$\mathbb{R}^n$ に限らずこの一般のベクトル空間で定義されます。生成系とは、その線形結合によってベクトル空間内のすべてのベクトルを表せる集合のことです。生成系のうち線形独立なものを**基底**といい、基底に含まれるベクトルの個数を**次元**といいます。

---

## まとめ

ベクトルは大きさと向きを持つ量で、成分表示すれば加法・スカラー倍・内積が定義できます。内積は2つのベクトルの方向の一致度を表し、線形独立は「無駄のない」ベクトルの組を特徴づけます。これらの概念は $\mathbb{R}^n$ に限らず、一般のベクトル空間で通用します。

---

## 関連ページ

- [行列](matrices.md)
- [線形写像](linear-maps.md)
