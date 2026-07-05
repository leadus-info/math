---
title: 場合の数
description: "何通りあるかを数える"
goal: "積の法則・和の法則・階乗の意味を理解し、基本的な場合の数を数えられるようになる"
tags: [math, probability, counting]
stage: advanced
subject: 確率
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 応用編
    path: ../index.md
  - title: 場合の数
    path: counting.md
requires:
  - title: 自然数
    path: ../../beginner/numbers/natural-numbers.md
---

## 「何通りあるか」を数える

ランチで「ごはんかパン」「魚か肉か野菜」を選ぶとき、組み合わせは全部で何通りでしょう。ごはんかパンの選び方が2通り、おかずが3通り、独立して選べるので $2 \times 3 = 6$ 通りです。「何通りあるか」を数えるのが**場合の数**です。

---

## 積の法則・和の法則

**独立して選べる場合は掛け算**を使います。

> Tシャツ4色 × ズボン3色 = $4 \times 3 = 12$ 通りのコーディネート

**どちらか一方を選ぶ（同時には使えない）場合は足し算**を使います。

> 家から駅まで「バスで3ルート」または「自転車で2ルート」→ 合計 $3 + 2 = 5$ 通り

---

## 階乗

$n!$（$n$ の**階乗**）は $1$ から $n$ までのすべての整数の積です。

$$n! = n \times (n-1) \times \cdots \times 2 \times 1$$

$$0! = 1, \quad 1! = 1, \quad 5! = 120$$

---

## まとめ

場合の数では「独立な選択は掛け算」「どちらかを選ぶ場合は足し算」が基本原理です。階乗はこの先の順列・組み合わせの計算の土台になります。

---

## 関連ページ

- [順列（応用編）](counting-permutations.md)
- [組み合わせ（応用編）](counting-combinations.md)
- [二項定理（応用編）](counting-binomial-theorem.md)
- [確率（応用編）](probability.md)
