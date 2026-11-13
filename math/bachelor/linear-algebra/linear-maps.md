---
title: 線形写像
description: "ベクトル空間の構造を保つ線形写像を定義し、標準基底の像から表現行列が定まることを証明し、核・像（kernel/image）を求め、基底の拡張を用いて次元定理を証明し、全射・単射の判定条件を導く"
goal: "線形写像の定義から表現行列の存在を証明し、次元定理を証明し、全射・単射の判定条件を説明できるようになる"
tags: [math, linear-algebra, linear-maps]
stage: bachelor
subject: 線形代数
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 線形写像
    path: linear-maps.md
requires:
  - title: 行列
    path: matrices.md
  - title: ベクトル
    path: vectors.md
  - title: 逆行列
    path: matrices-inverse.md
---

## 「構造を保つ」変換

地図を、ある地点（原点）を中心に固定して拡大コピーすると、原点は動かず、原点から見た矢印（ベクトル）は向きを保ったまま一様に引き伸ばされます。2つの矢印をつないだもの（和）を拡大しても、それぞれを拡大してからつないでも同じ結果です。このように「原点を動かさず、足し算とスカラー倍の構造を壊さない変換」が**線形写像**です。地図全体をずらす平行移動も直線を直線に移しますが、原点を動かすので線形写像ではありません。

---

## 線形写像の定義

$\mathbb{R}^n$ から $\mathbb{R}^m$ への写像 $T$ が**線形写像**であるとは、任意の $\boldsymbol{u}, \boldsymbol{v} \in \mathbb{R}^n$ と $c \in \mathbb{R}$ に対して次が成り立つことです。

$$T(\boldsymbol{u} + \boldsymbol{v}) = T(\boldsymbol{u}) + T(\boldsymbol{v}), \qquad T(c\boldsymbol{u}) = cT(\boldsymbol{u})$$

「先に足してから変換」と「先に変換してから足す」が同じ結果になる、という意味です。特に、2つ目の条件で $c=0$ とすると $T(\boldsymbol{0}) = T(0\cdot\boldsymbol{0}) = 0\,T(\boldsymbol{0}) = \boldsymbol{0}$ なので、$T(\boldsymbol{0}) = \boldsymbol{0}$ が常に成立します。原点を中心とする回転、原点を中心とする拡大縮小、原点を通る直線や平面への射影などは、すべてこの条件を満たします（平行移動のように原点を動かす変換は満たしません）。

---

## 基本用語の確認

以降の議論では「基底」「次元」「部分空間」という用語を使います。「基底」「次元」は前提記事([ベクトル](vectors.md)の「一般のベクトル空間」節)で既に定義済みなので、そちらを参照してください。「部分空間」はここで新たに定義します。

- **部分空間**：零ベクトルを含み、和とスカラー倍について閉じている部分集合 $W$ のことです。$W$は零ベクトルという加法の単位元をあらかじめ含み、和とスカラー倍について閉じているため、逆元(任意の$v \in W$について$-v=(-1)v$もスカラー倍の閉性から$W$に属する)を含め他のベクトル空間の公理は全体の空間から自然に継承されます。したがって、前提記事で参照した基底・次元の定義がそのまま部分空間にも適用できます。なお、1つのベクトル空間の基底に含まれるベクトルの個数は基底の取り方によらないことが知られており、前提記事の「次元」の定義はこれを前提にしています。本記事でもこの事実を用います。特に、$\mathbb{R}^n$ には標準基底（次節）という $n$ 個のベクトルからなる基底があるので、$\mathbb{R}^n$ の基底はどれもちょうど $n$ 個のベクトルからなります。

次元定理の証明に使う事実を、ここで準備しておきます。出発点は、前提記事で述べた「$\mathbb{R}^n$ の線形独立なベクトルの組は最大 $n$ 個」という事実です。

