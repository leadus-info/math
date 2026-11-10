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

数の世界では、$3x=6$ を解くのに両辺を $3$ で割る、つまり $3$ の逆数 $\frac13$ を掛けます。行列でも、連立方程式 $A\boldsymbol{x}=\boldsymbol{b}$ を「割り算」のように解くために、逆数にあたる行列を考えます。

$n$ 次正方行列 $A$ に対し、

$$AB = BA = I \quad (I \text{ は } n \text{ 次の単位行列})$$

を満たす $n$ 次正方行列 $B$ が存在するとき、$A$ は**正則**（可逆）であるといい、$B$ を $A$ の**逆行列**といいます。

このような $B$ は1つしかありません。実際、$B$ と $C$ がどちらも条件を満たすとすると、

$$B = BI = B(AC) = (BA)C = IC = C$$

です。そこで、$A$ の逆行列を $A^{-1}$ という1つの記号で表します。

逆行列は、$A$ による変換を打ち消す行列です。ベクトル $\boldsymbol{x}$ に $A$ を掛けて変換したあと $A^{-1}$ を掛けると、$A^{-1}(A\boldsymbol{x}) = (A^{-1}A)\boldsymbol{x} = I\boldsymbol{x} = \boldsymbol{x}$ と元に戻ります。例えば $A$ が原点を中心とする $90^\circ$ 回転なら、$A^{-1}$ は逆向きの $90^\circ$ 回転です。

逆行列が存在すれば、$\det(A) \neq 0$ です。行列式の記事で示した $\det(AB)=\det(A)\det(B)$ と $\det(I)=1$ より、

$$\det(A)\det(A^{-1}) = \det(AA^{-1}) = \det(I) = 1$$

となるので、$\det(A)$ は $0$ になりえません。逆向き（$\det(A)\neq0$ なら逆行列が存在する）は、次の節で逆行列を具体的に作ることで示します。

---

## n次正方行列の逆行列：余因子行列

行列 $A$ の $(i,j)$ 成分を $(j,i)$ 成分の位置に置いた行列を、$A$ の**転置**といい、$A^\top$ と書きます。行列式の余因子 $A_{ij}$ を並べた行列の転置を**余因子行列**といい、$\mathrm{adj}(A)$ と書きます。

$$\mathrm{adj}(A) = \begin{pmatrix}A_{11} & A_{21} & \cdots \\ A_{12} & A_{22} & \cdots \\ \vdots & & \ddots\end{pmatrix}$$

**定理**：$\det(A) \neq 0$ ならば $A^{-1} = \dfrac{1}{\det(A)}\,\mathrm{adj}(A)$。

**証明**：逆行列の定義は $AB=BA=I$ なので、$A \cdot \mathrm{adj}(A) = \det(A)\, I$ と $\mathrm{adj}(A)\cdot A = \det(A)\, I$ の両方を示せば、両辺を $\det(A)$（$\neq 0$）で割ることで定理が従います。まず $A \cdot \mathrm{adj}(A) = \det(A)\, I$ を示します。積 $A \cdot \mathrm{adj}(A)$ の $(i,k)$ 成分は、行列の積の定義より

$$\bigl(A \cdot \mathrm{adj}(A)\bigr)_{ik} = \sum_{j=1}^n a_{ij} A_{kj}$$

$i=k$ のとき、これは $A$ の第 $i$ 行に関する余因子展開（行列式の記事で定義済み）そのものなので $\det(A)$ に一致します。

$i \neq k$ のときは、$A$ の第 $k$ 行を第 $i$ 行で置き換えた行列 $A'$（同じ行が2つある行列）を考えます。

余因子 $A_{kj}$ や $A'_{kj}$ は、第 $k$ 行と第 $j$ 列を除いた小行列式に符号 $(-1)^{k+j}$ を掛けたものとして定義されます。小行列式とは、行列から指定した行と列を取り除いてできる小さい行列の行列式のことです。符号 $(-1)^{k+j}$ は $k,j$ という位置のみで決まり、$A$ の中身には依存しません。また、小行列式も第 $k$ 行を除いて計算するため、その値も第 $k$ 行の中身を含みません。したがって、この小行列式の値は第 $k$ 行そのものの中身にはよりません。よって、$A'$ が第 $k$ 行以外は $A$ と完全に一致することから $A'_{kj}=A_{kj}$ が成り立ちます。また置き換えにより $A'$ の第 $k$ 行は $A$ の第 $i$ 行と同じ、すなわち $a'_{kj}=a_{ij}$ です。

よって、$a'_{kj}=a_{ij}$ と $A'_{kj}=A_{kj}$ を代入すると、$A'$ の第 $k$ 行に関する余因子展開は $\sum_j a'_{kj}A'_{kj} = \sum_j a_{ij}A_{kj}$ となり、これは上で求めた成分の式にちょうど一致します。交代性（行列式の記事）より、同じ行が2つある行列の行列式は $0$ なので、この成分は $0$ になります。

