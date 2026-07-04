---
title: 二項分布
description: "n回の独立試行での成功回数の分布"
goal: "二項分布の定義と期待値・分散を理解し、使いどころを説明できるようになる"
tags: [math, probability, distributions]
stage: 発展編
subject: 確率
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 発展編
    path: /math/bachelor/index.md
  - title: 二項分布
    path: /math/bachelor/probability/distributions-binomial.md
requires:
  - title: 確率分布
    path: distributions.md
  - title: 二項分布
    path: /math/advanced/probability/binomial-distribution.md
---

## $B(n, p)$

コインを10回投げて表が出る回数のように、$n$ 回の独立な試行で各回成功確率 $p$ のとき、成功回数 $X$ の分布：

$$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k} \quad (k = 0, 1, \ldots, n)$$

$$E[X] = np, \quad \mathrm{Var}(X) = np(1-p)$$

**例**：コイン10回投げて表が出る回数は $B(10, 0.5)$。$E[X] = 5$、$\mathrm{Var}(X) = 2.5$。

---

## まとめ

二項分布は、$n$回の独立な試行における成功回数の分布で、期待値は $np$、分散は $np(1-p)$ です。

---

## 関連ページ

- [確率分布（発展編）](distributions.md)
- [ポアソン分布（発展編）](distributions-poisson.md)
