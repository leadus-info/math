---
title: 固有値
description: "固有値・固有ベクトルの計算と対角化"
goal: "固有多項式から固有値を求め、固有ベクトルを計算し、対角化可能かどうかを判定できるようになる"
tags: [math,linear-algebra,eigenvalues]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 線形代数
    path: /math/linear-algebra/index.md
  - title: 固有値
    path: /math/linear-algebra/eigenvalues/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 固有値（入門）
    path: /math/linear-algebra/eigenvalues/introduction.md
  - title: 行列（標準）
    path: /math/linear-algebra/matrices/standard.md
  - title: 多項式（標準）
    path: /math/algebra/polynomials/standard.md
---

## 固有値の定義

正方行列 $A$ に対して $A\boldsymbol{v} = \lambda\boldsymbol{v}$（$\boldsymbol{v} \neq \boldsymbol{0}$）を満たすとき、$\lambda$ を**固有値**、$\boldsymbol{v}$ を固有値 $\lambda$ に対応する**固有ベクトル**といいます。

$(A - \lambda I)\boldsymbol{v} = \boldsymbol{0}$ が非自明解を持つ条件は $\det(A - \lambda I) = 0$。

---

## 固有多項式と固有値の求め方

$p(\lambda) = \det(A - \lambda I)$ を**固有多項式**といいます。$n \times n$ 行列の固有多項式は $\lambda$ の $n$ 次多項式です。

固有値は $p(\lambda) = 0$ の根です。

**例**：$A = \begin{pmatrix}3&1\\0&2\end{pmatrix}$ のとき

$\det(A - \lambda I) = (3-\lambda)(2-\lambda) = 0$ より $\lambda = 3$ または $\lambda = 2$。

---

## 固有ベクトルの求め方

固有値 $\lambda$ が決まったら $(A - \lambda I)\boldsymbol{v} = \boldsymbol{0}$ を解きます。

上の例で $\lambda = 3$ のとき：$(A - 3I)\boldsymbol{v} = \begin{pmatrix}0&1\\0&-1\end{pmatrix}\boldsymbol{v} = \boldsymbol{0}$より $v_2 = 0$。固有ベクトルは $\boldsymbol{v} = c\begin{pmatrix}1\\0\end{pmatrix}$（$c \neq 0$）。

$\lambda = 2$ のとき：$(A-2I)\boldsymbol{v} = \begin{pmatrix}1&1\\0&0\end{pmatrix}\boldsymbol{v} = \boldsymbol{0}$より $v_1 + v_2 = 0$。固有ベクトルは $\boldsymbol{v} = c\begin{pmatrix}1\\-1\end{pmatrix}$。

---

## 対角化

$n$ 個の線形独立な固有ベクトル $\boldsymbol{v}_1, \ldots, \boldsymbol{v}_n$ が存在するとき $A$ は**対角化可能**です。

$$A = P\Lambda P^{-1}, \quad P = (\boldsymbol{v}_1 \cdots \boldsymbol{v}_n), \quad \Lambda = \mathrm{diag}(\lambda_1, \ldots, \lambda_n)$$

対角化のメリット：$A^k = P\Lambda^k P^{-1}$（$\Lambda^k$ は対角成分を $k$ 乗するだけ）。

**対角化可能の十分条件**：$n$ 個の相異なる固有値を持つ。

---

## トレースと行列式

固有値 $\lambda_1, \ldots, \lambda_n$ と行列の関係：

$$\mathrm{tr}(A) = \sum_i \lambda_i, \quad \det(A) = \prod_i \lambda_i$$

---

## 関連ページ

- [行列（標準）](../matrices/standard.md)
- [線形写像（標準）](../linear-maps/standard.md)
- [固有値（専門）](professional.md)
