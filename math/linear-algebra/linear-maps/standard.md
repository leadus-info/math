---
title: 線形写像
description: "核・像・次元定理"
goal: "線形写像の核・像を求め、次元定理を使って解空間の次元を計算できるようになる"
tags: [math,linear-algebra,linear-maps]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 線形代数
    path: /math/linear-algebra/index.md
  - title: 線形写像
    path: /math/linear-algebra/linear-maps/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 線形写像（入門）
    path: /math/linear-algebra/linear-maps/introduction.md
  - title: 行列（標準）
    path: /math/linear-algebra/matrices/standard.md
  - title: ベクトル（標準）
    path: /math/linear-algebra/vectors/standard.md
---

## 線形写像の定義

$\mathbb{R}^n$ から $\mathbb{R}^m$ への写像 $T$ が**線形写像**であるとは、任意の $\boldsymbol{u}, \boldsymbol{v} \in \mathbb{R}^n$ と $c \in \mathbb{R}$ に対して：

$$T(\boldsymbol{u} + \boldsymbol{v}) = T(\boldsymbol{u}) + T(\boldsymbol{v})$$
$$T(c\boldsymbol{u}) = cT(\boldsymbol{u})$$

が成り立つことです。特に $T(\boldsymbol{0}) = \boldsymbol{0}$ が常に成立します。

---

## 表現行列

$T: \mathbb{R}^n \to \mathbb{R}^m$ を線形写像、$\boldsymbol{e}_1, \ldots, \boldsymbol{e}_n$ を標準基底とすると：

$$T(\boldsymbol{x}) = A\boldsymbol{x}, \quad A = \begin{pmatrix} T(\boldsymbol{e}_1) & \cdots & T(\boldsymbol{e}_n) \end{pmatrix}$$

$A$ を $T$ の**表現行列**といいます（$m \times n$ 行列）。

**例**：$T: \mathbb{R}^2 \to \mathbb{R}^2$ が $\theta$ 回転のとき、表現行列は $\begin{pmatrix}\cos\theta & -\sin\theta \\ \sin\theta & \cos\theta\end{pmatrix}$。

---

## 核と像

**核**（kernel）：$\ker T = \{\boldsymbol{x} \in \mathbb{R}^n : T(\boldsymbol{x}) = \boldsymbol{0}\}$

$A\boldsymbol{x} = \boldsymbol{0}$ の解空間です。$\ker T$ は $\mathbb{R}^n$ の部分空間。

**像**（image）：$\mathrm{Im}\, T = \{T(\boldsymbol{x}) : \boldsymbol{x} \in \mathbb{R}^n\}$

$A$ の列ベクトルが張る部分空間（列空間）です。

---

## 次元定理（rank-nullity theorem）

$$\dim(\ker T) + \dim(\mathrm{Im}\, T) = n$$

$\dim(\ker T)$ を**退化次数**（nullity）、$\dim(\mathrm{Im}\, T)$ を**階数**（rank）といいます。

**例**：$A = \begin{pmatrix}1&2&3\\2&4&6\end{pmatrix}$ のとき $\mathrm{rank}(A) = 1$（行が比例）。次元定理より $\dim(\ker T) = 3 - 1 = 2$。

---

## 全射・単射の条件

- $T$ が単射 $\iff$ $\ker T = \{\boldsymbol{0}\}$ $\iff$ $\mathrm{rank}(A) = n$
- $T$ が全射 $\iff$ $\mathrm{Im}\, T = \mathbb{R}^m$ $\iff$ $\mathrm{rank}(A) = m$
- $n = m$ のとき全射 $\iff$ 単射 $\iff$ $A$ が可逆

---

## 関連ページ

- [行列（標準）](../matrices/standard.md)
- [ベクトル（標準）](../vectors/standard.md)
- [固有値（標準）](../eigenvalues/standard.md)