**補題**：$\boldsymbol{w}_1, \ldots, \boldsymbol{w}_r$ が線形独立で、$\boldsymbol{v}$ がそれらの線形結合で表せないならば、$\boldsymbol{w}_1, \ldots, \boldsymbol{w}_r, \boldsymbol{v}$ も線形独立である。

**証明**：$a_1\boldsymbol{w}_1 + \cdots + a_r\boldsymbol{w}_r + b\boldsymbol{v} = \boldsymbol{0}$ とします。$b \neq 0$ なら $\boldsymbol{v} = -\frac{1}{b}(a_1\boldsymbol{w}_1 + \cdots + a_r\boldsymbol{w}_r)$ となり、$\boldsymbol{v}$ が線形結合で表せないことに反します。よって $b=0$ で、残る式 $a_1\boldsymbol{w}_1 + \cdots + a_r\boldsymbol{w}_r = \boldsymbol{0}$ と $\boldsymbol{w}_1, \ldots, \boldsymbol{w}_r$ の線形独立性から $a_1 = \cdots = a_r = 0$ です。$\blacksquare$

この補題から、次の3つが従います。いずれも「線形結合で表せないベクトルを付け加える」操作をくり返します。付け加えるたびに線形独立な組が1つ大きくなり、$\mathbb{R}^n$ の線形独立な組は最大 $n$ 個なので、この操作は $n$ 回以内に止まります。止まったとき、付け加えられるベクトルはもうないので、それまでの組がすべてを張っています。

- **(a) 部分空間は基底をもつ**：$\mathbb{R}^n$ の部分空間 $W$ について、$W$ のベクトルを上の操作で付け加えていくと、$n$ 個以下のベクトルからなる $W$ の基底が得られます（$W=\{\boldsymbol{0}\}$ のときは、ベクトルを1つも含まない組を基底とし、次元は $0$ とします）。
- **(b) 基底の拡張**：$W$ の基底に、$\mathbb{R}^n$ のベクトルを上の操作で付け加えていくと、$\mathbb{R}^n$ の基底が得られます。$\mathbb{R}^n$ の基底はちょうど $n$ 個のベクトルからなるので、もとの基底が $k$ 個なら、付け加えるベクトルはちょうど $n-k$ 個です。
- **(c) 次元が全体と等しい部分空間は全体**：$\mathbb{R}^m$ の部分空間 $W$ の次元が $m$ ならば $W = \mathbb{R}^m$ です。$W$ の基底（$m$ 個）が $\mathbb{R}^m$ を張らないとすると、その線形結合で表せないベクトルを付け加えて、補題より $m+1$ 個の線形独立な組が得られ、「最大 $m$ 個」に反するからです。

---

## 表現行列

**定理**：$T: \mathbb{R}^n \to \mathbb{R}^m$ を線形写像、$\boldsymbol{e}_1, \ldots, \boldsymbol{e}_n$ を標準基底（下記）とすると、$A = \begin{pmatrix} T(\boldsymbol{e}_1) & \cdots & T(\boldsymbol{e}_n) \end{pmatrix}$（$m\times n$行列）とおくとき、任意の $\boldsymbol{x} \in \mathbb{R}^n$ について $T(\boldsymbol{x}) = A\boldsymbol{x}$ が成り立つ。

ここで $\boldsymbol{e}_i$ は、第 $i$ 成分だけが $1$ で他の成分が $0$ のベクトルで、前提記事[行列](matrices.md)の「基本ベクトル」と同じものです。$\boldsymbol{e}_1, \ldots, \boldsymbol{e}_n$ は線形独立で、任意の $\boldsymbol{x}=(x_1,\ldots,x_n)$ を $\boldsymbol{x} = \sum_{i=1}^n x_i \boldsymbol{e}_i$ と表せる（$\mathbb{R}^n$ を張る）ので $\mathbb{R}^n$ の基底であり、これを**標準基底**といいます。前提記事では「行列の各列は基本ベクトルの移った先」であることを例で見ましたが、この定理は、どんな線形写像もそのような行列で表せることを示しています。

