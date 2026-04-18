---
title: 行列
description: "行列の演算・行列式・逆行列・固有値"
goal: "行列の積・行列式・逆行列を計算し、固有値・固有ベクトルの意味と求め方を説明できるようになる"
tags: [math,linear-algebra,matrices]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 線形代数
    path: /math/linear-algebra/index.md
  - title: 行列
    path: /math/linear-algebra/matrices/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 行列（入門）
    path: /math/linear-algebra/matrices/introduction.md
  - title: ベクトル（標準）
    path: /math/linear-algebra/vectors/standard.md
---

## 行列の定義と基本演算

$m$ 行 $n$ 列の行列は数を $m \times n$ の格子に並べたものです。$(i, j)$ 成分を $a_{ij}$ と書きます。

**加法**（同じサイズ同士）：成分ごとに足します。

**スカラー倍**：すべての成分に定数を掛けます。

---

## 行列の積

$(m \times n)$ 行列 $A$ と $(n \times p)$ 行列 $B$ の積 $AB$ は $(m \times p)$ 行列で：

$$(AB)_{ij} = \sum_{k=1}^n a_{ik} b_{kj}$$

「$A$ の $i$ 行ベクトルと $B$ の $j$ 列ベクトルの内積」です。

**重要**：一般に $AB \neq BA$（掛け算の順序は変えられない）。

**例**：

$$\begin{pmatrix}1&2\\3&4\end{pmatrix}\begin{pmatrix}5\\6\end{pmatrix} = \begin{pmatrix}17\\39\end{pmatrix}$$

---

## 行列式

正方行列 $A$ の**行列式** $\det(A)$：

$$\det\begin{pmatrix}a&b\\c&d\end{pmatrix} = ad - bc$$

**幾何学的意味**：$A$ が表す変換で面積が $|\det(A)|$ 倍になる（符号は向きを表す）。

$\det(A) = 0 \iff$ 逆行列が存在しない（変換が次元を下げる）。

---

## 逆行列

$AB = BA = I$（単位行列）を満たす $B$ を $A^{-1}$（逆行列）といいます。

2次行列の逆行列：

$$\begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1} = \frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$$

連立方程式 $A\boldsymbol{x} = \boldsymbol{b}$ は $\det(A) \neq 0$ のとき $\boldsymbol{x} = A^{-1}\boldsymbol{b}$ で解けます。

---

## 固有値と固有ベクトル

$A\boldsymbol{v} = \lambda \boldsymbol{v}$（$\boldsymbol{v} \neq \boldsymbol{0}$）を満たす $\lambda$ を**固有値**、$\boldsymbol{v}$ を**固有ベクトル**といいます。

「$A$ を掛けても方向が変わらないベクトル」で、大きさだけが $\lambda$ 倍になります。

**固有多項式**：$\det(A - \lambda I) = 0$ を解いて固有値を求めます。

**例題**：$A = \begin{pmatrix}3&1\\0&2\end{pmatrix}$

$\det(A - \lambda I) = (3-\lambda)(2-\lambda) = 0$ より $\lambda = 3$ または $\lambda = 2$。

---

## 関連ページ

- [ベクトル（標準）](../vectors/standard.md)
- [行列（専門）](professional.md)
