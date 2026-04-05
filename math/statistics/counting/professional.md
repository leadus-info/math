---
title: 場合の数
description: "母関数・包除原理・ラムゼー理論"
tags: [math,statistics,counting]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 統計・確率
    path: /math/statistics/index.md
  - title: 場合の数
    path: /math/statistics/counting/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 場合の数
    path: /math/statistics/counting/introduction.md
  - title: 数列（専門）
    path: ../../functions/sequences/professional.md
  - title: 集合（専門）
    path: ../../math-language/sets/professional.md
---

## 母関数

数列 $\{a_n\}$ に対する**普通母関数**：

$$G(x) = \sum_{n=0}^{\infty} a_n x^n$$

母関数は数列の情報を関数の形に「圧縮」します。\
数列の演算が母関数上の代数的操作に対応します。

**例（二項係数の母関数）**：

$$\sum_{k=0}^{n}\binom{n}{k}x^k = (1+x)^n$$

これは二項定理そのものです。

**カタラン数**：$C_n = \frac{1}{n+1}\binom{2n}{n}$（括弧の正しい入れ方の数など）の母関数：

$$G(x) = \frac{1 - \sqrt{1-4x}}{2x}$$

---

## 包除原理

**定理**：有限集合 $A_1, \ldots, A_n$ について：

$$\left|A_1 \cup \cdots \cup A_n\right| = \sum_i |A_i| - \sum_{i<j}|A_i \cap A_j| + \sum_{i<j<k}|A_i \cap A_j \cap A_k| - \cdots$$

**撹乱順列（完全順列）**：$n$ 要素の順列で、どの要素も元の位置にないものの個数：

$$D_n = n!\sum_{k=0}^{n}\frac{(-1)^k}{k!}$$

$$D_1=0,\ D_2=1,\ D_3=2,\ D_4=9,\ D_5=44,\ldots$$

$n \to \infty$ で $D_n/n! \to 1/e \approx 0.368$。

---

## ラムゼー理論

**ラムゼーの定理（$R(3,3) = 6$）**：\
6人の中には「互いに知り合い3人」または「互いに知らない3人」が必ず存在します。

**証明**：任意の1人（$X$）に注目します。残り5人との関係は知り合い・他人の2種類。\
鳩の巣原理から少なくとも3人は同じ関係にあります。\
その3人の中に知り合いのペアがあればその3人で「知り合い3人組」が完成し、\
なければその3人全員が互いに他人です。

$R(3,3) = 6$ は厳密に最小で、5人では保証されません（グラフで反例が作れます）。

**参考文献**：Graham, R. L., Rothschild, B. L., & Spencer, J. H. (1990). *Ramsey Theory* (2nd ed.). Wiley.

---

## 関連ページ

- [場合の数](standard.md)
- [確率（専門）](../probability/professional.md)
