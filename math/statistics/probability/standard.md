---
title: 確率
description: "起こりやすさを数値で表す"
tags: [math,statistics,probability]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 統計・確率
    path: /math/statistics/index.md
  - title: 確率
    path: /math/statistics/probability/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 場合の数
    path: /math/statistics/counting/introduction.md
  - title: 分数
    path: /math/numbers/fractions/introduction.md
---




## 確率の定義（古典的確率）

起こりやすさを 0 から 1 の数値で表したものが確率です。

同様に確からしい（等確率の）根元事象が $n$ 個あり、事象 $A$ が $m$ 個の根元事象からなるとき

$$P(A) = \frac{m}{n}$$

$0 \leq P(A) \leq 1$、$P(\text{全事象}) = 1$、$P(\emptyset) = 0$。

例：サイコロで偶数が出る確率：$P = \dfrac{3}{6} = \dfrac{1}{2}$

---

## 余事象

$A$ が起きない事象を**余事象** $A^c$ といいます。

$$P(A^c) = 1 - P(A)$$

「少なくとも1回以上」のような問題は余事象で考えると楽なことが多いです。

例：コインを3回投げて少なくとも1回表が出る確率：\
$$1 - P(\text{3回全部裏}) = 1 - \left(\frac{1}{2}\right)^3 = \frac{7}{8}$$

---

## 加法定理

$$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$

$A$ と $B$ が**排反**（同時に起きない、$A \cap B = \emptyset$）のとき：

$$P(A \cup B) = P(A) + P(B)$$

---

## 独立な事象

$A$ と $B$ が**独立**（一方の結果が他方に影響しない）とは

$$P(A \cap B) = P(A) \times P(B)$$

が成り立つことです。

例：コインを2回投げるとき「1回目が表」と「2回目が表」は独立。\
両方表の確率 $= \dfrac{1}{2} \times \dfrac{1}{2} = \dfrac{1}{4}$

---

## 条件付き確率

「$B$ が起きたとわかった上での $A$ の確率」を**条件付き確率**といいます。

$$P(A \mid B) = \frac{P(A \cap B)}{P(B)} \quad (P(B) > 0)$$

---

## ベイズの定理

$$P(A \mid B) = \frac{P(B \mid A) \cdot P(A)}{P(B)}$$

「結果 $B$ が観測されたとき、原因 $A$ の確率は？」という問いに答えます。\
医療検査の偽陽性・偽陰性の評価などで重要です。

---

## 関連ページ

- [場合の数](../counting/introduction.md)
