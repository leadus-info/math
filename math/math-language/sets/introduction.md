---
title: 集合
description: "ものの集まりを数学で扱う"
tags: [math,math-language,sets]
level: introduction
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 数学の言語
    url: /math/math-language/index.html
  - title: 集合
    url: /math/math-language/sets/introduction.html
levels:
  - level: introduction
  - level: standard
    url: standard.html
  - level: professional
    url: professional.html

requires:
  - title: 自然数
    url: /math/numbers/natural-numbers/introduction
  - title: 必要・十分条件
    url: /math/math-language/conditions/introduction
---



「クラスの生徒全員」「10以下の偶数」——
こういった「ものの集まり」を数学的に扱う道具が**集合**です。

---

## 集合とは

要素がはっきり決まる「ものの集まり」が集合です。

「背の高い人の集合」は曖昧なので集合ではありません（どこから「高い」か不明）。
「身長180cm以上の人の集合」は明確なので集合です。

---

## 集合の書き方

$A = \{1, 2, 3, 4, 5\}$

3は $A$ に含まれる → $3 \in A$
6は $A$ に含まれない → $6 
otin A$

---

## 集合の演算

**和集合**（AまたはBに含まれる）
$A \cup B$

**共通部分**（AかつBに含まれる）
$A \cap B$

**補集合**（全体のうちAに含まれない部分）
$A^c$

---

## 集合と論理の対応

「$x \in A$ ならば $x \in B$」は「$A$ は $B$ の部分集合」($A \subset B$)。
条件（論理）と集合は深く対応しています。

---

## 関連ページ

- [必要・十分条件](../conditions/introduction.md)
- [場合の数](../../statistics/counting/introduction.md)
