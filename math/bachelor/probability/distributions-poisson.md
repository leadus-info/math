---
title: ポアソン分布
description: "単位時間あたりまれにしか起きない事象の発生回数が従うポアソン分布の定義・期待値・分散と、二項分布の極限として現れる近似の関係を解説する"
goal: "ポアソン分布の定義と、二項分布との関係を理解できるようになる"
tags: [math, probability, distributions]
stage: bachelor
subject: 確率
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: ポアソン分布
    path: distributions-poisson.md
requires:
  - title: 二項分布
    path: distributions-binomial.md
---

## $\mathrm{Po}(\lambda)$

単位時間あたり平均 $\lambda$ 回起きる事象の、ある単位時間での発生回数：

$$P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!} \quad (k = 0, 1, 2, \ldots)$$

$$E[X] = \lambda, \quad \mathrm{Var}(X) = \lambda$$

$n$ が大きく $p$ が小さい二項分布 $B(n,p)$（$\lambda = np$ 固定）の近似として現れます。

---

## まとめ

ポアソン分布は、単位時間あたりまれにしか起きない事象の発生回数を表す分布で、二項分布の極限として現れます。

---

## 関連ページ

- [正規分布（発展編）](distributions-normal.md)
