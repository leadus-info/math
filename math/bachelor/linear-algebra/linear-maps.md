---
title: 線形写像
description: "ベクトルの構造を保つ変換"
goal: "線形写像を定義から理解し、表現行列・核・像を求め、次元定理を使えるようになる"
tags: [math, linear-algebra, linear-maps]
stage: 発展編
subject: 線形代数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 発展編
    path: /math/bachelor/index.md
  - title: 線形写像
    path: /math/bachelor/linear-algebra/linear-maps.md
requires:
  - title: 行列
    path: /math/bachelor/linear-algebra/matrices.md
  - title: ベクトル
    path: /math/bachelor/linear-algebra/vectors.md
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

$T: \mathbb{R}^n \to \mathbb{R}^m$ を線形写像、$\boldsymbol{e}_1, \ldots, \boldsymbol{e}_n$ を標準基底とすると、

$$T(\boldsymbol{x}) = A\boldsymbol{x}, \quad A = \begin{pmatrix} T(\boldsymbol{e}_1) & \cdots & T(\boldsymbol{e}_n) \end{pmatrix}$$

と書けます。この $A$（$m \times n$ 行列）を $T$ の**表現行列**といい、$\mathbb{R}^n$ から $\mathbb{R}^m$ への線形写像は必ずある行列で表せます。

**例**：$T: \mathbb{R}^2 \to \mathbb{R}^2$ が $\theta$ 回転のとき、表現行列は $\begin{pmatrix}\cos\theta & -\sin\theta \\ \sin\theta & \cos\theta\end{pmatrix}$。

---

## 核と像

**核**（kernel）：$\ker T = \{\boldsymbol{x} \in \mathbb{R}^n : T(\boldsymbol{x}) = \boldsymbol{0}\}$。これは $A\boldsymbol{x} = \boldsymbol{0}$ の解空間で、$\mathbb{R}^n$ の部分空間です。

**像**（image）：$\mathrm{Im}\, T = \{T(\boldsymbol{x}) : \boldsymbol{x} \in \mathbb{R}^n\}$。$A$ の列ベクトルが張る部分空間（列空間）です。

---

## 次元定理

$$\dim(\ker T) + \dim(\mathrm{Im}\, T) = n$$

$\dim(\ker T)$ を**退化次数**（nullity）、$\dim(\mathrm{Im}\, T)$ を**階数**（rank）といいます。

**例**：$A = \begin{pmatrix}1&2&3\\2&4&6\end{pmatrix}$ のとき $\mathrm{rank}(A) = 1$（行が比例）。次元定理より $\dim(\ker T) = 3 - 1 = 2$。

---

## 全射・単射の条件

- $T$ が単射 $\iff$ $\ker T = \{\boldsymbol{0}\}$ $\iff$ $\mathrm{rank}(A) = n$
- $T$ が全射 $\iff$ $\mathrm{Im}\, T = \mathbb{R}^m$ $\iff$ $\mathrm{rank}(A) = m$
- $n = m$ のとき、全射 $\iff$ 単射 $\iff$ $A$ が可逆

---

## まとめ

線形写像は足し算とスカラー倍を保つ変換で、$\mathbb{R}^n$ から $\mathbb{R}^m$ への線形写像はすべて行列で表現できます。核と像はその写像の「潰れ方」と「届く範囲」を表し、次元定理はこの2つの次元の和が定義域の次元に一致することを示します。

---

## 関連ページ

- [固有値（発展編）](eigenvalues.md)
