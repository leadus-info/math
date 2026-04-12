---
title: 点
description: "距離空間・位相空間・多様体上の点"
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
  - title: 点
    path: /math/geometry/point/introduction.md
  - title: 集合（専門）
    path: ../../math-language/sets/professional.md
  - title: 極限（専門）
    path: ../../functions/limits/professional.md
---

## 距離空間

「距離」の概念を公理的に定義します。

**定義**：集合 $X$ と関数 $d: X \times X \to [0, \infty)$ の組 $(X, d)$ が**距離空間**であるとは：

1. $d(x, y) = 0 \iff x = y$（非退化性）
2. $d(x, y) = d(y, x)$（対称性）
3. $d(x, z) \leq d(x, y) + d(y, z)$（**三角不等式**）

**例**：
- $(\mathbb{R}^n, \|\cdot - \cdot\|_2)$：ユークリッド距離（標準的な例）
- $(\mathbb{R}^n, \|\cdot - \cdot\|_\infty)$：最大値距離
- 離散距離：$d(x,y) = 1$（$x \neq y$）、$0$（$x = y$）

---

## 位相空間

距離を使わずに「近さ」を定義する枠組みが**位相空間**です。

**定義**：集合 $X$ と「開集合族」$\mathcal{T} \subseteq 2^X$ の組 $(X, \mathcal{T})$ が位相空間であるとは：

1. $\emptyset, X \in \mathcal{T}$
2. 有限個の開集合の共通部分は開集合
3. 任意個の開集合の合併は開集合

距離空間では $d$-開球 $B_r(x) = \{y : d(x,y) < r\}$ を使って自然に位相が定まります。\
位相空間は距離空間より広いクラスです。

---

## 連続写像

$(X, \mathcal{T}_X)$ から $(Y, \mathcal{T}_Y)$ への写像 $f: X \to Y$ が**連続**とは：\
$V \in \mathcal{T}_Y \Rightarrow f^{-1}(V) \in \mathcal{T}_X$（開集合の逆像が開集合）。

距離空間では「$\varepsilon$-$\delta$ 連続」と一致します。

---

## 多様体

局所的にユークリッド空間と同相な位相空間が**$n$ 次元多様体**です。

各点 $p$ の近傍が $\mathbb{R}^n$ と同相（チャート）で、チャートの間の変換（遷移写像）が滑らかな場合を**滑らかな多様体**（微分可能多様体）といいます。

例：$S^2$（球面、$n=2$）、$T^2$（トーラス、$n=2$）、$\mathbb{R}^n$ そのもの。

**参考文献**：Munkres, J. R. (2000). *Topology* (2nd ed.). Prentice Hall.

---

## 関連ページ

- [点](standard.md)
- [集合（専門）](../../math-language/sets/professional.md)
- [ベクトル（専門）](../../linear-algebra/vectors/professional.md)
