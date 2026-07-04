---
title: 順列
description: "順番を区別して選ぶ場合の数"
goal: "順列の公式を理解し、計算できるようになる"
tags: [math, probability, counting]
stage: 応用編
subject: 確率
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 応用編
    path: /math/advanced/index.md
  - title: 順列
    path: /math/advanced/probability/counting-permutations.md
requires:
  - title: 場合の数
    path: counting.md
---

## 順番を区別して選ぶ

5人から3人を「1位・2位・3位」に決めるように、順番が意味を持つ選び方を**順列**といいます。$n$ 個から $r$ 個を順番を区別して選ぶ場合の数：

$$_nP_r = \frac{n!}{(n-r)!} = n(n-1)\cdots(n-r+1)$$

**例**：$_5P_3 = 5 \times 4 \times 3 = 60$（1位の選び方5通り、2位は残り4通り、3位は残り3通り）。

---

## まとめ

順列は、順番を区別して$n$個から$r$個を選ぶ場合の数で、$_nP_r = \dfrac{n!}{(n-r)!}$ で求められます。

---

## 関連ページ

- [組み合わせ（応用編）](counting-combinations.md)
