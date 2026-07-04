---
title: 集合
description: "ものの集まりを数学で扱う"
goal: "集合の意味を理解し、和集合・共通部分・補集合を具体例で説明できるようになる"
tags: [math,foundations,sets]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 基礎
    path: /math/foundations/index.md
  - title: 集合
    path: /math/foundations/sets/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 自然数（入門）
    path: /math/numbers/natural-numbers/introduction.md
---

## 「ものの集まり」を扱う

「クラスの生徒全員」「今日の最高気温が30度以上だった日」——こうした「ものの集まり」を数学的に扱う道具が**集合**です。

集合で大切なのは、**何が含まれて何が含まれないかが明確なこと**です。「背の高い人の集合」は「どこから高いのか」が曖昧なので、数学的な集合としては扱いにくいです。「身長170cm以上の人の集合」なら明確です。

---

## 集合の3つの基本操作

クラスを例に考えます。
$A$：「数学が好きな生徒の集合」、$B$：「理科が好きな生徒の集合」

**和集合**（$A \cup B$）——どちらかが好きな生徒全員

**共通部分**（$A \cap B$）——両方が好きな生徒だけ

**補集合**（$A^c$）——数学が好きでない生徒（クラス全体から $A$ を除いた部分）

---

## 部分集合

「正三角形の集合」は「二等辺三角形の集合」に含まれます。正三角形はすべて二等辺三角形でもあるからです。

このように「$A$ のすべての要素が $B$ にも属する」とき、$A$ は $B$ の**部分集合**といい、$A \subset B$ と書きます。

---

## まとめ

集合は「はっきり決まるものの集まり」です。和集合・共通部分・補集合の3操作が基本で、「すべての要素が別の集合にも属する」関係が部分集合です。

---

## 関連ページ

- [必要・十分条件（入門）](../logic/introduction.md)
- [場合の数（入門）](../../probability/counting/introduction.md)
