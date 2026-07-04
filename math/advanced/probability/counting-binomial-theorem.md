---
title: 二項定理
description: "(a+b)^nの展開を組み合わせの数で表す"
goal: "二項定理を理解し、(a+b)^nの展開に使えるようになる"
tags: [math, probability, counting]
stage: 応用編
subject: 確率
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 応用編
    path: /math/advanced/index.md
  - title: 二項定理
    path: /math/advanced/probability/counting-binomial-theorem.md
requires:
  - title: 組み合わせ
    path: counting-combinations.md
---

## (a+b)^nの展開

$$(a + b)^n = \sum_{k=0}^n \binom{n}{k} a^{n-k} b^k$$

**例**：$(a+b)^3 = a^3 + 3a^2b + 3ab^2 + b^3$（係数 $\binom{3}{0}=1$, $\binom{3}{1}=3$, $\binom{3}{2}=3$, $\binom{3}{3}=1$）。

---

## まとめ

二項定理は、$(a+b)^n$ の展開の各項の係数が組み合わせ $\binom{n}{k}$ で表せることを示す定理です。

---

## 関連ページ

- [組み合わせ（応用編）](counting-combinations.md)
- [多項式（応用編）](/math/advanced/algebra/polynomials.md)