**証明**：$\boldsymbol{x} = (x_1, \ldots, x_n)$ は標準基底を用いて $\boldsymbol{x} = \sum_{i=1}^n x_i \boldsymbol{e}_i$ と書けます。線形写像の2条件（和とスカラー倍の保存）をくり返し使うと、

$$T(\boldsymbol{x}) = T\left(\sum_{i=1}^n x_i \boldsymbol{e}_i\right) = \sum_{i=1}^n x_i\, T(\boldsymbol{e}_i)$$

一方、行列とベクトルの積の定義から $A\boldsymbol{x} = \sum_{i=1}^n x_i\, T(\boldsymbol{e}_i)$（$A$ の $i$ 列目が $T(\boldsymbol{e}_i)$ であることによる）なので、$T(\boldsymbol{x}) = A\boldsymbol{x}$。$\blacksquare$

この $A$ を $T$ の**表現行列**といい、$\mathbb{R}^n$ から $\mathbb{R}^m$ への線形写像は必ずある行列で表せます。

**例**：$T: \mathbb{R}^2 \to \mathbb{R}^2$ が原点を中心とする反時計回りの $\theta$ 回転のとき、表現行列は $\begin{pmatrix}\cos\theta & -\sin\theta \\ \sin\theta & \cos\theta\end{pmatrix}$。

---

## 核と像

**核**（kernel）：$\ker T = \{\boldsymbol{x} \in \mathbb{R}^n : T(\boldsymbol{x}) = \boldsymbol{0}\}$。これは $A\boldsymbol{x} = \boldsymbol{0}$ の解空間で、$\mathbb{R}^n$ の部分空間です。

**像**（image）：$\mathrm{Im}\, T = \{T(\boldsymbol{x}) : \boldsymbol{x} \in \mathbb{R}^n\}$。$A\boldsymbol{x} = \sum x_i\,(A\text{ の第 }i\text{ 列})$ なので、$A$ の列ベクトルが張る部分空間（列空間）です。

どちらも部分空間の条件を満たすことを確かめます。

- $\ker T$：$T(\boldsymbol{0})=\boldsymbol{0}$ より $\boldsymbol{0} \in \ker T$。$\boldsymbol{u}, \boldsymbol{v} \in \ker T$、$c \in \mathbb{R}$ なら、線形性より $T(\boldsymbol{u}+\boldsymbol{v}) = T(\boldsymbol{u})+T(\boldsymbol{v}) = \boldsymbol{0}$、$T(c\boldsymbol{u}) = cT(\boldsymbol{u}) = \boldsymbol{0}$ なので、$\boldsymbol{u}+\boldsymbol{v}$、$c\boldsymbol{u}$ も $\ker T$ に属します。
- $\mathrm{Im}\,T$：$\boldsymbol{0} = T(\boldsymbol{0}) \in \mathrm{Im}\,T$。$T(\boldsymbol{u})$、$T(\boldsymbol{v}) \in \mathrm{Im}\,T$ なら、線形性より $T(\boldsymbol{u})+T(\boldsymbol{v}) = T(\boldsymbol{u}+\boldsymbol{v})$、$cT(\boldsymbol{u}) = T(c\boldsymbol{u})$ もある元の像なので $\mathrm{Im}\,T$ に属します。

よって、準備の (a) より $\ker T$ と $\mathrm{Im}\,T$ はどちらも基底をもち、次元が定まります。

---

## 次元定理

$\dim(\ker T)$ を**退化次数**（nullity）、$\dim(\mathrm{Im}\, T)$ を**階数**（rank）といいます。

**次元定理**：$T: \mathbb{R}^n \to \mathbb{R}^m$ が線形写像ならば、

$$\dim(\ker T) + \dim(\mathrm{Im}\, T) = n$$

