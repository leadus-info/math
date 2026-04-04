---
title: 行列
description: "数を格子状に並べた構造"
tags: [math,linear-algebra,matrices]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 線形代数
    path: /math/linear-algebra/index.html
  - title: 行列
    path: /math/linear-algebra/matrices/standard.html
levels:
  - level: 入門
    path: introduction.html
  - level: 標準
  - level: 専門
    path: professional.html
level: 標準
requires:
  - title: ベクトル
    path: /math/linear-algebra/vectors/introduction
  - title: 等号・等式
    path: /math/math-language/equations/introduction
---

## 行列の定義

数を格子状に並べたものが行列です。
ベクトルの変換や連立方程式を統一的に扱えます。

$m$ 行 $n$ 列の**行列**は $mn$ 個の数を $m \times n$ の格子状に並べたものです。

$$A = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix} \quad \text{（2行3列の行列）}$$

$i$ 行 $j$ 列の成分を $a_{ij}$ と書きます。

---

## 基本演算

**足し算**：同じサイズの行列どうし、成分ごとに足します。

$$\begin{pmatrix}1&2\\3&4\end{pmatrix} + \begin{pmatrix}5&6\\7&8\end{pmatrix} = \begin{pmatrix}6&8\\10&12\end{pmatrix}$$

**スカラー倍**：すべての成分に定数を掛けます。

---

## 行列の積

$(m \times n)$ 行列 $A$ と $(n \times p)$ 行列 $B$ の積 $AB$ は $(m \times p)$ 行列で、

$$(AB)_{ij} = \sum_{k=1}^n a_{ik} b_{kj}$$

つまり「$A$ の $i$ 行と $B$ の $j$ 列の内積」です。

例：

$$\begin{pmatrix}1&2\\3&4\end{pmatrix}\begin{pmatrix}5\\6\end{pmatrix} = \begin{pmatrix}1 \cdot 5 + 2 \cdot 6\\3 \cdot 5 + 4 \cdot 6\end{pmatrix} = \begin{pmatrix}17\\39\end{pmatrix}$$

**重要**：一般に $AB \neq BA$（掛け算の順序は交換できない）。

---

## 連立方程式と行列

$$\begin{cases}2x + y = 5 \\ x - y = 1\end{cases}$$

は行列を使って $A\boldsymbol{x} = \boldsymbol{b}$ と書けます：

$$\begin{pmatrix}2&1\\1&-1\end{pmatrix}\begin{pmatrix}x\\y\end{pmatrix} = \begin{pmatrix}5\\1\end{pmatrix}$$

逆行列 $A^{-1}$ が存在すれば $\boldsymbol{x} = A^{-1}\boldsymbol{b}$ で解けます。

---

## 逆行列

$AB = BA = I$（**単位行列**）を満たす $B$ を $A$ の**逆行列** $A^{-1}$ といいます。

単位行列 $I$ は対角成分が 1、それ以外が 0 の行列です：$I = \begin{pmatrix}1&0\\0&1\end{pmatrix}$

2次正方行列の逆行列：

$$\begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1} = \frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$$

$ad - bc = 0$ のとき逆行列は存在しません（この値を**行列式**といいます）。

---

## 行列式

正方行列 $A$ に対して**行列式** $\det(A)$ が定まります。

$$\det\begin{pmatrix}a&b\\c&d\end{pmatrix} = ad - bc$$

行列式の幾何学的な意味：「行列 $A$ が表す線形変換で面積が何倍になるか」。
$\det(A) = 0$ のとき変換は次元を下げる（逆変換が存在しない）。

---

## 関連ページ

- [ベクトル](../vectors/introduction.md)
- [等号・等式](../../math-language/equations/introduction.md)
