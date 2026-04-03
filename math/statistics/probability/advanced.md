---
title: 確率（発展）
description: "起こりやすさを数値で表す（発展）"
difficulty: 3
tags: [math,statistics,probability,advanced]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 統計・確率
    href: /math/statistics/index.html
  - text: 確率（発展）
    href: /math/statistics/probability/advanced.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
  - text: 専門
    href: professional.html
---







# 確率
コインを投げると表か裏が出る——どちらが出るかはわかりません。
**確率**は「起こりやすさ」を 0 から 1 の数値で表す道具です。

## このページで扱うこと
- 確率の定義と基本的な計算
- 余事象・和の法則
- 条件付き確率とベイズの定理

## 前提知識
- [場合の数](professional.md)
- [分数](professional.md)

---

## 確率の定義

$$P(A) = \frac{\text{事象 } A \text{ が起きる場合の数}}{\text{全体の場合の数}}$$

$$0 \leq P(A) \leq 1$$

---

## 余事象

「$A$ が起きない」確率：

$$P(A^c) = 1 - P(A)$$

「少なくとも 1 回」などは余事象で考えると楽になります。

---

## 和の法則

$$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$

$A$ と $B$ が同時に起きない場合：

$$P(A \cup B) = P(A) + P(B)$$

---

## 独立な事象

$A$ と $B$ が独立（一方が他方に影響しない）なら：

$$P(A \cap B) = P(A) \times P(B)$$

---

## 条件付き確率

「$B$ が起きたとわかった上での $A$ の確率」：

$$P(A \mid B) = \frac{P(A \cap B)}{P(B)}$$

---

## ベイズの定理

$$P(A \mid B) = \frac{P(B \mid A) \times P(A)}{P(B)}$$

「結果 $B$ が起きたとき、原因 $A$ の確率は？」を計算します。

---

## 関連ページ

- [場合の数](professional.md)
- [確率（専門）](professional.md)
