---
title: 小数
description: "実数の完備性・デデキント切断・コーシー列"
tags: [math,numbers,decimals]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 数
    url: /math/numbers/index.html
  - title: 小数
    url: /math/numbers/decimals/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: 分数（専門）
    url: ../fractions/professional.md
  - title: 数列（専門）
    url: ../../functions/sequences/professional.md
  - title: 集合
    url: /math/math-language/sets/introduction
---


> この記事は [標準](standard.md) の続きです。先に標準を読むことを推奨します。

実数の厳密な構成と完備性について扱います。  
基礎は[小数（入門）](introduction.md)を参照してください。

## このページで扱うこと
- デデキント切断による実数の構成
- コーシー列による実数の構成
- 実数の完備性と連続性

---

## デデキント切断

実数を「有理数の切断」として定義します。

有理数の集合 $A, B$（$A \cup B = \mathbb{Q}$, $A \cap B = \emptyset$）で  
$a \in A, b \in B \Rightarrow a < b$ を満たすとき、組 $(A, B)$ を**デデキント切断**といいます。

$$\sqrt{2} = (A, B),\quad A = \{q \in \mathbb{Q} \mid q < 0 \text{ または } q^2 < 2\}$$

---

## コーシー列による構成

有理数のコーシー列 $\{a_n\}$（任意の $\varepsilon > 0$ に対し $|a_m - a_n| < \varepsilon$）の同値類として実数を定義します。

$$\sqrt{2} \leftrightarrow \left\{1, 1.4, 1.41, 1.414, \ldots\right\}$$

---

## 完備性公理

実数の最も重要な性質：**上に有界な空でない集合は上限（sup）を持つ**。

$$A = \{x \in \mathbb{R} \mid x^2 < 2\} \implies \sup A = \sqrt{2} \in \mathbb{R}$$

$\mathbb{Q}$ ではこの性質が成り立ちません（$\sqrt{2} \notin \mathbb{Q}$）。

---

## 関連ページ

- [小数](introduction.md)
- [極限（専門）](../../functions/limits/professional.md)
- [数列（専門）](../../functions/sequences/professional.md)
