---
title: 場合の数
description: "母関数・包除原理・ラムゼー理論"
goal: "母関数・包除原理を使って数列や計数問題を解き、ラムゼー数 R(3,3)=6 を証明できるようになる"
tags: [math,probability,counting]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 確率
    path: /math/probability/index.md
  - title: 場合の数
    path: /math/probability/counting/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 場合の数（標準）
    path: /math/probability/counting/standard.md
  - title: 自然数（専門）
    path: /math/numbers/natural-numbers/professional.md
---

## 母関数

数列 $\{a_n\}$ に対する**普通母関数**：$G(x) = \sum_{n=0}^\infty a_n x^n$

数列の情報を形式的べき級数に「圧縮」し、代数的操作で数列の性質を調べます。

**二項係数の母関数**（二項定理）：$\sum_{k=0}^n \binom{n}{k} x^k = (1+x)^n$

**カタラン数** $C_n$（$n$ 組の括弧の正しい組み合わせ数など）：

$$C_0=1,\ C_1=1,\ C_2=2,\ C_3=5,\ C_4=14,\ldots,\quad C_n = \frac{1}{n+1}\binom{2n}{n}$$

母関数：$G(x) = \frac{1 - \sqrt{1-4x}}{2x}$（$G = 1 + xG^2$ から導く）

---

## 包除原理

**定理**：有限集合 $A_1, \ldots, A_n$ について：

$$\left|\bigcup_{i=1}^n A_i\right| = \sum_i |A_i| - \sum_{i<j} |A_i \cap A_j| + \sum_{i<j<k} |A_i \cap A_j \cap A_k| - \cdots$$

**撹乱順列**（不動点を持たない順列）の個数：

$$D_n = n! \sum_{k=0}^n \frac{(-1)^k}{k!}$$

$$D_1=0,\ D_2=1,\ D_3=2,\ D_4=9,\ D_5=44,\ldots$$

$n \to \infty$ で $D_n / n! \to 1/e \approx 0.368$。

---

## ラムゼー理論

$R(m, n)$：$m$ クリーク（完全部分グラフ）または $n$ 独立集合を必ず含む最小頂点数のグラフ。

**定理**：$R(3, 3) = 6$（6人いれば「互いに知り合い3人」または「互いに他人3人」が必ず存在）

**証明**：任意の1人 $X$ を選びます。残り5人との関係は「知り合い」または「他人」。鳩の巣原理より少なくとも3人は同じ関係にあります。

- 「知り合い3人 $\{A,B,C\}$」の場合：$A, B$ が知り合いなら $\{X, A, B\}$ が求める3人。$A, B$ が他人なら $\{A, B, C\}$ 内に「他人3人」を探せる（帰納的に確認）。
- 「他人3人」の場合も同様。

5人では成立しません（反例グラフ：5頂点のペンタゴン $C_5$）。

**参考文献**：Graham, R. L., Rothschild, B. L., & Spencer, J. H. (1990). *Ramsey Theory* (2nd ed.). Wiley.

---

## 関連ページ

- [場合の数（標準）](standard.md)
- [確率（専門）](../probability/professional.md)
