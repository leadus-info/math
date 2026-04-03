---
title: 確率
description: "起こりやすさを数で表す"
difficulty: 2
tags: [math,statistics,probability]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 統計・確率
    href: /math/statistics/index.html
  - text: 確率
    href: /math/statistics/probability/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 確率
コインを投げると表か裏が出ます。どちらが出るかは事前にわかりません。
**確率**は「どれくらい起こりやすいか」を $0$ から $1$ の数で表したものです。

## このページで扱うこと
- 確率の定義と基本計算
- 余事象（起きない確率）
- 条件付き確率

## 前提知識
- [場合の数](../counting/standard.md)
- [分数](../../numbers/fractions/standard.md)

---

## 確率とは？

$$P(A) = \frac{\text{事象 } A \text{ の場合の数}}{\text{全体の場合の数}}$$

- $P(A) = 0$：絶対起きない
- $P(A) = 1$：必ず起きる
- $0 \leq P(A) \leq 1$：常に $0$ 以上 $1$ 以下

**例**：サイコロで $3$ が出る確率 $= \dfrac{1}{6}$

---

## 余事象

「$A$ が起きない確率」を**余事象**といいます。

$$P(\text{$A$ が起きない}) = 1 - P(A)$$

「少なくとも $1$ 回 $A$ が起きる」確率は、余事象「$1$ 回も起きない」を使うと楽です。

**例**：コイン $3$ 回投げて少なくとも $1$ 回表が出る確率

$$1 - P(\text{$3$ 回全部裏}) = 1 - \left(\frac{1}{2}\right)^3 = 1 - \frac{1}{8} = \frac{7}{8}$$

---

## 和の法則

$$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$

$A$ と $B$ が同時に起きない（排反）なら：

$$P(A \cup B) = P(A) + P(B)$$

---

## 独立な事象

一方が他方に影響しない場合：

$$P(A \cap B) = P(A) \times P(B)$$

**例**：$2$ 枚のコインを投げるとき、両方表 $= \dfrac{1}{2} \times \dfrac{1}{2} = \dfrac{1}{4}$

---

## 条件付き確率

「$B$ が起きたとわかった上での $A$ の確率」：

$$P(A \mid B) = \frac{P(A \cap B)}{P(B)}$$

**例**：赤玉 $3$ 個・白玉 $2$ 個の袋から $1$ 個取り出して赤だったとき、
次も赤が出る確率は（袋に戻さない場合）$\dfrac{2}{4} = \dfrac{1}{2}$

---

## 関連ページ

- [場合の数](../counting/standard.md)
- [確率（発展）](../probability/advanced.md) — より詳しく学ぶ
