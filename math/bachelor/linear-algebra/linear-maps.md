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
---

## 「構造を保つ」変換

地図を拡大コピーするとき、距離は変わっても「直線は直線のまま」「平行な道は平行なまま」です。このように「足し算とスカラー倍の構造を壊さない変換」が**線形写像**です。

---

## 線形写像の定義

$\mathbb{R}^n$ から $\mathbb{R}^m$ への写像 $T$ が**線形写像**であるとは、任意の $\boldsymbol{u}, \boldsymbol{v} \in \mathbb{R}^n$ と $c \in \mathbb{R}$ に対して次が成り立つことです。

$$T(\boldsymbol{u} + \boldsymbol{v}) = T(\boldsymbol{u}) + T(\boldsymbol{v}), \qquad T(c\boldsymbol{u}) = cT(\boldsymbol{u})$$

「先に足してから変換」と「先に変換してから足す」が同じ結果になる、という意味です。特に $T(\boldsymbol{0}) = \boldsymbol{0}$ が常に成立します。回転・拡大縮小・射影などは、すべてこの条件を満たします。

---

## 表現行列

**定理**：$T: \mathbb{R}^n \to \mathbb{R}^m$ を線形写像、$\boldsymbol{e}_1, \ldots, \boldsymbol{e}_n$ を標準基底とすると、$A = \begin{pmatrix} T(\boldsymbol{e}_1) & \cdots & T(\boldsymbol{e}_n) \end{pmatrix}$（$m\times n$行列）とおくとき、任意の $\boldsymbol{x} \in \mathbb{R}^n$ について $T(\boldsymbol{x}) = A\boldsymbol{x}$ が成り立つ。

**証明**：$\boldsymbol{x} = (x_1, \ldots, x_n)$ は標準基底を用いて $\boldsymbol{x} = \sum_{i=1}^n x_i \boldsymbol{e}_i$ と書けます。線形写像の2条件（和とスカラー倍の保存）をくり返し使うと、

$$T(\boldsymbol{x}) = T\left(\sum_{i=1}^n x_i \boldsymbol{e}_i\right) = \sum_{i=1}^n x_i\, T(\boldsymbol{e}_i)$$

一方、行列とベクトルの積の定義から $A\boldsymbol{x} = \sum_{i=1}^n x_i\, T(\boldsymbol{e}_i)$（$A$ の $i$ 列目が $T(\boldsymbol{e}_i)$ であることによる）なので、$T(\boldsymbol{x}) = A\boldsymbol{x}$。$\blacksquare$

この $A$ を $T$ の**表現行列**といい、$\mathbb{R}^n$ から $\mathbb{R}^m$ への線形写像は必ずある行列で表せます。

**例**：$T: \mathbb{R}^2 \to \mathbb{R}^2$ が $\theta$ 回転のとき、表現行列は $\begin{pmatrix}\cos\theta & -\sin\theta \\ \sin\theta & \cos\theta\end{pmatrix}$。

---

## 核と像

**核**（kernel）：$\ker T = \{\boldsymbol{x} \in \mathbb{R}^n : T(\boldsymbol{x}) = \boldsymbol{0}\}$。これは $A\boldsymbol{x} = \boldsymbol{0}$ の解空間で、$\mathbb{R}^n$ の部分空間です。

**像**（image）：$\mathrm{Im}\, T = \{T(\boldsymbol{x}) : \boldsymbol{x} \in \mathbb{R}^n\}$。$A$ の列ベクトルが張る部分空間（列空間）です。

---

## 次元定理

$\dim(\ker T)$ を**退化次数**（nullity）、$\dim(\mathrm{Im}\, T)$ を**階数**（rank）といいます。

**次元定理**：$T: \mathbb{R}^n \to \mathbb{R}^m$ が線形写像ならば、

$$\dim(\ker T) + \dim(\mathrm{Im}\, T) = n$$

**証明**：$\ker T$ の基底を $\boldsymbol{v}_1, \ldots, \boldsymbol{v}_k$（$k = \dim\ker T$）とし、これを $\mathbb{R}^n$ の基底 $\boldsymbol{v}_1, \ldots, \boldsymbol{v}_k, \boldsymbol{v}_{k+1}, \ldots, \boldsymbol{v}_n$ に拡張します（基底の拡張定理）。$\mathrm{Im}\,T = \{T(\boldsymbol{v}_{k+1}), \ldots, T(\boldsymbol{v}_n)\}$ が張る空間であることを示せば、$\dim(\mathrm{Im}\,T) = n-k$ が言えて定理が従います。

