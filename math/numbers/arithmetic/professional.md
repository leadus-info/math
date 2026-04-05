---
title: 四則演算
description: "群・環・体の代数的構造"
tags: [math,operations,arithmetic]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 乗法・べき乗
    path: /math/numbers/arithmetic/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 乗法・べき乗
    path: /math/numbers/arithmetic/introduction.md
  - title: 集合
    path: /math/math-language/sets/introduction.md
  - title: 負数（専門）
    path: ../../numbers/negative-numbers/professional.md
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
