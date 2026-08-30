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

前提記事「行列」で見た、行列がベクトルを変換する操作(行列とベクトルの積)を思い出してください。行列どうしの積 $AB$ は、この変換を2回続けて施す操作、すなわち変換の合成に対応します。

変換の合成とは、ある変換を施した結果に対してさらに別の変換を施す操作のことです。

**命題**：任意の $p$ 次元ベクトル $\boldsymbol{x}$ について、$(AB)\boldsymbol{x} = A(B\boldsymbol{x})$ が成り立つ。

**証明**：

$$((AB)\boldsymbol{x})_i = \sum_{j=1}^p (AB)_{ij} x_j = \sum_{j=1}^p \sum_{k=1}^n a_{ik} b_{kj} x_j = \sum_{k=1}^n a_{ik} \sum_{j=1}^p b_{kj} x_j = \sum_{k=1}^n a_{ik} (B\boldsymbol{x})_k = (A(B\boldsymbol{x}))_i$$

（2つ目の等号で $AB$ の定義式を代入し、3つ目の等号で和の順序を交換して $a_{ik}$ を $j$ についての和の外にくくり出し、4つ目の等号で内側の和が $B\boldsymbol{x}$ の第 $k$ 成分であることを使っています）。$\blacksquare$

この対応により、一般に $AB \neq BA$（掛け算の順序は変えられません）——「先に回転してからx軸方向にだけ拡大」と「先にx軸方向にだけ拡大してから回転」が違う結果になるのと同じです。全方向を同じ倍率で拡大するだけなら、方向を特別扱いしない変換なので、先にかけても後にかけても結果は同じです。x軸方向にだけ拡大するというように方向ごとに倍率が異なる場合は、回転の向きによって扱いが変わるため、順序を入れ替えると結果も変わってしまいます。

**例**：$\begin{pmatrix}1&2\\3&4\end{pmatrix}\begin{pmatrix}5\\6\end{pmatrix} = \begin{pmatrix}17\\39\end{pmatrix}$

**例（$AB\neq BA$の確認）**：$A=\begin{pmatrix}1&1\\0&1\end{pmatrix}$、$B=\begin{pmatrix}1&0\\1&1\end{pmatrix}$ とすると、

$$AB=\begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}1&0\\1&1\end{pmatrix}=\begin{pmatrix}2&1\\1&1\end{pmatrix}, \qquad BA=\begin{pmatrix}1&0\\1&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}1&1\\1&2\end{pmatrix}$$

$AB\neq BA$ であることが具体的に確認できます。

---

## 単位行列と結合律

行列の積には、実数の掛け算における $1$ に相当する特別な行列が存在します。行の数と列の数が等しい行列を**正方行列**といいます。

正方行列で、左上から右下に並ぶ成分($(1,1)$成分、$(2,2)$成分、…)を**対角成分**といいます。**単位行列**とは、対角成分がすべて $1$ で、それ以外の成分がすべて $0$ である正方行列のことで、$I$ と表します。例えば $2$ 次の単位行列は $I=\begin{pmatrix}1&0\\0&1\end{pmatrix}$ です。

**定理**：$n$ 次正方行列 $A$ と $n$ 次単位行列 $I$ について、$AI = IA = A$ が成り立つ。

**証明**：$I$ の $(k,j)$ 成分は $k=j$ のとき $1$、それ以外は $0$ なので、

$$(AI)_{ij} = \sum_{k=1}^n a_{ik} I_{kj} = a_{ij}$$

（和の中で $k=j$ の項だけが残るため）となります。$IA=A$ も同様に示せます。$\blacksquare$

例えば、

$$\begin{pmatrix}1&2\\3&4\end{pmatrix}\begin{pmatrix}1&0\\0&1\end{pmatrix}=\begin{pmatrix}1&0\\0&1\end{pmatrix}\begin{pmatrix}1&2\\3&4\end{pmatrix}=\begin{pmatrix}1&2\\3&4\end{pmatrix}$$

のように、単位行列との積は元の行列を変えません。

**定理（結合律）**：$(AB)C = A(BC)$ が成り立つ（一方で非可換性のため、積の順序 $AB$ と $BA$ を入れ替えることはできない）。

**証明**：$A$ を $(m\times n)$、$B$ を $(n\times p)$、$C$ を $(p\times q)$ 行列とすると、

$$((AB)C)_{il} = \sum_{j=1}^p (AB)_{ij} c_{jl} = \sum_{j=1}^p \sum_{k=1}^n a_{ik} b_{kj} c_{jl} = \sum_{k=1}^n a_{ik} \sum_{j=1}^p b_{kj} c_{jl} = \sum_{k=1}^n a_{ik} (BC)_{kl} = (A(BC))_{il}$$

（2つ目の等号で $AB$ の定義式を代入し、3つ目の等号で和の順序を交換し、4つ目の等号で内側の和が $BC$ の第 $(k,l)$ 成分であることを使っています）。$\blacksquare$

具体例で確認すると、先ほどの $A=\begin{pmatrix}1&1\\0&1\end{pmatrix}$、$B=\begin{pmatrix}1&0\\1&1\end{pmatrix}$ に加えて $C=\begin{pmatrix}2&0\\0&1\end{pmatrix}$ とすると、

$$BC=\begin{pmatrix}1&0\\1&1\end{pmatrix}\begin{pmatrix}2&0\\0&1\end{pmatrix}=\begin{pmatrix}2&0\\2&1\end{pmatrix}$$

であり、

$$(AB)C=\begin{pmatrix}2&1\\1&1\end{pmatrix}\begin{pmatrix}2&0\\0&1\end{pmatrix}=\begin{pmatrix}4&1\\2&1\end{pmatrix}, \qquad A(BC)=\begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}2&0\\2&1\end{pmatrix}=\begin{pmatrix}4&1\\2&1\end{pmatrix}$$

のように、$C$ をかける順序（先に $AB$ を計算してから $C$ をかけるか、先に $BC$ を計算してから $A$ をかけるか）を変えても結果は一致します。

---

## まとめ

行列の積は、行ベクトルと列ベクトルの内積を並べたものとして定義され、一般に交換法則が成り立ちません。単位行列を持ち、結合律 $(AB)C=A(BC)$ を満たします。

---

## 関連ページ

- [行列式](matrices-determinant.md)
