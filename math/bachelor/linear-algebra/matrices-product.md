---
title: 行列の積
description: "行ベクトルと列ベクトルの内積を並べる行列の積の定義と具体的な計算方法を扱い、一般に交換法則が成り立たないことも解説する"
goal: "行列の積の定義を理解し、計算できるようになる"
tags: [math, linear-algebra, matrices]
stage: bachelor
subject: 線形代数
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 行列の積
    path: matrices-product.md
requires:
  - title: 行列
    path: matrices.md
---

## 行列の積の定義

$(m \times n)$ 行列 $A$ と $(n \times p)$ 行列 $B$ の積 $AB$ は $(m \times p)$ 行列で、

$$(AB)_{ij} = \sum_{k=1}^n a_{ik} b_{kj}$$

「$A$ の $i$ 行ベクトルと $B$ の $j$ 列ベクトルの内積」です。一般に $AB \neq BA$（掛け算の順序は変えられません）——「先に回転してから拡大」と「先に拡大してから回転」が違う結果になるのと同じです。

**例**：$\begin{pmatrix}1&2\\3&4\end{pmatrix}\begin{pmatrix}5\\6\end{pmatrix} = \begin{pmatrix}17\\39\end{pmatrix}$

---

## まとめ

行列の積は、行ベクトルと列ベクトルの内積を並べたものとして定義され、一般に交換法則が成り立ちません。

---

## 関連ページ

- [行列式（発展編）](matrices-determinant.md)
