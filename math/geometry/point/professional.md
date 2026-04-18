---
title: 点
description: "距離空間・位相空間・多様体"
goal: "距離空間の公理から位相空間の定義へと抽象化の流れを理解し、多様体の概念を説明できるようになる"
tags: [math,geometry,point]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 点
    path: /math/geometry/point/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 点（標準）
    path: /math/geometry/point/standard.md
  - title: 集合（専門）
    path: /math/math-language/sets/professional.md
---

## 距離空間

**定義**：集合 $X$ と関数 $d: X \times X \to [0, \infty)$ の組 $(X, d)$ が**距離空間**であるとは：

1. $d(x, y) = 0 \iff x = y$（非退化性）
2. $d(x, y) = d(y, x)$（対称性）
3. $d(x, z) \leq d(x, y) + d(y, z)$（三角不等式）

**例**：
- $\mathbb{R}^n$ と通常の距離 $d(x,y) = \|x - y\|_2$（ユークリッド距離空間）
- 離散距離：$d(x,y) = 1$（$x \neq y$）、$d(x,x) = 0$

**定義**：$x_0$ を中心、半径 $r$ の**開球**：$B_r(x_0) = \{x \in X : d(x, x_0) < r\}$

---

## 位相空間

距離を使わずに「近さ」を定義する枠組みです。

**定義**：集合 $X$ と開集合族 $\mathcal{T} \subset 2^X$ の組 $(X, \mathcal{T})$ が**位相空間**であるとは：

1. $\emptyset, X \in \mathcal{T}$
2. 有限個の開集合の共通部分は開集合
3. 任意個の開集合の合併は開集合

距離空間では開球を使って自然に位相が定まります。位相空間は距離空間より広いクラスです。

**連続写像**：$(X, \mathcal{T}_X) \to (Y, \mathcal{T}_Y)$ への写像 $f$ が連続 $\iff$ $V \in \mathcal{T}_Y \Rightarrow f^{-1}(V) \in \mathcal{T}_X$

---

## 多様体

**定義**：$(n$ 次元）**多様体**とは、各点の近傍が $\mathbb{R}^n$ と同相な（位相）空間です。

より精密に：$(M, \mathcal{T})$ が第2可算ハウスドルフ空間で、各点 $p \in M$ に対して $\mathbb{R}^n$ との同相写像を持つ近傍（チャート）が存在するものです。

チャート間の遷移写像が $C^\infty$ のとき**滑らかな多様体**（可微分多様体）といいます。

**例**：$\mathbb{R}^n$（自明）、$S^n$（$n$ 次元球面）、$T^n$（$n$ 次元トーラス）

**参考文献**：Munkres, J. R. (2000). *Topology* (2nd ed.). Prentice Hall.

---

## 関連ページ

- [点（標準）](standard.md)
- [集合（専門）](../../math-language/sets/professional.md)
- [ベクトル（専門）](../../linear-algebra/vectors/professional.md)
