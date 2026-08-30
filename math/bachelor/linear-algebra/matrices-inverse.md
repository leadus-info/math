---
title: 逆行列
description: "行列による変換を打ち消す逆行列の意味と2次行列の公式を理解し、余因子展開と交代性から余因子行列と行列式・単位行列の関係を証明して余因子行列による逆行列の公式を導き、掃き出し法や連立方程式を解く手段としての利用を扱う"
goal: "逆行列の意味を理解し、余因子行列による逆行列の公式を証明し、掃き出し法で逆行列を求めて連立方程式を解く手段として使えるようになる"
tags: [math, linear-algebra, matrices]
stage: bachelor
subject: 線形代数
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 逆行列
    path: matrices-inverse.md
requires:
  - title: 行列式
    path: matrices-determinant.md
---

## 逆行列の定義

$AB = BA = I$（単位行列）を満たす $B$ を $A^{-1}$（逆行列）といいます。

$$\begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1} = \frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$$

連立方程式 $A\boldsymbol{x} = \boldsymbol{b}$ は、$\det(A) \neq 0$ のとき $\boldsymbol{x} = A^{-1}\boldsymbol{b}$ で解けます。

---

## n次正方行列の逆行列：余因子行列

行列式の余因子 $A_{ij}$ を並べた行列の転置を**余因子行列**（**随伴行列**）といいます。

$$\mathrm{adj}(A) = \begin{pmatrix}A_{11} & A_{21} & \cdots \\ A_{12} & A_{22} & \cdots \\ \vdots & & \ddots\end{pmatrix}$$

**定理**：$\det(A) \neq 0$ ならば $A^{-1} = \dfrac{1}{\det(A)}\,\mathrm{adj}(A)$。

**証明**：$A \cdot \mathrm{adj}(A) = \det(A)\, I$ を示せば、両辺を $\det(A)$（$\neq 0$）で割ることで定理が従います。積 $A \cdot \mathrm{adj}(A)$ の $(i,k)$ 成分は、行列の積の定義より

$$\bigl(A \cdot \mathrm{adj}(A)\bigr)_{ik} = \sum_{j=1}^n a_{ij} A_{kj}$$

$i=k$ のとき、これは $A$ の第 $i$ 行に関する余因子展開（行列式の記事で定義済み）そのものなので $\det(A)$ に一致します。

$i \neq k$ のときは、$A$ の第 $k$ 行を第 $i$ 行で置き換えた行列 $A'$（同じ行が2つある行列）を考えます。

余因子 $A_{kj}$ や $A'_{kj}$ は、第 $k$ 行と第 $j$ 列を除いた小行列式に符号 $(-1)^{k+j}$ を掛けたものとして定義されます。小行列式とは、行列から指定した行と列を取り除いてできる小さい行列の行列式のことです。符号は $k,j$ のみで決まり、小行列式も第 $k$ 行を除いて計算するため、この定義は第 $k$ 行そのものの中身にはよりません。よって、$A'$ が第 $k$ 行以外は $A$ と完全に一致することから $A'_{kj}=A_{kj}$ が成り立ちます。また置き換えにより $A'$ の第 $k$ 行は $A$ の第 $i$ 行と同じ、すなわち $a'_{kj}=a_{ij}$ です。

よって $A'$ の第 $k$ 行に関する余因子展開 $\sum_j a'_{kj}A'_{kj}$ は $\sum_j a_{ij}A_{kj}$、つまり上で求めた成分の式にちょうど一致します。交代性（行列式の記事）より、同じ行が2つある行列の行列式は $0$ なので、この成分は $0$ になります。

まとめると $\bigl(A\cdot\mathrm{adj}(A)\bigr)_{ik} = \det(A)$（$i=k$）、$0$（$i\neq k$）となり、これはちょうど $\det(A)\,I$ の成分と一致します。よって $A\cdot\mathrm{adj}(A) = \det(A)\,I$、すなわち $A^{-1} = \dfrac{1}{\det(A)}\mathrm{adj}(A)$。$\blacksquare$

（$2$ 次の場合、この公式は $\dfrac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$ に一致します。）余因子の計算量が $n$ が大きくなると急激に増えるため、実際の計算では次の**掃き出し法**がよく使われます。

**掃き出し法**：$(A \mid I)$ という $n \times 2n$ 行列を作り、行基本変形（行の入れ替え・定数倍・他の行への加算）を繰り返して左半分を単位行列 $I$ にすると、右半分が $A^{-1}$ になります。

**例題**：$A=\begin{pmatrix}2&1\\1&1\end{pmatrix}$ の逆行列を掃き出し法で求める。

$$\left(\begin{array}{cc|cc}2&1&1&0\\1&1&0&1\end{array}\right) \xrightarrow{R_1\leftrightarrow R_2} \left(\begin{array}{cc|cc}1&1&0&1\\2&1&1&0\end{array}\right) \xrightarrow{R_2-2R_1} \left(\begin{array}{cc|cc}1&1&0&1\\0&-1&1&-2\end{array}\right) \xrightarrow{R_1+R_2,\ -R_2} \left(\begin{array}{cc|cc}1&0&1&-1\\0&1&-1&2\end{array}\right)$$

よって $A^{-1}=\begin{pmatrix}1&-1\\-1&2\end{pmatrix}$。$\det(A)=2\times1-1\times1=1$ なので、逆行列の公式 $\dfrac{1}{\det(A)}\begin{pmatrix}1&-1\\-1&2\end{pmatrix}$ と一致することも確認できます。

---

## まとめ

逆行列は、掛けると単位行列になる「変換を打ち消す」行列です。行列式が0でないときにのみ存在し、$A\cdot\mathrm{adj}(A)=\det(A)I$ を余因子展開と交代性から証明することで、余因子行列を使った公式が導けます。実用上は掃き出し法で求めることが多く、連立方程式を解く手段としても使えます。

---

## 関連ページ

- [固有値](eigenvalues.md)
