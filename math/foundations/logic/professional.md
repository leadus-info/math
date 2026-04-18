---
title: 必要・十分条件
description: "一階述語論理と証明論"
goal: "一階述語論理の構文・意味論を理解し、健全性・完全性定理の内容と、ゲーデルの不完全性定理の帰結を説明できるようになる"
tags: [math,foundations,logic]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 基礎
    path: /math/foundations/index.md
  - title: 必要・十分条件
    path: /math/foundations/logic/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 必要・十分条件（標準）
    path: /math/foundations/logic/standard.md
  - title: 集合（専門）
    path: /math/foundations/sets/professional.md
---

## 一階述語論理

**命題論理**では $P, Q$ を原子命題として扱いましたが、**一階述語論理（FOL）** では個体と述語を導入します。

- 個体変数：$x, y, z, \ldots$
- 述語記号：$P(x)$（「$x$ は偶数」など）
- 量化子：$\forall$（全称）、$\exists$（存在）

$$\forall x \in \mathbb{N},\ \exists y \in \mathbb{N},\ y > x \quad \text{（自然数には最大値がない）}$$

量化子の否定：

$$\neg (\forall x\, P(x)) \equiv \exists x\, \neg P(x)$$
$$\neg (\exists x\, P(x)) \equiv \forall x\, \neg P(x)$$

---

## 健全性と完全性

公理系 $T$ と論理的推論規則の下で、

- **健全性**（soundness）：$T \vdash \varphi \Rightarrow T \models \varphi$（証明できれば恒真）
- **完全性**（completeness）：$T \models \varphi \Rightarrow T \vdash \varphi$（恒真なら証明できる）

ゲーデルの完全性定理（1930）：一階述語論理の自然な公理系は健全かつ完全です。すなわち「論理的に真な文はすべて証明できる」。

**参考文献**：Gödel, K. (1930). "Die Vollständigkeit der Axiome des logischen Funktionenkalküls." *Monatshefte für Mathematik und Physik*, 37, 349–360.

---

## ゲーデルの不完全性定理

自然数の算術を含む「十分強い」無矛盾な公理系 $T$ について（1931）：

**第一不完全性定理**：$T$ には証明も反証もできない命題が存在します。

**第二不完全性定理**：$T$ は自身の無矛盾性を $T$ の中で証明できません。

「十分強い」とは、ペアノ算術（PA）程度の表現力を持つという意味です。この定理は「数学は完全に形式化できない」ことを示し、20世紀数学に深遠な影響を与えました。

証明の核心はゲーデル数（命題を自然数にエンコードする技法）と、「この命題は証明できない」を表す自己言及的命題の構成にあります。

**参考文献**：Gödel, K. (1931). "Über formal unentscheidbare Sätze der Principia Mathematica und verwandter Systeme I." *Monatshefte für Mathematik und Physik*, 38, 173–198.

---

## 関連ページ

- [必要・十分条件（標準）](standard.md)
- [集合（専門）](../sets/professional.md)
- [自然数（専門）](../../numbers/natural-numbers/professional.md)
