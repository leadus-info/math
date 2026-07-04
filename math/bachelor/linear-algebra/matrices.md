---
title: 行列
description: "数を格子状に並べた構造——演算・行列式・逆行列"
goal: "行列の積・行列式・逆行列を定義から計算し、行列を連立方程式の表現と線形変換の両面から理解できるようになる"
tags: [math, linear-algebra, matrices]
stage: 発展編
subject: 線形代数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 発展編
    path: /math/bachelor/index.md
  - title: 行列
    path: /math/bachelor/linear-algebra/matrices.md
requires:
  - title: ベクトル
    path: vectors.md
  - title: 等号・等式
    path: /math/intermediate/algebra/equations.md
---

## 数を格子状に並べる

$$\begin{pmatrix} 2 & 1 \\ 1 & -1 \end{pmatrix}$$

こんな「数の表」が**行列**です。横の並びを「行」、縦の並びを「列」と呼びます。連立方程式

$$\begin{cases} 2x + y = 5 \\ x - y = 1 \end{cases}$$

の係数を取り出すと $\begin{pmatrix} 2 & 1 \\ 1 & -1 \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 5 \\ 1 \end{pmatrix}$ と書けます。2本でも100本でも同じ形で書けるのが行列の強みです。行列はまた、ベクトルを「変換する操作」とも読め、回転・拡大縮小・反転がすべて行列で統一的に表せます。

---

## 行列の定義と基本演算

$m$ 行 $n$ 列の行列は数を $m \times n$ の格子に並べたもので、$(i, j)$ 成分を $a_{ij}$ と書きます。

**加法**（同じサイズ同士）：成分ごとに足します。

**スカラー倍**：すべての成分に定数を掛けます。

---

## 行列の積

$(m \times n)$ 行列 $A$ と $(n \times p)$ 行列 $B$ の積 $AB$ は $(m \times p)$ 行列で、

$$(AB)_{ij} = \sum_{k=1}^n a_{ik} b_{kj}$$

「$A$ の $i$ 行ベクトルと $B$ の $j$ 列ベクトルの内積」です。一般に $AB \neq BA$（掛け算の順序は変えられません）——「先に回転してから拡大」と「先に拡大してから回転」が違う結果になるのと同じです。

**例**：$\begin{pmatrix}1&2\\3&4\end{pmatrix}\begin{pmatrix}5\\6\end{pmatrix} = \begin{pmatrix}17\\39\end{pmatrix}$

---

## 行列式

正方行列 $A$ の**行列式** $\det(A)$：

$$\det\begin{pmatrix}a&b\\c&d\end{pmatrix} = ad - bc$$

**幾何学的意味**：$A$ が表す変換で面積が $|\det(A)|$ 倍になる（符号は向きの反転を表す）。$\det(A) = 0 \iff$ 逆行列が存在しない（変換が次元を下げる）。

---

## 逆行列

$AB = BA = I$（単位行列）を満たす $B$ を $A^{-1}$（逆行列）といいます。

$$\begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1} = \frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$$

連立方程式 $A\boldsymbol{x} = \boldsymbol{b}$ は、$\det(A) \neq 0$ のとき $\boldsymbol{x} = A^{-1}\boldsymbol{b}$ で解けます。

---

## まとめ

行列は「数を格子状に並べた構造」で、連立方程式をひとつの式で表す道具であると同時に、ベクトルを変換する操作でもあります。行列の積は一般に非可換で、行列式は変換による面積・体積の拡大率、逆行列は変換を打ち消す操作として理解できます。

---

## 関連ページ

- [ベクトル（発展編）](vectors.md)
- [固有値（発展編）](/math/bachelor/linear-algebra/eigenvalues.md)
