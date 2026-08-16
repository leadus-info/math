---
title: 固有値
description: "行列を掛けても方向が変わらない固有ベクトルと固有値を固有多項式から求め、相異なる固有値を持てば対角化可能であることを証明し、対角化によるべき乗の簡単化、トレース・行列式が固有値の総和・総積に一致することを証明する"
goal: "固有値・固有ベクトルを固有多項式から計算し、対角化可能性の十分条件を証明し、トレース・行列式と固有値の関係を証明できるようになる"
tags: [math, linear-algebra, eigenvalues]
stage: bachelor
subject: 線形代数
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 固有値
    path: eigenvalues.md
requires:
  - title: 線形写像
    path: linear-maps.md
  - title: 多項式
    path: ../../advanced/algebra/polynomials.md
---

## 方向が変わらないベクトル

行列を掛けると、普通はベクトルの方向が変わります。しかしある特別なベクトルは、行列を掛けても方向が変わらず、大きさだけが変わります。鏡の変換（$y$ 軸に関する反射）を考えると、$x$ 軸方向 $(1,0)$ は $(-1,0)$（$-1$倍）に、$y$ 軸方向 $(0,1)$ は $(0,1)$（$1$倍）のままです。

---

## 固有値の定義

正方行列 $A$ に対して $A\boldsymbol{v} = \lambda\boldsymbol{v}$（$\boldsymbol{v} \neq \boldsymbol{0}$）を満たすとき、$\lambda$ を**固有値**、$\boldsymbol{v}$ を固有値 $\lambda$ に対応する**固有ベクトル**といいます。$A\boldsymbol{v}=\lambda\boldsymbol{v}$ は $(A-\lambda I)\boldsymbol{v}=\boldsymbol{0}$ と同値です。

**命題**：$(A - \lambda I)\boldsymbol{v} = \boldsymbol{0}$ が $\boldsymbol{v}\neq\boldsymbol{0}$ なる解を持つことと、$\det(A - \lambda I) = 0$ は同値である。

**証明**：線形写像で証明した「単射 $\iff$ 核が $\{\boldsymbol{0}\}$」を、線形写像 $T(\boldsymbol{x})=(A-\lambda I)\boldsymbol{x}$ に適用します。$(A-\lambda I)\boldsymbol{v}=\boldsymbol{0}$ が非自明解を持つことは $\ker T \neq \{\boldsymbol{0}\}$ と同じ、すなわち $T$ が単射でないことと同じです。正方行列の場合、単射性は全射性・可逆性と同値（線形写像の記事の結論）なので、これは $A-\lambda I$ が可逆でないこと、すなわち $\det(A-\lambda I)=0$ と同値です。$\blacksquare$

---

## 固有多項式と固有値・固有ベクトルの求め方

$p(\lambda) = \det(A - \lambda I)$ を**固有多項式**といいます。$n \times n$ 行列の固有多項式は $\lambda$ の $n$ 次多項式で、固有値は $p(\lambda) = 0$ の根です。

**例**：$A = \begin{pmatrix}3&1\\0&2\end{pmatrix}$ のとき $\det(A - \lambda I) = (3-\lambda)(2-\lambda) = 0$ より $\lambda = 3$ または $\lambda = 2$。

固有値が決まったら $(A - \lambda I)\boldsymbol{v} = \boldsymbol{0}$ を解いて固有ベクトルを求めます。$\lambda = 3$ のとき $(A-3I)\boldsymbol{v} = \begin{pmatrix}0&1\\0&-1\end{pmatrix}\boldsymbol{v}=\boldsymbol{0}$ より $v_2=0$、固有ベクトルは $c\begin{pmatrix}1\\0\end{pmatrix}$。$\lambda=2$ のとき $v_1+v_2=0$ より固有ベクトルは $c\begin{pmatrix}1\\-1\end{pmatrix}$。

---

## 対角化

$n$ 個の線形独立な固有ベクトル $\boldsymbol{v}_1, \ldots, \boldsymbol{v}_n$ が存在するとき $A$ は**対角化可能**です。

$$A = P\Lambda P^{-1}, \quad P = (\boldsymbol{v}_1 \cdots \boldsymbol{v}_n), \quad \Lambda = \mathrm{diag}(\lambda_1, \ldots, \lambda_n)$$

**対角化可能の十分条件**：$n\times n$ 行列 $A$ が $n$ 個の相異なる固有値を持つならば、$A$ は対角化可能である。

**証明**：相異なる固有値 $\lambda_1,\ldots,\lambda_n$ に対応する固有ベクトルを $\boldsymbol{v}_1,\ldots,\boldsymbol{v}_n$ とします。これらが線形独立であることを、線形独立でないと仮定して矛盾を導くことで示します。

線形独立でないなら、その中に他の線形結合で表せるものがあり、$\boldsymbol{v}_1,\ldots,\boldsymbol{v}_k$ を線形従属となる最小個数の組（$k$ が最小）とできます。このとき $\boldsymbol{v}_k = c_1\boldsymbol{v}_1+\cdots+c_{k-1}\boldsymbol{v}_{k-1}$（$\boldsymbol{v}_1,\ldots,\boldsymbol{v}_{k-1}$ は最小性より線形独立）と書け、両辺に $A$ を掛けると、

