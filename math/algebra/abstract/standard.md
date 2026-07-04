---
title: 抽象代数
description: "群・環・体の定義と基本定理"
goal: "群・環・体を公理で定義し、準同型・部分群・商群の概念を理解して基本的な例を分類できるようになる"
tags: [math,algebra,abstract]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 代数
    path: /math/algebra/index.md
  - title: 抽象代数
    path: /math/algebra/abstract/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 抽象代数（入門）
    path: /math/algebra/abstract/introduction.md
  - title: 証明法（標準）
    path: /math/foundations/proofs/standard.md
  - title: 集合（標準）
    path: /math/foundations/sets/standard.md
---

## 群の定義

集合 $G$ と二項演算 $\cdot: G \times G \to G$ の組 $(G, \cdot)$ が**群**であるとは：

1. **結合律**：$(a \cdot b) \cdot c = a \cdot (b \cdot c)$
2. **単位元**：$e \cdot a = a \cdot e = a$ を満たす $e \in G$ が存在する
3. **逆元**：各 $a$ に対し $a \cdot a^{-1} = a^{-1} \cdot a = e$ を満たす $a^{-1}$ が存在する

$a \cdot b = b \cdot a$ が成り立つとき**可換群**（アーベル群）といいます。

| 群 | 演算 | 単位元 |
|----|------|--------|
| $(\mathbb{Z}, +)$ | 足し算 | $0$ |
| $(\mathbb{Q}\setminus\{0\}, \times)$ | 掛け算 | $1$ |
| $(\mathbb{Z}/n\mathbb{Z}, +)$ | 剰余の足し算 | $[0]$ |

---

## 部分群と剰余類

$H \subset G$ が $G$ の**部分群**であるとは、$H$ 自身が $G$ の演算のもとで群をなすことです。

**ラグランジュの定理**：有限群 $G$ の部分群 $H$ について $|H|$ は $|G|$ を割り切ります。

$a \in G$ に対する $H$ の**左剰余類**：$aH = \{ah \mid h \in H\}$

$H$ が $G$ の**正規部分群**（$gHg^{-1} = H$、$\forall g$）のとき、剰余類全体 $G/H$ が自然に群をなします（**商群**）。

---

## 環と体

**環** $(R, +, \cdot)$：$(R, +)$ が可換群、$\cdot$ について結合律・分配律が成立。

**整域**：零因子を持たない可換単位環（$ab = 0 \Rightarrow a=0$ または $b=0$）。

**体**：$0$ 以外の全元が乗法逆元を持つ可換単位環。

$$\text{体} \subset \text{整域} \subset \text{可換環} \subset \text{環}$$

---

## 準同型と同型

**群準同型** $\varphi: G \to H$：$\varphi(ab) = \varphi(a)\varphi(b)$ を満たす写像。

- **核**：$\ker \varphi = \{g \in G : \varphi(g) = e_H\}$（正規部分群）
- **像**：$\mathrm{Im}\, \varphi = \{\varphi(g) : g \in G\}$（$H$ の部分群）

**準同型定理**：$G / \ker \varphi \cong \mathrm{Im}\, \varphi$

全単射な準同型を**同型**（$G \cong H$）といいます。同型な群は代数的に区別できません。

---

## 巡回群

1つの元 $g$ で生成される群 $\langle g \rangle = \{\ldots, g^{-2}, g^{-1}, e, g, g^2, \ldots\}$ を**巡回群**といいます。

- 位数 $n$ の有限巡回群は $\mathbb{Z}/n\mathbb{Z}$ と同型
- 無限巡回群は $\mathbb{Z}$ と同型

---

## 関連ページ

- [乗法・べき乗（専門）](../../numbers/arithmetic/professional.md)
- [多項式（専門）](../polynomials/professional.md)
- [行列（標準）](../../linear-algebra/matrices/standard.md) — 行列のなす群
