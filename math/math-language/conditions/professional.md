---
title: 必要・十分条件
description: "述語論理・証明論・モデル理論の入口"
tags: [math,math-language,conditions]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 数学の言語
    path: /math/math-language/index.html
  - title: 必要・十分条件
    path: /math/math-language/conditions/professional.html
levels:
  - level: 入門
    path: introduction.html
  - level: 標準
    path: standard.html
  - level: 専門
level: 専門
requires:
  - title: 必要・十分条件
    path: /math/math-language/conditions/introduction
  - title: 集合（専門）
    path: ../sets/professional.md
---

## このページで扱うこと

述語論理・公理系・証明論の基礎を扱います。

- 一階述語論理の構文と意味論
- 健全性・完全性定理
- ゲーデルの不完全性定理の概要

---

## 一階述語論理

命題論理を拡張し、$\forall$（全称）・$\exists$（存在）量化子を導入します。

$$\forall x\,\exists y\,(x < y) \quad \text{（自然数について真）}$$

---

## 健全性・完全性定理

**健全性**: 証明可能 $\Rightarrow$ 恒真  
**完全性**（ゲーデル）: 恒真 $\Rightarrow$ 証明可能

---

## ゲーデルの不完全性定理

十分強い公理系（ペアノ算術など）において:

1. 証明も反証もできない命題が存在する
2. 自身の無矛盾性を証明できない

---

## 関連ページ

- [必要・十分条件](introduction.md)
- [集合（専門）](../sets/professional.md)
