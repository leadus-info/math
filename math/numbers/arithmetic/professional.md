---
title: 乗法・べき乗
description: "群・環・体の代数的構造"
goal: "群・環・体の公理を述べ、整数・有理数・実数をこれらの枠組みで位置づけられるようになる"
tags: [math,numbers,arithmetic]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 乗法・べき乗
    path: /math/numbers/arithmetic/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 乗法・べき乗（標準）
    path: /math/numbers/arithmetic/standard.md
  - title: 自然数（専門）
    path: /math/numbers/natural-numbers/professional.md
  - title: 集合（標準）
    path: /math/foundations/sets/standard.md
---

## 群

**定義**：集合 $G$ と二項演算 $\cdot: G \times G \to G$ の組 $(G, \cdot)$ が**群**であるとは、以下を満たすことです。

1. **結合律**：$(a \cdot b) \cdot c = a \cdot (b \cdot c)$（すべての $a,b,c \in G$）
2. **単位元の存在**：$e \cdot a = a \cdot e = a$ を満たす $e \in G$ が存在する
3. **逆元の存在**：各 $a \in G$ に対して $a \cdot a^{-1} = a^{-1} \cdot a = e$ を満たす $a^{-1} \in G$ が存在する

さらに $a \cdot b = b \cdot a$ が成り立つとき**可換群**（アーベル群）といいます。

**例**：$( \mathbb{Z}, + )$ は可換群（単位元 $0$、$n$ の逆元は $-n$）。$( \mathbb{Z}, \times )$ は群でない（$2$ に逆元が存在しない）。$( \mathbb{Q} \setminus \{0\}, \times )$ は可換群。

---

## 環

**定義**：集合 $R$ と二項演算 $+$（加法）と $\cdot$（乗法）の組 $(R, +, \cdot)$ が**環**であるとは、以下を満たすことです。

1. $(R, +)$ は可換群
2. 乗法の結合律：$(a \cdot b) \cdot c = a \cdot (b \cdot c)$
3. 分配律：$a \cdot (b + c) = a \cdot b + a \cdot c$ および $(a + b) \cdot c = a \cdot c + b \cdot c$

乗法が可換（$ab = ba$）のとき**可換環**、乗法の単位元 $1$ が存在するとき**単位的環**といいます。

**例**：$( \mathbb{Z}, +, \times )$ は可換単位的環。加法単位元は $0$、乗法単位元は $1$。

$ab = 0$ かつ $a \neq 0$、$b \neq 0$ となる元を**零因子**といいます。零因子を持たない可換単位的環を**整域**といいます。$\mathbb{Z}$ は整域です。

---

## 体

**定義**：可換単位的環 $(F, +, \cdot)$ で $0 \neq 1$ かつ $0$ 以外のすべての元が乗法逆元を持つものを**体**といいます。

体の上では加減乗除が自由に行えます。

**例**：$( \mathbb{Q}, +, \times )$、$( \mathbb{R}, +, \times )$、$( \mathbb{C}, +, \times )$ はすべて体。$( \mathbb{Z}, +, \times )$ は体でない（例えば $2$ に乗法逆元 $\frac{1}{2} \notin \mathbb{Z}$ が存在しない）。

$p$ が素数のとき、$\mathbb{Z}/p\mathbb{Z} = \{0, 1, \ldots, p-1\}$（$p$ を法とする剰余環）は体になります。

---

## 準同型定理

環の準同型 $\varphi: R \to S$（加法と乗法を保つ写像）に対して：

$$R / \ker(\varphi) \cong \mathrm{Im}(\varphi)$$

**核**：$\ker(\varphi) = \{r \in R : \varphi(r) = 0\}$（$R$ のイデアル）。

**参考文献**：Lang, S. (2002). *Algebra* (3rd ed.). Springer.

---

## 関連ページ

- [乗法・べき乗（標準）](standard.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
- [複素数（専門）](../complex-numbers/professional.md)
