---
title: 関数
description: "関数の定義・性質・合成・逆関数"
goal: "関数を写像として定義し、単射・全射・全単射・合成・逆関数を正確に扱えるようになる"
tags: [math,analysis,functions]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 解析
    path: /math/analysis/index.md
  - title: 関数
    path: /math/analysis/functions/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 関数（入門）
    path: /math/analysis/functions/introduction.md
  - title: 集合（標準）
    path: /math/foundations/sets/standard.md
---

## 関数の定義

集合 $A$ から集合 $B$ への**関数**（写像）$f: A \to B$ とは、$A$ の各要素 $x$ に対して $B$ の要素 $f(x)$ をただ一つ対応させる規則です。

- $A$：**定義域**（domain）
- $B$：**終域**（codomain）
- $\{f(x) \mid x \in A\}$：**値域**（range）— 終域の部分集合

値域と終域は一般に異なります。$f: \mathbb{R} \to \mathbb{R}$、$f(x) = x^2$ の値域は $[0, \infty)$ であり終域 $\mathbb{R}$ より小さい。

---

## 単射・全射・全単射

**単射**（one-to-one）：$f(x_1) = f(x_2) \Rightarrow x_1 = x_2$\
異なる入力は異なる出力を持つ。

**全射**（onto）：任意の $y \in B$ に対し $f(x) = y$ となる $x \in A$ が存在する。\
終域のすべての値が出力として現れる。

**全単射**（bijection）：単射かつ全射。$A$ と $B$ の間に完全な1対1対応。

**例**：$f: \mathbb{R} \to \mathbb{R}$、$f(x) = x^2$\
単射でない（$f(2) = f(-2) = 4$）、全射でない（$f(x) = -1$ の解なし）。

---

## 合成関数

$f: A \to B$、$g: B \to C$ のとき、**合成関数** $g \circ f: A \to C$ を

$$(g \circ f)(x) = g(f(x))$$

で定義します。「$f$ を先に、次に $g$ を適用する」。

**例**：$f(x) = x^2$、$g(x) = x + 1$ のとき $(g \circ f)(x) = x^2 + 1$。

一般に $g \circ f \neq f \circ g$（合成の順序は交換できない）。

---

## 逆関数

$f: A \to B$ が全単射のとき、$g(f(x)) = x$ かつ $f(g(y)) = y$ を満たす $g: B \to A$ が一意に存在します。これを**逆関数** $f^{-1}$ といいます。

**例**：$f(x) = 2x + 1$ の逆関数は $f^{-1}(y) = \frac{y-1}{2}$。

グラフでは $y = f(x)$ と $y = f^{-1}(x)$ は直線 $y = x$ に関して対称です。

---

## 単調性・有界性

**単調増加**：$x_1 < x_2 \Rightarrow f(x_1) < f(x_2)$\
**単調減少**：$x_1 < x_2 \Rightarrow f(x_1) > f(x_2)$

**上に有界**：$f(x) \leq M$ を満たす $M$ が存在する\
**下に有界**：$f(x) \geq m$ を満たす $m$ が存在する

---

## 関連ページ

- [極限（標準）](../limits/standard.md)
- [集合（標準）](../../foundations/sets/standard.md)
- [一次関数（標準）](../../specific-functions/linear/standard.md)
