---
title: 固有値
description: "行列を掛けても方向が変わらないベクトル"
goal: "固有値・固有ベクトルを固有多項式から計算し、対角化可能かどうかを判定して行列のべき乗を簡単化できるようになる"
tags: [math, linear-algebra, eigenvalues]
stage: 発展編
subject: 線形代数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 発展編
    path: /math/bachelor/index.md
  - title: 固有値
    path: /math/bachelor/linear-algebra/eigenvalues.md
requires:
  - title: 線形写像
    path: /math/bachelor/linear-algebra/linear-maps.md
  - title: 多項式
    path: /math/advanced/algebra/polynomials.md
---

## 方向が変わらないベクトル

行列を掛けると、普通はベクトルの方向が変わります。しかしある特別なベクトルは、行列を掛けても方向が変わらず、大きさだけが変わります。鏡の変換（$y$ 軸に関する反射）を考えると、$x$ 軸方向 $(1,0)$ は $(-1,0)$（$-1$倍）に、$y$ 軸方向 $(0,1)$ は $(0,1)$（$1$倍）のままです。

---

## 固有値の定義

正方行列 $A$ に対して $A\boldsymbol{v} = \lambda\boldsymbol{v}$（$\boldsymbol{v} \neq \boldsymbol{0}$）を満たすとき、$\lambda$ を**固有値**、$\boldsymbol{v}$ を固有値 $\lambda$ に対応する**固有ベクトル**といいます。

$(A - \lambda I)\boldsymbol{v} = \boldsymbol{0}$ が非自明解を持つ条件は $\det(A - \lambda I) = 0$ です。

---

## 固有多項式と固有値・固有ベクトルの求め方

$p(\lambda) = \det(A - \lambda I)$ を**固有多項式**といいます。$n \times n$ 行列の固有多項式は $\lambda$ の $n$ 次多項式で、固有値は $p(\lambda) = 0$ の根です。

**例**：$A = \begin{pmatrix}3&1\\0&2\end{pmatrix}$ のとき $\det(A - \lambda I) = (3-\lambda)(2-\lambda) = 0$ より $\lambda = 3$ または $\lambda = 2$。

固有値が決まったら $(A - \lambda I)\boldsymbol{v} = \boldsymbol{0}$ を解いて固有ベクトルを求めます。$\lambda = 3$ のとき $(A-3I)\boldsymbol{v} = \begin{pmatrix}0&1\\0&-1\end{pmatrix}\boldsymbol{v}=\boldsymbol{0}$ より $v_2=0$、固有ベクトルは $c\begin{pmatrix}1\\0\end{pmatrix}$。$\lambda=2$ のとき $v_1+v_2=0$ より固有ベクトルは $c\begin{pmatrix}1\\-1\end{pmatrix}$。

---

## 対角化

$n$ 個の線形独立な固有ベクトル $\boldsymbol{v}_1, \ldots, \boldsymbol{v}_n$ が存在するとき $A$ は**対角化可能**です。

$$A = P\Lambda P^{-1}, \quad P = (\boldsymbol{v}_1 \cdots \boldsymbol{v}_n), \quad \Lambda = \mathrm{diag}(\lambda_1, \ldots, \lambda_n)$$

**対角化可能の十分条件**：$n$ 個の相異なる固有値を持つ。

対角化のメリットは、行列の累乗が簡単になることです。$A^{100}\boldsymbol{v}$ を直接計算するのは大変ですが、$\boldsymbol{v}$ が固有ベクトルなら $A^{100}\boldsymbol{v} = \lambda^{100}\boldsymbol{v}$ で済みます。一般に

$$A^k = P\Lambda^k P^{-1}$$

（$\Lambda^k$ は対角成分を $k$ 乗するだけ）。Googleのページランクアルゴリズム、量子力学のエネルギー準位、主成分分析など、固有値は科学・工学の中心にあります。

---

## トレースと行列式

固有値 $\lambda_1, \ldots, \lambda_n$ と行列の関係：

$$\mathrm{tr}(A) = \sum_i \lambda_i, \quad \det(A) = \prod_i \lambda_i$$

---

## まとめ

固有ベクトルは行列を掛けても方向が変わらない特別なベクトルで、対応する倍率が固有値です。固有多項式 $\det(A-\lambda I)=0$ を解けば固有値が求まり、線形独立な固有ベクトルが十分にあれば対角化ができ、行列のべき乗の計算が劇的に簡単になります。

---

## 関連ページ

- [行列（発展編）](matrices.md)
- [線形写像（発展編）](linear-maps.md)
