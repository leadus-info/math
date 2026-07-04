---
title: 集合
description: "集合の演算・写像・主な集合"
goal: "集合の記法・演算法則・写像の概念を理解し、数の集合の包含関係を説明できるようになる"
tags: [math,foundations,sets]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 基礎
    path: /math/foundations/index.md
  - title: 集合
    path: /math/foundations/sets/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 集合（入門）
    path: /math/foundations/sets/introduction.md
  - title: 自然数（標準）
    path: /math/numbers/natural-numbers/standard.md
---

## 集合の記法

集合を表す記法は2種類あります。

**列挙記法**：要素を直接並べる。$A = \{1, 2, 3, 4, 5\}$

**内包記法**：条件で定義する。$B = \{x \mid x \text{ は10以下の偶数}\} = \{2, 4, 6, 8, 10\}$

$3 \in A$（3は $A$ の要素）、$6 \notin A$（6は $A$ の要素でない）。

---

## よく使う集合

| 記号 | 集合 | 例 |
|------|------|----|
| $\mathbb{N}$ | 自然数全体 | $\{1, 2, 3, \ldots\}$ |
| $\mathbb{Z}$ | 整数全体 | $\{\ldots, -2, -1, 0, 1, 2, \ldots\}$ |
| $\mathbb{Q}$ | 有理数全体 | $\frac{p}{q}$（$q \neq 0$）の形 |
| $\mathbb{R}$ | 実数全体 | 数直線上のすべての点 |
| $\emptyset$ | 空集合 | 要素が1つもない集合 |

包含関係：$\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R}$

---

## 演算の法則

集合の演算には以下の法則が成り立ちます。

**交換律**：$A \cup B = B \cup A$、$A \cap B = B \cap A$

**結合律**：$(A \cup B) \cup C = A \cup (B \cup C)$

**分配律**：$A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$

**ド・モルガンの法則**：

$$(A \cup B)^c = A^c \cap B^c, \quad (A \cap B)^c = A^c \cup B^c$$

「AまたはBでない」$=$ 「Aでない かつ Bでない」という直感に対応します。

---

## 写像

集合 $A$ の各要素に集合 $B$ の要素をただ一つ対応させる規則を**写像**といいます。

$$f: A \to B, \quad a \mapsto f(a)$$

- $A$：**定義域**、$B$：**終域**
- $\{f(a) \mid a \in A\}$：**値域**（終域の部分集合）

**単射**（一対一）：$f(a) = f(b) \Rightarrow a = b$（異なる入力は異なる出力）

**全射**（上への写像）：任意の $b \in B$ に対して $f(a) = b$ となる $a \in A$ が存在する

**全単射**（両方）：単射かつ全射——$A$ と $B$ の間に完全な1対1対応がある

---

## 関連ページ

- [必要・十分条件（標準）](../logic/standard.md)
- [集合（専門）](professional.md)
