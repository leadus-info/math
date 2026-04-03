---
title: 場合の数
description: "「何通りあるか」を数える"
difficulty: 1
tags: [math,statistics,counting]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 統計・確率
    href: /math/statistics/index.html
  - text: 場合の数
    href: /math/statistics/counting/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 場合の数
「服が $3$ 着、ズボンが $4$ 本あると、何通りの組み合わせができる？」
こういった「何通りあるか」を数えるのが**場合の数**です。

## このページで扱うこと
- 樹形図・加法則・乗法則
- 順列（並び方の数）
- 組み合わせ（選び方の数）

## 前提知識
- [自然数](../../numbers/natural-numbers/standard.md)
- [乗法・べき乗](../../numbers/arithmetic/standard.md)

---

## 乗法則（積の法則）

「服 $3$ 着 × ズボン $4$ 本」のように、$A$ と $B$ を組み合わせるとき：

$$\text{A の数} \times \text{B の数}$$

**例**：サイコロを $2$ 回振ると $6 \times 6 = 36$ 通り。

---

## 加法則（和の法則）

「A か B かどちらか（同時に起こらない）」のとき：

$$\text{A の数} + \text{B の数}$$

**例**：バスか電車で行く方法が $3$ 種類・$5$ 種類なら合計 $3 + 5 = 8$ 通り。

---

## 階乗

$$n! = n \times (n-1) \times \cdots \times 2 \times 1$$

$$5! = 5 \times 4 \times 3 \times 2 \times 1 = 120, \quad 0! = 1$$

---

## 順列（並び方）

$n$ 個から $r$ 個を**順番を区別して**並べる場合の数：

$$_nP_r = \frac{n!}{(n-r)!}$$

**例**：$5$ 人から $3$ 人を $1$・$2$・$3$ 位に選ぶ → $_5P_3 = 5 \times 4 \times 3 = 60$

---

## 組み合わせ（選び方）

$n$ 個から $r$ 個を**順番を区別せず**選ぶ場合の数：

$$\binom{n}{r} = \frac{n!}{r!(n-r)!}$$

**例**：$5$ 人から $3$ 人を選ぶ（チーム編成）→ $\dbinom{5}{3} = 10$

---

## 順列 vs 組み合わせ

$\{A, B, C\}$ から $2$ 人選ぶとき：

- **順列**（順番あり）：AB・BA・AC・CA・BC・CB → $6$ 通り
- **組み合わせ**（順番なし）：AB・AC・BC → $3$ 通り

$$_nP_r = \binom{n}{r} \times r!$$

---

## 関連ページ

- [確率](../probability/standard.md)
- [場合の数（発展）](../counting/advanced.md) — より詳しく学ぶ
