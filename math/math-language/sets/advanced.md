---
title: 集合（発展）
description: "ものの集まりを数学で扱う（発展）"
difficulty: 2
tags: [math,math-language,sets,advanced]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数学の言語
    href: /math/math-language/index.html
  - text: 集合（発展）
    href: /math/math-language/sets/advanced.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
  - text: 専門
    href: professional.html
---







# 集合
「クラスの生徒全員」「5 以下の自然数」——こうした「ものの集まり」を数学的に扱う道具が**集合**です。

## このページで扱うこと
- 集合の書き方
- 和集合・共通部分・補集合
- 写像の概念

## 前提知識
- [自然数](professional.md)

---

## 集合の書き方

$$A = \{1, 2, 3, 4, 5\}$$
$$B = \{x \mid x \text{ は 10 以下の偶数}\} = \{2, 4, 6, 8, 10\}$$

$3 \in A$（3 は $A$ の要素）、$6 \notin A$（6 は $A$ の要素でない）。

---

## よく使う集合

| 記号 | 集合 |
|------|------|
| $\mathbb{N}$ | 自然数 |
| $\mathbb{Z}$ | 整数 |
| $\mathbb{Q}$ | 有理数 |
| $\mathbb{R}$ | 実数 |
| $\emptyset$ | 空集合 |

---

## 集合の演算

**和集合**（どちらかに属する）：$A \cup B$

**共通部分**（両方に属する）：$A \cap B$

**補集合**（$A$ に属さない）：$A^c$

**ド・モルガンの法則**：

$$(A \cup B)^c = A^c \cap B^c, \quad (A \cap B)^c = A^c \cup B^c$$

---

## 写像

集合 $A$ の各要素に集合 $B$ の要素を対応させる規則が**写像**です。関数もこの一種です。

---

## 関連ページ

- [必要・十分条件](professional.md)
- [場合の数](professional.md)
- [集合（専門）](professional.md) — ZFC 公理・順序数・基数
