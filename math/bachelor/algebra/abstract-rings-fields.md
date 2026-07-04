---
title: 環と体
description: "2つの演算を持つ構造"
goal: "環・整域・体の定義とその包含関係を理解できるようになる"
tags: [math, algebra, abstract]
stage: 発展編
subject: 代数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 発展編
    path: /math/bachelor/index.md
  - title: 環と体
    path: /math/bachelor/algebra/abstract-rings-fields.md
requires:
  - title: 群
    path: abstract-groups.md
---

## 環と体の定義

群に2つ目の演算（掛け算）を加えた構造が**環**、さらに $0$ 以外の全要素に乗法逆元がある可換環が**体**です。

**環** $(R, +, \cdot)$：$(R, +)$ が可換群、$\cdot$ について結合律・分配律が成立。

**整域**：零因子を持たない可換単位環（$ab=0 \Rightarrow a=0$ または $b=0$）。

$$\text{体} \subset \text{整域} \subset \text{可換環} \subset \text{環}$$

整数 $\mathbb{Z}$ は環（割り算はできないことがある）、有理数 $\mathbb{Q}$・実数 $\mathbb{R}$・複素数 $\mathbb{C}$ は体（自由に四則演算できる）です。

---

## まとめ

環は群に掛け算を加えた構造で、体は環の中でも0以外のすべての要素に乗法逆元がある特別な場合です。体・整域・可換環・環はこの順に包含関係にあります。

---

## 関連ページ

- [群（発展編）](abstract-groups.md)
- [準同型・同型（発展編）](abstract-homomorphisms.md)