**証明**：$\ker T$ の基底を $\boldsymbol{v}_1, \ldots, \boldsymbol{v}_k$（$k = \dim\ker T$）とし、準備の (b) により、これを $\mathbb{R}^n$ の基底 $\boldsymbol{v}_1, \ldots, \boldsymbol{v}_k, \boldsymbol{v}_{k+1}, \ldots, \boldsymbol{v}_n$ に拡張します。

$T(\boldsymbol{v}_{k+1}), \ldots, T(\boldsymbol{v}_n)$ が $\mathrm{Im}\,T$ の基底であること、すなわち $\mathrm{Im}\,T$ を張ることと線形独立であることを示せば、$\dim(\mathrm{Im}\,T) = n-k$ が言えて定理が従います。

*張ること*：任意の $\boldsymbol{x} \in \mathbb{R}^n$ は基底を使って $\boldsymbol{x} = \sum_{i=1}^n c_i \boldsymbol{v}_i$ と書け、

$$T(\boldsymbol{x}) = \sum_{i=1}^k c_i T(\boldsymbol{v}_i) + \sum_{i=k+1}^n c_i T(\boldsymbol{v}_i) = \sum_{i=k+1}^n c_i T(\boldsymbol{v}_i)$$

（$\boldsymbol{v}_1,\ldots,\boldsymbol{v}_k \in \ker T$ なので前半の項はすべて $\boldsymbol{0}$）。よって $\mathrm{Im}\,T$ の任意の元は $T(\boldsymbol{v}_{k+1}), \ldots, T(\boldsymbol{v}_n)$ の線形結合で表せます。

*線形独立であること*：$\sum_{i=k+1}^n c_i T(\boldsymbol{v}_i) = \boldsymbol{0}$ と仮定すると、線形性より $T\left(\sum_{i=k+1}^n c_i \boldsymbol{v}_i\right) = \boldsymbol{0}$ なので $\sum_{i=k+1}^n c_i \boldsymbol{v}_i \in \ker T$ です。$\boldsymbol{v}_1,\ldots,\boldsymbol{v}_k$ は $\ker T$ の基底なので、ある $d_1, \ldots, d_k$ を用いて

$$\sum_{i=k+1}^n c_i \boldsymbol{v}_i = \sum_{i=1}^k d_i \boldsymbol{v}_i$$

と書けます。移項すると

$$d_1\boldsymbol{v}_1 + \cdots + d_k\boldsymbol{v}_k - c_{k+1}\boldsymbol{v}_{k+1} - \cdots - c_n\boldsymbol{v}_n = \boldsymbol{0}$$

で、$\boldsymbol{v}_1,\ldots,\boldsymbol{v}_n$ は基底なので線形独立です。線形独立の定義より係数はすべて $0$ で、特に $c_{k+1}=\cdots=c_n=0$ です。

以上より $T(\boldsymbol{v}_{k+1}), \ldots, T(\boldsymbol{v}_n)$ は $\mathrm{Im}\,T$ の基底なので $\dim(\mathrm{Im}\,T) = n-k$、すなわち $\dim(\ker T) + \dim(\mathrm{Im}\,T) = k + (n-k) = n$。$\blacksquare$

**例**：$A = \begin{pmatrix}1&2&3\\2&4&6\end{pmatrix}$ を表現行列とする線形写像 $T: \mathbb{R}^3 \to \mathbb{R}^2$、$T(\boldsymbol{x}) = A\boldsymbol{x}$ を考えます。$\mathrm{Im}\,T$ は $A$ の列 $\begin{pmatrix}1\\2\end{pmatrix}$、$\begin{pmatrix}2\\4\end{pmatrix}$、$\begin{pmatrix}3\\6\end{pmatrix}$ が張る空間です。2列目・3列目はそれぞれ1列目の $2$ 倍・$3$ 倍なので、$\mathrm{Im}\,T$ は $\begin{pmatrix}1\\2\end{pmatrix}$ が張る1次元の空間で、$\mathrm{rank}(A) = \dim(\mathrm{Im}\,T) = 1$ です。次元定理より $\dim(\ker T) = 3 - 1 = 2$ です。

