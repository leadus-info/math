---
title: 群
description: "演算の最も基本的な構造"
goal: "群の定義を公理から理解し、部分群・剰余類・商群を説明できるようになる"
tags: [math, algebra, abstract]
stage: 発展編
subject: 代数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 発展編
    path: /math/bachelor/index.md
  - title: 群
    path: /math/bachelor/algebra/abstract-groups.md
requires:
  - title: 抽象代数
    path: abstract.md
---

## 群の定義

集合 $G$ と二項演算 $\cdot: G \times G \to G$ の組 $(G, \cdot)$ が**群**であるとは、次の3条件を満たすことです。

1. **結合律**：$(a \cdot b) \cdot c = a \cdot (b \cdot c)$
2. **単位元**：$e \cdot a = a \cdot e = a$ を満たす $e \in G$ が存在する
3. **逆元**：各 $a$ に対し $a \cdot a^{-1} = a^{-1} \cdot a = e$ を満たす $a^{-1}$ が存在する

$a \cdot b = b \cdot a$ が成り立つとき**可換群**（アーベル群）といいます。

| 群 | 演算 | 単位元 |
|----|------|--------|
| $(\mathbb{Z}, +)$ | 足し算 | $0$ |
| $(\mathbb{Q}\setminus\{0\}, \times)$ | 掛け算 | $1$ |
| $(\mathbb{Z}/n\mathbb{Z}, +)$ | 剰余の足し算 | $[0]$ |

---

## 部分群と剰余類

$H \subset G$ が $G$ の**部分群**であるとは、$H$ 自身が $G$ の演算のもとで群をなすことです。

**ラグランジュの定理**：有限群 $G$ の部分群 $H$ について、$|H|$ は $|G|$ を割り切る。

$a \in G$ に対する $H$ の**左剰余類**を $aH = \{ah \mid h \in H\}$ で定義します。$H$ が $G$ の**正規部分群**（$gHg^{-1} = H$、$\forall g$）のとき、剰余類全体 $G/H$ が自然に群をなします（**商群**）。

---

## まとめ

群は、結合律・単位元・逆元の3条件を満たす集合と演算の組です。部分群のうち正規部分群は、剰余類全体に自然な群構造（商群）を与えます。

---

## 関連ページ

- [抽象代数（発展編）](abstract.md)
- [環と体（発展編）](abstract-rings-fields.md)