*生成すること*：任意の $\boldsymbol{x} \in \mathbb{R}^n$ は基底を使って $\boldsymbol{x} = \sum_{i=1}^n c_i \boldsymbol{v}_i$ と書け、

$$T(\boldsymbol{x}) = \sum_{i=1}^k c_i T(\boldsymbol{v}_i) + \sum_{i=k+1}^n c_i T(\boldsymbol{v}_i) = \sum_{i=k+1}^n c_i T(\boldsymbol{v}_i)$$

（$\boldsymbol{v}_1,\ldots,\boldsymbol{v}_k \in \ker T$ なので前半の項はすべて $\boldsymbol{0}$）。よって $\mathrm{Im}\,T$ の任意の元は $T(\boldsymbol{v}_{k+1}), \ldots, T(\boldsymbol{v}_n)$ の線形結合で表せます。

*線形独立であること*：$\sum_{i=k+1}^n c_i T(\boldsymbol{v}_i) = \boldsymbol{0}$ と仮定すると、線形性より $T\left(\sum_{i=k+1}^n c_i \boldsymbol{v}_i\right) = \boldsymbol{0}$ なので $\sum_{i=k+1}^n c_i \boldsymbol{v}_i \in \ker T$。これは $\boldsymbol{v}_1,\ldots,\boldsymbol{v}_k$ の線形結合として一意に書けるはずですが、$\boldsymbol{v}_1,\ldots,\boldsymbol{v}_n$ は基底（線形独立）なので、$\sum_{i=k+1}^n c_i \boldsymbol{v}_i$ をこの2通りの方法で表す係数を比較すると $c_{k+1}=\cdots=c_n=0$ しかありえません。

以上より $T(\boldsymbol{v}_{k+1}), \ldots, T(\boldsymbol{v}_n)$ は $\mathrm{Im}\,T$ の基底なので $\dim(\mathrm{Im}\,T) = n-k$、すなわち $\dim(\ker T) + \dim(\mathrm{Im}\,T) = k + (n-k) = n$。$\blacksquare$

**例**：$A = \begin{pmatrix}1&2&3\\2&4&6\end{pmatrix}$ のとき $\mathrm{rank}(A) = 1$（行が比例）。次元定理より $\dim(\ker T) = 3 - 1 = 2$。

---

## 全射・単射の条件

**命題**：$T$ が単射であることと $\ker T = \{\boldsymbol{0}\}$ は同値である。

**証明**：$T$ が単射ならば、$T(\boldsymbol{x})=\boldsymbol{0}=T(\boldsymbol{0})$ を満たす $\boldsymbol{x}$ は $\boldsymbol{x}=\boldsymbol{0}$ に限られるので $\ker T=\{\boldsymbol{0}\}$。逆に $\ker T=\{\boldsymbol{0}\}$ とすると、$T(\boldsymbol{u})=T(\boldsymbol{v})$ から線形性より $T(\boldsymbol{u}-\boldsymbol{v})=\boldsymbol{0}$、すなわち $\boldsymbol{u}-\boldsymbol{v}\in\ker T=\{\boldsymbol{0}\}$ なので $\boldsymbol{u}=\boldsymbol{v}$。よって単射です。$\blacksquare$

$\ker T=\{\boldsymbol{0}\}$ は $\dim(\ker T)=0$ と同じなので、次元定理より $\dim(\mathrm{Im}\,T)=n$、すなわち $\mathrm{rank}(A)=n$ と同値です。まとめると、

- $T$ が単射 $\iff$ $\ker T = \{\boldsymbol{0}\}$ $\iff$ $\mathrm{rank}(A) = n$
- $T$ が全射 $\iff$ $\mathrm{Im}\, T = \mathbb{R}^m$（定義より）$\iff$ $\mathrm{rank}(A) = m$
- $n = m$ のとき、次元定理より $\dim(\ker T)=0 \iff \dim(\mathrm{Im}\,T)=n=m$ なので、全射 $\iff$ 単射 $\iff$ $A$ が可逆

---

## まとめ

線形写像は足し算とスカラー倍を保つ変換で、標準基底での像を並べた行列がその表現行列になることが証明できます。核と像はその写像の「潰れ方」と「届く範囲」を表し、核の基底を定義域の基底に拡張するという構成により、次元定理（核と像の次元の和が定義域の次元に一致する）が証明できます。この定理から、単射・全射の条件がランクを使って簡潔に判定できます。

---

## 関連ページ

- [固有値](eigenvalues.md)
