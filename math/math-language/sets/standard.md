---
title: 集合
description: "ものの集まりを数学で扱う"
difficulty: 1
tags: [math,math-language,sets]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数学の言語
    href: /math/math-language/index.html
  - text: 集合
    href: /math/math-language/sets/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 集合
「クラスの女子全員」「10 以下の偶数」——こういった「ものの集まり」を数学的に扱う道具が**集合**です。

## このページで扱うこと
- 集合の書き方
- 部分集合（含まれる関係）
- 和集合・共通部分・補集合

## 前提知識
- [自然数](../../numbers/natural-numbers/standard.md)

---

## 集合の書き方

要素を $\{\ \}$ で囲んで書きます。

$$A = \{1, 2, 3, 4, 5\}$$

「$3$ は $A$ の要素」→ $3 \in A$
「$6$ は $A$ の要素でない」→ $6 \notin A$

条件で書くこともできます。

$$B = \{x \mid x \text{ は } 10 \text{ 以下の偶数}\} = \{2, 4, 6, 8, 10\}$$

---

## よく使う集合

| 記号 | 意味 |
|------|------|
| $\mathbb{N}$ | 自然数全体 |
| $\mathbb{Z}$ | 整数全体 |
| $\mathbb{Q}$ | 有理数（分数）全体 |
| $\mathbb{R}$ | 実数全体 |
| $\emptyset$ | 何も入っていない集合（空集合） |

$$\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R}$$

---

## 集合の演算

**和集合**（どちらかに入っている）：$A \cup B$

$$A = \{1,2,3\},\ B = \{2,3,4\} \implies A \cup B = \{1,2,3,4\}$$

**共通部分**（両方に入っている）：$A \cap B$

$$A \cap B = \{2,3\}$$

**補集合**（全体から $A$ を除いたもの）：$A^c$

全体を $U = \{1,2,3,4,5\}$ とすると $A^c = \{4,5\}$

---

## ド・モルガンの法則

$$(A \cup B)^c = A^c \cap B^c$$
$$(A \cap B)^c = A^c \cup B^c$$

「AまたはBでない」＝「Aでない かつ Bでない」という直感に対応します。

---

## 関連ページ

- [必要・十分条件](../conditions/standard.md)
- [場合の数](../../statistics/counting/standard.md)
- [集合（発展）](../sets/advanced.md) — より詳しく学ぶ