核を直接求めて確かめます。$A\boldsymbol{x} = \boldsymbol{0}$ は、2行目が1行目の $2$ 倍なので、$x_1 + 2x_2 + 3x_3 = 0$ の1本の式と同じです。$x_2 = s$、$x_3 = t$ を自由に選ぶと $x_1 = -2s - 3t$ なので、

$$\boldsymbol{x} = \begin{pmatrix}-2s-3t\\ s\\ t\end{pmatrix} = s\begin{pmatrix}-2\\1\\0\end{pmatrix} + t\begin{pmatrix}-3\\0\\1\end{pmatrix}$$

です。$(-2,1,0)$ と $(-3,0,1)$ は $\ker T$ を張り、第2・第3成分を見ると $s\cdot(-2,1,0)+t\cdot(-3,0,1)=\boldsymbol{0}$ なら $s=t=0$ なので線形独立です。よって、これらが $\ker T$ の基底で $\dim(\ker T) = 2$ となり、次元定理の結果と一致します。

---

## 全射・単射の条件

**命題**：$T$ が単射であることと $\ker T = \{\boldsymbol{0}\}$ は同値である。

**証明**：$T$ が単射ならば、$T(\boldsymbol{x})=\boldsymbol{0}=T(\boldsymbol{0})$ を満たす $\boldsymbol{x}$ は $\boldsymbol{x}=\boldsymbol{0}$ に限られるので $\ker T=\{\boldsymbol{0}\}$。逆に $\ker T=\{\boldsymbol{0}\}$ とすると、$T(\boldsymbol{u})=T(\boldsymbol{v})$ から線形性より $T(\boldsymbol{u}-\boldsymbol{v})=\boldsymbol{0}$、すなわち $\boldsymbol{u}-\boldsymbol{v}\in\ker T=\{\boldsymbol{0}\}$ なので $\boldsymbol{u}=\boldsymbol{v}$。よって単射です。$\blacksquare$

$\ker T=\{\boldsymbol{0}\}$ は $\dim(\ker T)=0$ と同じなので、次元定理より $\dim(\mathrm{Im}\,T)=n$、すなわち $\mathrm{rank}(A)=n$ と同値です。まとめると、

- $T$ が単射 $\iff$ $\ker T = \{\boldsymbol{0}\}$ $\iff$ $\mathrm{rank}(A) = n$
- $T$ が全射 $\iff$ $\mathrm{Im}\, T = \mathbb{R}^m$（定義より）$\iff$ $\mathrm{rank}(A) = m$
- $n = m$ のとき、全射 $\iff$ 単射

2つ目の後半の同値は次のとおりです。$\mathrm{Im}\,T = \mathbb{R}^m$ なら $\dim(\mathrm{Im}\,T) = m$ です。逆に $\dim(\mathrm{Im}\,T) = m$ なら、$\mathrm{Im}\,T$ は次元 $m$ の $\mathbb{R}^m$ の部分空間なので、準備の (c) より $\mathrm{Im}\,T = \mathbb{R}^m$ です。3つ目は、$n=m$ のとき単射 $\iff \mathrm{rank}(A)=n$、全射 $\iff \mathrm{rank}(A)=m=n$ と、条件が一致することから従います。

なお、$n=m$ のとき、これらの条件は表現行列 $A$ が可逆であることとも同値であることが知られています（[逆行列](matrices-inverse.md)も参照）。

---

## まとめ

線形写像は足し算とスカラー倍を保つ変換で、標準基底での像を並べた行列がその表現行列になることが証明できます。核と像はその写像の「潰れ方」と「届く範囲」を表し、核の基底を定義域の基底に拡張するという構成により、次元定理（核と像の次元の和が定義域の次元に一致する）が証明できます。この定理から、単射・全射の条件がランクを使って簡潔に判定できます。

---

## 関連ページ

- [固有値](eigenvalues.md)
