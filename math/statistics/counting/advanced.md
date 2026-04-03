---
title: 場合の数（発展）
description: "何通りあるかを数える（発展）"
difficulty: 2
tags: [math,statistics,counting,advanced]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 統計・確率
    href: /math/statistics/index.html
  - text: 場合の数（発展）
    href: /math/statistics/counting/advanced.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
  - text: 専門
    href: professional.html
---







# 場合の数
「何通りあるか」を数えるのが**場合の数**です。
確率の計算の基礎になります。

## このページで扱うこと
- 加法則・乗法則
- 順列（並び方）と組み合わせ（選び方）
- よく使う公式

## 前提知識
- [自然数](professional.md)
- [四則演算](professional.md)

---

## 加法則・乗法則

**加法則**：A か B か（排反）

$$\text{A の数} + \text{B の数}$$

**乗法則**：A の後に B

$$\text{A の数} \times \text{B の数}$$

---

## 階乗

$$n! = n \times (n-1) \times \cdots \times 1, \quad 0! = 1$$

$$5! = 120$$

---

## 順列（順番あり）

$n$ 個から $r$ 個を**順番を区別して**選ぶ：

$$_nP_r = \frac{n!}{(n-r)!}$$

**例**：5 人から 3 人を 1・2・3 位に選ぶ

$$_5P_3 = 5 \times 4 \times 3 = 60$$

---

## 組み合わせ（順番なし）

$n$ 個から $r$ 個を**順番を区別せず**選ぶ：

$$\binom{n}{r} = \frac{n!}{r!(n-r)!}$$

**例**：5 人から 3 人を選ぶ（1 チームを作る）

$$\binom{5}{3} = 10$$

---

## 順列と組み合わせの違い

$$_nP_r = \binom{n}{r} \times r!$$

同じ 3 人を選ぶとき、並び順を考えると $6$ 倍になります。

---

## 関連ページ

- [確率](professional.md)
- [場合の数（専門）](professional.md)
