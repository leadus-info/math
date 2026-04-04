---
title: 四則演算
description: "群・環・体の代数的構造"
tags: [math,operations,arithmetic]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数
    href: /math/numbers/index.html
  - text: 乗法・べき乗
    href: /math/numbers/arithmetic/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: 乗法・べき乗
    url: \1/introduction.md
  - title: 集合
    url: \1/introduction.md
  - title: 負数（専門）
    url: ../../numbers/negative-numbers/professional.md
---










# 四則演算（発展）
演算を抽象化した代数的構造（群・環・体）を扱います。

## このページで扱うこと
- 群・環・体の定義と例
- 準同型定理の概要
- 体上の多項式環

---

## 群（Group）

集合 $G$ と二項演算 $\cdot$ が以下を満たすとき $(G, \cdot)$ を**群**といいます。

1. **結合律**: $(a \cdot b) \cdot c = a \cdot (b \cdot c)$
2. **単位元**: $e \cdot a = a \cdot e = a$ なる $e$ が存在
3. **逆元**: 各 $a$ に対し $a \cdot a^{-1} = e$ なる $a^{-1}$ が存在

| 例 | 演算 | 群か |
|----|------|------|
| $(\mathbb{Z}, +)$ | 加算 | ○ |
| $(\mathbb{Z}, \times)$ | 乗算 | ×（逆元なし） |
| $(\mathbb{Q}\setminus\{0\}, \times)$ | 乗算 | ○ |

---

## 環（Ring）

加算について可換群をなし、乗算について結合律・分配律が成り立つ構造。

$$\mathbb{Z}, \mathbb{Q}, \mathbb{R}, \mathbb{C}, \mathbb{Z}[x]$$

---

## 体（Field）

0 以外のすべての元が乗法逆元を持つ可換環。

$$\mathbb{Q},\ \mathbb{R},\ \mathbb{C},\ \mathbb{Z}/p\mathbb{Z}\text{（}p\text{: 素数）}$$

体の上では加減乗除が自由に行えます。

---

## 準同型定理

群の準同型 $\varphi: G \to H$ に対して:

$$G / \ker(\varphi) \cong \text{Im}(\varphi)$$

---

## 関連ページ

- [乗法・べき乗](introduction.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
- [複素数（専門）](../complex-numbers/professional.md)
