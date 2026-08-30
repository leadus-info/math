---
title: 行列の積
description: "行ベクトルと列ベクトルの内積を並べる行列の積の定義と具体的な計算方法を扱い、単位行列・結合律とともに、一般に交換法則が成り立たないことも解説する"
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

$$(AB)_{ij} = \sum_{k=1}^n a_{ik} b_{kj} \qquad (i=1,\dots,m,\ j=1,\dots,p)$$

「$A$ の $i$ 行ベクトルと $B$ の $j$ 列ベクトルの内積」です。

前提記事「行列」で見た、行列がベクトルを変換する操作(行列とベクトルの積)を思い出してください。行列どうしの積 $AB$ は、この変換を2回続けて施す操作、すなわち変換の合成に対応します。変換の合成とは、ある変換を施した結果に対してさらに別の変換を施す操作のことです。実際、$p$ 次元ベクトル $x$ について

$$((AB)x)_i = \sum_{j=1}^p (AB)_{ij} x_j = \sum_{j=1}^p \sum_{k=1}^n a_{ik} b_{kj} x_j = \sum_{k=1}^n a_{ik} \sum_{j=1}^p b_{kj} x_j = \sum_{k=1}^n a_{ik} (Bx)_k = (A(Bx))_i$$

が成り立つので、$(AB)x = A(Bx)$ です。

この対応により、一般に $AB \neq BA$（掛け算の順序は変えられません）——「先に回転してから拡大」と「先に拡大してから回転」が違う結果になるのと同じです。

**例**：$\begin{pmatrix}1&2\\3&4\end{pmatrix}\begin{pmatrix}5\\6\end{pmatrix} = \begin{pmatrix}17\\39\end{pmatrix}$

**例（$AB\neq BA$の確認）**：$A=\begin{pmatrix}1&1\\0&1\end{pmatrix}$、$B=\begin{pmatrix}1&0\\1&1\end{pmatrix}$ とすると、

$$AB=\begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}1&0\\1&1\end{pmatrix}=\begin{pmatrix}2&1\\1&1\end{pmatrix}, \qquad BA=\begin{pmatrix}1&0\\1&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}1&1\\1&2\end{pmatrix}$$

$AB\neq BA$ であることが具体的に確認できます。

---

## 単位行列と結合律

行列の積には、実数の掛け算における $1$ に相当する特別な行列が存在します。**単位行列**とは、対角成分がすべて $1$ で、それ以外の成分がすべて $0$ である正方行列のことで、$I$ と表します。例えば $2$ 次の単位行列は $I=\begin{pmatrix}1&0\\0&1\end{pmatrix}$ です。

$n$ 次正方行列 $A$ と $n$ 次単位行列 $I$ について、$AI = IA = A$ が成り立ちます。例えば、

$$\begin{pmatrix}1&2\\3&4\end{pmatrix}\begin{pmatrix}1&0\\0&1\end{pmatrix}=\begin{pmatrix}1&0\\0&1\end{pmatrix}\begin{pmatrix}1&2\\3&4\end{pmatrix}=\begin{pmatrix}1&2\\3&4\end{pmatrix}$$

のように、単位行列との積は元の行列を変えません。

また、行列の積では**結合律** $(AB)C = A(BC)$ が成り立ちます（一方で非可換性のため、積の順序 $AB$ と $BA$ を入れ替えることはできません）。先ほどの $A=\begin{pmatrix}1&1\\0&1\end{pmatrix}$、$B=\begin{pmatrix}1&0\\1&1\end{pmatrix}$ に加えて $C=\begin{pmatrix}2&0\\0&1\end{pmatrix}$ とすると、

$$(AB)C=\begin{pmatrix}2&1\\1&1\end{pmatrix}\begin{pmatrix}2&0\\0&1\end{pmatrix}=\begin{pmatrix}4&1\\2&1\end{pmatrix}, \qquad A(BC)=\begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}2&0\\2&1\end{pmatrix}=\begin{pmatrix}4&1\\2&1\end{pmatrix}$$

のように、$C$ をかける順序（先に $AB$ を計算してから $C$ をかけるか、先に $BC$ を計算してから $A$ をかけるか）を変えても結果は一致します。

---

## まとめ

行列の積は、行ベクトルと列ベクトルの内積を並べたものとして定義され、一般に交換法則が成り立ちません。

---

## 関連ページ

- [行列式](matrices-determinant.md)
