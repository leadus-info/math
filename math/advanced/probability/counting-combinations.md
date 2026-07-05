---
title: 組み合わせ
description: "順番を区別せずに選ぶ場合の数"
goal: "組み合わせの公式と重複組み合わせを理解し、計算できるようになる"
tags: [math, probability, counting]
stage: advanced
subject: 確率
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 応用編
    path: ../index.md
  - title: 組み合わせ
    path: counting-combinations.md
requires:
  - title: 順列
    path: counting-permutations.md
---

## 順番を区別せずに選ぶ

5人から3人のチームを作るように、誰が選ばれるかだけが問題になる選び方を**組み合わせ**といいます。$n$ 個から $r$ 個を順番を区別せず選ぶ場合の数：

$$\binom{n}{r} = \frac{n!}{r!(n-r)!} = \frac{_nP_r}{r!}$$

**例**：$\binom{5}{3} = \frac{60}{6} = 10$

順列を $r!$ で割るのは、$r$ 個の選択物の並べ方（$r!$ 通り）が同一視されるためです。**性質**：$\binom{n}{r} = \binom{n}{n-r}$（選ぶのと選ばないのを入れ替えても同じ）。

---

## 重複組み合わせ

$n$ 種類から重複を許して $r$ 個選ぶ場合の数：

$$\binom{n+r-1}{r}$$

**例**：りんご・みかん・ぶどうから3個選ぶ（同じ種類を複数可）：$\binom{3+3-1}{3} = \binom{5}{3} = 10$

---

## まとめ

組み合わせは、順番を区別せず$n$個から$r$個を選ぶ場合の数で、$\binom{n}{r} = \dfrac{n!}{r!(n-r)!}$ で求められます。重複を許す場合は重複組み合わせの公式を使います。

---

## 関連ページ

- [二項定理（応用編）](counting-binomial-theorem.md)