$$\lambda_k \boldsymbol{v}_k = c_1\lambda_1\boldsymbol{v}_1+\cdots+c_{k-1}\lambda_{k-1}\boldsymbol{v}_{k-1}$$

一方、元の式の両辺を $\lambda_k$ 倍すると $\lambda_k\boldsymbol{v}_k = c_1\lambda_k\boldsymbol{v}_1+\cdots+c_{k-1}\lambda_k\boldsymbol{v}_{k-1}$。この2つを引き算すると、

$$\boldsymbol{0} = c_1(\lambda_1-\lambda_k)\boldsymbol{v}_1+\cdots+c_{k-1}(\lambda_{k-1}-\lambda_k)\boldsymbol{v}_{k-1}$$

$\boldsymbol{v}_1,\ldots,\boldsymbol{v}_{k-1}$ は線形独立なので、すべての係数が $0$、すなわち $c_i(\lambda_i-\lambda_k)=0$。固有値はすべて相異なる（$\lambda_i \neq \lambda_k$）ので $c_i=0$（$i=1,\ldots,k-1$）となり、$\boldsymbol{v}_k=\boldsymbol{0}$ となって固有ベクトルの定義（$\boldsymbol{v}\neq\boldsymbol{0}$）に矛盾します。よって $\boldsymbol{v}_1,\ldots,\boldsymbol{v}_n$ は線形独立で、$A$ は対角化可能です。$\blacksquare$

対角化のメリットは、行列の累乗が簡単になることです。$A^{100}\boldsymbol{v}$ を直接計算するのは大変ですが、$\boldsymbol{v}$ が固有ベクトルなら $A^{100}\boldsymbol{v} = \lambda^{100}\boldsymbol{v}$ で済みます。

**命題**：$A=P\Lambda P^{-1}$ のとき、任意の自然数 $k$ について $A^k = P\Lambda^k P^{-1}$。

**証明**：数学的帰納法で示します。$k=1$ は仮定そのものです。$k$ で成り立つと仮定すると、

$$A^{k+1} = A \cdot A^k = (P\Lambda P^{-1})(P\Lambda^k P^{-1}) = P\Lambda(P^{-1}P)\Lambda^k P^{-1} = P\Lambda^{k+1}P^{-1}$$

（$P^{-1}P=I$ を使いました）。よってすべての自然数 $k$ で成り立ちます。$\blacksquare$（$\Lambda$ は対角行列なので $\Lambda^k$ は対角成分を $k$ 乗するだけで計算できます。）

Googleのページランクアルゴリズム、量子力学のエネルギー準位、主成分分析など、固有値は科学・工学の中心にあります。

---

## トレースと行列式

**命題**：$n\times n$ 行列 $A$ の固有値（重複度を含めて）を $\lambda_1, \ldots, \lambda_n$ とすると、

$$\mathrm{tr}(A) = \sum_i \lambda_i, \quad \det(A) = \prod_i \lambda_i$$

**証明**：固有多項式 $p(\lambda) = \det(A-\lambda I)$ は、複素数の範囲まで根を認めれば重複度を込めてちょうど $n$ 個の根 $\lambda_1,\ldots,\lambda_n$ を持つので、最高次係数に注意すると次のように因数分解できます。

$$p(\lambda) = (-1)^n(\lambda-\lambda_1)(\lambda-\lambda_2)\cdots(\lambda-\lambda_n)$$

*定数項の比較*：$\lambda=0$ を代入すると $p(0)=\det(A) = (-1)^n(-\lambda_1)(-\lambda_2)\cdots(-\lambda_n) = (-1)^n(-1)^n\prod_i\lambda_i = \prod_i \lambda_i$。

*$\lambda^{n-1}$ の係数の比較*：右辺を展開したときの $\lambda^{n-1}$ の係数は $(-1)^n \times (-1)^{n-1}\sum_i\lambda_i = (-1)^{2n-1}\sum_i \lambda_i = -\sum_i\lambda_i$。一方、$\det(A-\lambda I)$ を行列式の定義（余因子展開）から直接調べると、$\lambda^{n-1}$ の項は対角成分の積 $\prod_i(a_{ii}-\lambda)$ からしか出てこず、その係数は $-\sum_i a_{ii} = -\mathrm{tr}(A)$ になります。両者を比較すると $\mathrm{tr}(A) = \sum_i \lambda_i$。$\blacksquare$

---

## まとめ

固有ベクトルは行列を掛けても方向が変わらない特別なベクトルで、対応する倍率が固有値です。固有方程式が非自明解を持つ条件が線形写像の単射性の議論から$\det(A-\lambda I)=0$と同値であることが証明でき、相異なる固有値に対応する固有ベクトルは線形独立であることも証明できるので、そのとき対角化が可能になり、行列のべき乗の計算が劇的に簡単になります。トレース・行列式はそれぞれ固有値の総和・総積に一致することも、固有多項式の係数比較から証明できます。

---

## 関連ページ

- [行列](matrices.md)
