---
title: 必要・十分条件
description: "述語論理・証明論・モデル理論の入口"
tags: [math,math-language,conditions]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数学の言語
    path: /math/math-language/index.md
  - title: 必要・十分条件
    path: /math/math-language/conditions/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 必要・十分条件
    path: /math/math-language/conditions/introduction.md
  - title: 集合（専門）
    path: ../sets/professional.md
---

## 命題論理

**命題**とは真偽が定まる文です。\
命題 $P$、$Q$ から複合命題を構成します。

| 記号 | 読み方 | 真になる条件 |
|------|--------|------------|
| $\neg P$ | Pでない | $P$ が偽のとき |
| $P \wedge Q$ | PかつQ | $P$ も $Q$ も真のとき |
| $P \vee Q$ | PまたはQ | 少なくとも一方が真のとき |
| $P \Rightarrow Q$ | PならばQ | $P$ が真かつ $Q$ が偽でないとき |
| $P \Leftrightarrow Q$ | PとQは同値 | 真偽が一致するとき |

**真理値表（$P \Rightarrow Q$）**：

| $P$ | $Q$ | $P \Rightarrow Q$ |
|-----|-----|-------------------|
| T | T | T |
| T | F | **F** |
| F | T | T |
| F | F | T |

「$P$ が偽のとき $P \Rightarrow Q$ は真」——これは「偽からは何でも導ける」という論理的慣習です。

---

## 一階述語論理

命題論理を拡張し、変数と量化子を導入します。

- $\forall x\, P(x)$：「すべての $x$ について $P(x)$ が成り立つ」
- $\exists x\, P(x)$：「$P(x)$ が成り立つ $x$ が存在する」

**例**：

$$\forall x \in \mathbb{R},\ x^2 \geq 0 \quad \text{（真）}$$
$$\exists x \in \mathbb{R},\ x^2 = -1 \quad \text{（偽）}$$

**量化子の否定**：

$$\neg(\forall x\, P(x)) \iff \exists x\, \neg P(x)$$
$$\neg(\exists x\, P(x)) \iff \forall x\, \neg P(x)$$

---

## ゲーデルの不完全性定理

**第一不完全性定理**：ペアノ算術（PA）を含む十分強い無矛盾な公理系には、\
「その公理系では証明も反証もできない命題」が存在します。

**第二不完全性定理**：そのような公理系は自身の無矛盾性を証明できません。

これは「数学は完全に形式化できない」ことを示す20世紀数学の最重要結果の一つです。

**参考文献**：Gödel, K. (1931). "Über formal unentscheidbare Sätze der Principia Mathematica und verwandter Systeme I." *Monatshefte für Mathematik und Physik*, 38, 173–198.

---

## 関連ページ

- [必要・十分条件](standard.md)
- [集合（専門）](../sets/professional.md)