まとめると $\bigl(A\cdot\mathrm{adj}(A)\bigr)_{ik} = \det(A)$（$i=k$）、$0$（$i\neq k$）となり、これはちょうど $\det(A)\,I$ の成分と一致します。よって $A\cdot\mathrm{adj}(A) = \det(A)\,I$ です。

次に、逆向きの積 $\mathrm{adj}(A)\cdot A = \det(A)\,I$ を、転置を使って示します。

- 上で示した等式は任意の正方行列について成り立つので、$A^\top$ に当てはめると $A^\top\cdot\mathrm{adj}(A^\top) = \det(A^\top)\,I$ です。行列式の性質 $\det(A^\top)=\det(A)$（行列式の記事）より、右辺は $\det(A)\,I$ です。
- $A^\top$ の $(i,j)$ 余因子は、$A^\top$ から第 $i$ 行と第 $j$ 列を除いた小行列式から作ります。この小行列は、$A$ から第 $j$ 行と第 $i$ 列を除いた小行列の転置なので、再び $\det(A^\top)=\det(A)$ より、$A^\top$ の $(i,j)$ 余因子は $A$ の $(j,i)$ 余因子 $A_{ji}$ に等しくなります（符号 $(-1)^{i+j}$ も共通です）。したがって $\mathrm{adj}(A^\top)=\mathrm{adj}(A)^\top$ です。
- これらから $A^\top\cdot\mathrm{adj}(A)^\top = \det(A)\,I$ となります。両辺の転置をとります。一般に、積の転置は $((XY)^\top)_{ik}=(XY)_{ki}=\sum_j x_{kj}y_{ji}=\sum_j (Y^\top)_{ij}(X^\top)_{jk}$ より $(XY)^\top=Y^\top X^\top$ となるので、$\mathrm{adj}(A)\cdot A = \det(A)\,I$ が得られます。

以上で両側の等式がそろったので、$\det(A)\neq0$ のとき $B=\dfrac{1}{\det(A)}\mathrm{adj}(A)$ は $AB=BA=I$ を満たし、$A^{-1} = \dfrac{1}{\det(A)}\mathrm{adj}(A)$ です。$\blacksquare$

前の節の結果と合わせると、次のことがわかります。

$$A \text{ が正則（逆行列が存在する）} \iff \det(A) \neq 0$$

**2次の場合**：$A=\begin{pmatrix}a&b\\c&d\end{pmatrix}$ の余因子は、それぞれの成分の行と列を除いた $1\times1$ の行列式に符号を掛けて、$A_{11}=d$、$A_{12}=-c$、$A_{21}=-b$、$A_{22}=a$ です。これを転置して並べると $\mathrm{adj}(A)=\begin{pmatrix}A_{11}&A_{21}\\A_{12}&A_{22}\end{pmatrix}=\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$ で、$\det(A)=ad-bc$ なので、定理より次の公式が得られます。

$$ad-bc\neq0 \text{ のとき} \quad \begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1} = \frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$$

$ad-bc=0$ のときは、上の同値関係より逆行列は存在しません。

---

## 掃き出し法

余因子の計算量は $n$ が大きくなると急激に増えるため、実際の計算では**掃き出し法**がよく使われます。

**掃き出し法**：$(A \mid I)$ という $n \times 2n$ 行列を作り、行基本変形（2つの行の入れ替え・ある行の $0$ でない定数倍・ある行に他の行の定数倍を加える）を繰り返して左半分を単位行列 $I$ にすると、右半分が $A^{-1}$ になります。

具体的には、第 $1$ 列から第 $n$ 列まで順に、第 $j$ 列について次の操作を行います（このとき、第 $1$ 行〜第 $j-1$ 行にはすでにピボットが決まっています）。

1. 第 $j$ 列の第 $j$ 行〜第 $n$ 行の成分の中から、$0$ でない成分を1つ選び（**ピボット**）、必要なら行を入れ替えて、その行を第 $j$ 行（これまでにピボットを決めた行のすぐ下）に移す。
2. 第 $j$ 行をピボットの逆数倍して、ピボットを $1$ にする。
3. 第 $j$ 行以外の各行から、第 $j$ 行の適当な定数倍を引いて、第 $j$ 列のピボット以外の成分をすべて $0$ にする。

これを $j=1,2,\ldots,n$ について行うと、第 $j$ 列は第 $j$ 成分だけが $1$ で他が $0$ になるので、左半分が $I$ になります（第 $j$ 列の操作 2・3 では、第 $j$ 行を定数倍したり、その定数倍を他の行から引いたりします。第 $j$ 行の第 $1$ 〜 $j-1$ 列はすでに $0$ なので、処理済みの列は崩れません）。

