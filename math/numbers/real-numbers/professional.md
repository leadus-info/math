---
title: 実数
description: "実数の公理的構成——デデキント切断とコーシー列"
goal: "デデキント切断とコーシー列による実数の2つの構成を説明し、両者が同型であることを述べられるようになる"
tags: [math,numbers,real-numbers]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 実数
    path: /math/numbers/real-numbers/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 実数（標準）
    path: /math/numbers/real-numbers/standard.md
  - title: 分数（専門）
    path: /math/numbers/fractions/professional.md
  - title: 集合（専門）
    path: /math/foundations/sets/professional.md
---

## デデキント切断による構成

有理数の全体を2つの空でない部分集合 $A$, $B$ に分割し、$a \in A$, $b \in B$ ならば $a < b$ が成り立つとき、組 $(A, B)$ を**デデキント切断**といいます。

**定義**：実数 $\mathbb{R}$ をデデキント切断全体の集合として定義します。

有理数 $q$ は切断 $A = \{x \in \mathbb{Q} : x < q\}$, $B = \{x \in \mathbb{Q} : x \geq q\}$ と対応します。

無理数 $\sqrt{2}$ は $A = \{x \in \mathbb{Q} : x < 0 \text{ または } x^2 < 2\}$, $B = \{x \in \mathbb{Q} : x > 0 \text{ かつ } x^2 \geq 2\}$ という切断として表現されます。

**演算の定義**：切断の加法・乗法を定義し、順序・体の公理がすべて満たされることを確認します。上限の存在は切断の定義から直接従います。

**参考文献**：Dedekind, R. (1872). *Stetigkeit und irrationale Zahlen*. Vieweg.

---

## コーシー列による構成

有理数のコーシー列 $\{a_n\}$：任意の $\varepsilon > 0$ に対して $N$ が存在し、$m, n > N \Rightarrow |a_m - a_n| < \varepsilon$。

2つのコーシー列 $\{a_n\}$, $\{b_n\}$ を同値とする関係：

$$\{a_n\} \sim \{b_n\} \iff \lim_{n \to \infty}|a_n - b_n| = 0$$

**定義**：実数 $\mathbb{R}$ を有理コーシー列の同値類の全体として定義します。

$\sqrt{2}$ は $1, 1.4, 1.41, 1.414, \ldots$ というコーシー列の同値類として現れます。

---

## 2つの構成の同値性

デデキント切断による $\mathbb{R}$ とコーシー列による $\mathbb{R}$ は、順序体として同型です。

さらに、次の意味で $\mathbb{R}$ は本質的に一意です：

**定理**：完備順序体は同型を除いて一意に存在します。

証明の概略：任意の完備順序体には $\mathbb{Q}$ を部分体として含み（$\mathbb{Z}$ の構造から自然に埋め込まれる）、完備性により $\mathbb{Q}$ のコーシー列の収束先がすべて存在するため、構造が一意に決まります。

---

## アルキメデス性

**定理**：任意の実数 $x > 0$ と $y > 0$ に対して、$nx > y$ となる自然数 $n$ が存在します。

**証明**：$nx \leq y$ がすべての $n$ で成り立つとすると、$\{nx : n \in \mathbb{N}\}$ は上に有界。上限 $s$ が存在し、$s - x$ は上限でないから $nx > s - x$ となる $n$ が存在します。すると $(n+1)x > s$ で上限に矛盾。$\square$

アルキメデス性から $\mathbb{Q}$ が $\mathbb{R}$ で稠密（任意の実数を有理数で任意精度に近似できる）ことが従います。

**参考文献**：Rudin, W. (1976). *Principles of Mathematical Analysis* (3rd ed.). McGraw-Hill.

---

## 関連ページ

- [実数（標準）](standard.md)
- [極限（専門）](../../analysis/limits/professional.md)
- [集合（専門）](../../foundations/sets/professional.md)
