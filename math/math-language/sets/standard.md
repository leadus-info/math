---
title: 集合
description: "ものの集まりを数学で扱う"
tags: [math,math-language,sets]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 数学の言語
    path: /math/math-language/index.html
  - title: 集合
    path: /math/math-language/sets/standard.html
levels:
  - level: introduction
    path: introduction.html
  - level: standard
  - level: professional
    path: professional.html
level: standard
requires:
  - title: 自然数
    path: /math/numbers/natural-numbers/introduction
---



「ものの集まり」を数学的に扱う道具が集合です。
現代数学のほぼすべての概念は集合の言葉で記述されます。

## 集合の定義

要素がはっきり決まる「ものの集まり」を**集合**といいます。

$$A = \{1, 2, 3, 4, 5\}$$
$$B = \{x \mid x \text{ は 10 以下の偶数}\} = \{2, 4, 6, 8, 10\}$$

$3 \in A$（3 は $A$ の要素）、$6 \notin A$（6 は $A$ の要素でない）。

「背の高い人の集合」は要素が曖昧なので数学的な集合として扱えません。
要素かどうかが明確に判定できることが条件です。

---

## よく使う集合

| 記号 | 内容 |
|------|------|
| $\mathbb{N}$ | 自然数全体 $\{1, 2, 3, \ldots\}$ |
| $\mathbb{Z}$ | 整数全体 $\{\ldots, -2, -1, 0, 1, 2, \ldots\}$ |
| $\mathbb{Q}$ | 有理数全体（分数で表せる数） |
| $\mathbb{R}$ | 実数全体 |
| $\emptyset$ | 空集合（要素が一つもない集合） |

$$\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R}$$

---

## 集合の演算

**和集合**（少なくとも一方に属する）：

$$A \cup B = \{x \mid x \in A \text{ または } x \in B\}$$

**共通部分**（両方に属する）：

$$A \cap B = \{x \mid x \in A \text{ かつ } x \in B\}$$

**補集合**（全体 $U$ のうち $A$ に属さない）：

$$A^c = \{x \in U \mid x \notin A\}$$

**部分集合**：$A$ のすべての要素が $B$ にも属するとき $A \subset B$。

---

## ド・モルガンの法則

$$(A \cup B)^c = A^c \cap B^c$$
$$(A \cap B)^c = A^c \cup B^c$$

「AまたはBでない」＝「Aでない かつ Bでない」という直感に対応します。

---

## 写像

集合 $A$ の各要素に集合 $B$ の要素をただ一つ対応させる規則を**写像**といいます。
関数は写像の特別な場合（$A, B$ が数の集合）です。

$$f: A \to B, \quad f(x) = x^2$$

写像において「$A$ のすべての要素が対応先を持つ」ことが重要で、
「$B$ のすべての要素が対応元を持つ」かどうかは別の話（全射）です。

---

## 集合と論理の対応

「条件 $P(x)$」と「集合 $\{x \mid P(x)\}$」は対応します。

- $P \Rightarrow Q$（「PならばQ」）$\Leftrightarrow$ $\{x \mid P(x)\} \subset \{x \mid Q(x)\}$
- $P \Leftrightarrow Q$（同値）$\Leftrightarrow$ $\{x \mid P(x)\} = \{x \mid Q(x)\}$

---

## 関連ページ

- [必要・十分条件](../conditions/introduction.md)
- [場合の数](../../statistics/counting/introduction.md)