**右半分が $A^{-1}$ になる理由**：行列式の記事で見たように、行基本変形を1回施すことは、対応する基本行列 $E$ を左から掛けることと同じです。行う変形を順に $E_1, E_2, \ldots, E_k$ とし、$P = E_k\cdots E_2E_1$ とおくと、変形全体は $P$ を左から掛けることにあたり、

$$P\,(A \mid I) = (PA \mid PI) = (PA \mid P)$$

です。左半分が $I$ になったのなら $PA=I$ で、右半分は $P$ そのものです。このとき $\det(P)\det(A)=\det(I)=1$ より $\det(A)\neq0$ なので、前の節より $A^{-1}$ が存在し、

$$P = P(AA^{-1}) = (PA)A^{-1} = IA^{-1} = A^{-1}$$

となります。よって右半分は $A^{-1}$ です。

**$A$ が正則でないとき**：もし左半分を $I$ にできたとすると、上と同じ計算で $\det(A)\neq0$ となります。したがって $\det(A)=0$ のときは、どのように変形しても左半分を $I$ にできません。実際の計算では、ある列でピボットに選べる $0$ でない成分がなくなるところで行き詰まり、それによって逆行列が存在しないと判定できます。

**例題**：$A=\begin{pmatrix}2&1\\1&1\end{pmatrix}$ の逆行列を掃き出し法で求める。

$$\left(\begin{array}{cc|cc}2&1&1&0\\1&1&0&1\end{array}\right) \xrightarrow{R_1\leftrightarrow R_2} \left(\begin{array}{cc|cc}1&1&0&1\\2&1&1&0\end{array}\right) \xrightarrow{R_2-2R_1} \left(\begin{array}{cc|cc}1&1&0&1\\0&-1&1&-2\end{array}\right) \xrightarrow{R_1+R_2,\ -R_2} \left(\begin{array}{cc|cc}1&0&1&-1\\0&1&-1&2\end{array}\right)$$

よって $A^{-1}=\begin{pmatrix}1&-1\\-1&2\end{pmatrix}$。$\det(A)=2\times1-1\times1=1$ なので、2次の公式 $\dfrac{1}{1}\begin{pmatrix}1&-1\\-1&2\end{pmatrix}$ と一致することも確認できます。

---

## 連立方程式への応用

$A$ を $n$ 次正方行列とし、連立方程式 $A\boldsymbol{x} = \boldsymbol{b}$ を考えます。$A$ が正則（$\det(A)\neq0$）なら、解はただ1つで $\boldsymbol{x} = A^{-1}\boldsymbol{b}$ です。

- **解はこれに限られる**：$\boldsymbol{x}$ が解なら、$A\boldsymbol{x}=\boldsymbol{b}$ の両辺に左から $A^{-1}$ を掛けて $A^{-1}A\boldsymbol{x} = A^{-1}\boldsymbol{b}$、すなわち $\boldsymbol{x} = A^{-1}\boldsymbol{b}$ です。
- **実際に解である**：$A(A^{-1}\boldsymbol{b}) = (AA^{-1})\boldsymbol{b} = I\boldsymbol{b} = \boldsymbol{b}$ です。

**例**：上の例題の $A$ と $\boldsymbol{b}=\begin{pmatrix}3\\2\end{pmatrix}$ について、連立方程式 $2x+y=3,\ x+y=2$ の解は

$$\boldsymbol{x}=A^{-1}\boldsymbol{b}=\begin{pmatrix}1&-1\\-1&2\end{pmatrix}\begin{pmatrix}3\\2\end{pmatrix}=\begin{pmatrix}1\\1\end{pmatrix}$$

となります。実際に $x=1,\ y=1$ を元の連立方程式に代入すると $2\times1+1=3$、$1+1=2$ となり、成り立つことが確認できます。

$\det(A)=0$ のときは $A^{-1}$ が存在しないので、この方法は使えません。このとき連立方程式は、解をもたないこともあれば、解が1つに定まらないこともあります。例えば $A=\begin{pmatrix}1&1\\1&1\end{pmatrix}$（$\det(A)=0$）では、$x+y=1,\ x+y=2$ には解がなく、$x+y=1,\ x+y=1$ には $(x,y)=(t,1-t)$ という無数の解があります。

---

## まとめ

逆行列は、掛けると単位行列になる「変換を打ち消す」行列です。逆行列が存在することと行列式が $0$ でないことは同値で、$A\cdot\mathrm{adj}(A)=\mathrm{adj}(A)\cdot A=\det(A)I$ を余因子展開・交代性・転置の性質から証明することで、余因子行列を使った公式が導けます。実用上は掃き出し法で求めることが多く、連立方程式を解く手段としても使えます。

---

## 関連ページ

- [固有値](eigenvalues.md)
