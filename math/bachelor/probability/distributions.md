---
title: 確率分布
description: "確率変数の値の広がり方"
goal: "確率質量関数・確率密度関数の枠組みを理解し、離散分布・連続分布の違いを説明できるようになる"
tags: [math, probability, distributions]
stage: 発展編
subject: 確率
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 確率分布
    path: distributions.md
requires:
  - title: 確率変数と確率分布
    path: ../../advanced/probability/random-variables.md
  - title: 積分
    path: ../../advanced/analysis/integrals.md
---

## 「何が出るか」を関数で表す

サイコロを1回振ったとき、出る目 $X$ は $1$ から $6$ のどれかで、各値の出やすさをまとめると「確率変数の値とその確率の対応」が得られます。これを**確率分布**といいます。「値 × その確率」を全部足したものが**期待値**（平均）です。

---

## 離散確率分布

**確率質量関数（PMF）**：$p(x) = P(X = x)$。条件は $p(x) \geq 0$、$\sum_x p(x) = 1$。

**期待値**：$E[X] = \sum_x x \cdot p(x)$

**分散**：$\mathrm{Var}(X) = E[(X - E[X])^2] = E[X^2] - (E[X])^2$

---

## 連続確率分布

**確率密度関数（PDF）**：$f(x) \geq 0$、$\int_{-\infty}^{\infty} f(x)\,dx = 1$ を満たす関数で、

$$P(a \leq X \leq b) = \int_a^b f(x)\,dx, \qquad E[X] = \int_{-\infty}^{\infty} x f(x)\,dx$$

---

## まとめ

確率分布は確率変数の値の広がり方を表します。離散分布は確率質量関数、連続分布は確率密度関数で記述されます。代表的な分布は、それぞれ異なる状況（成功回数、まれな事象の発生回数、多くの量の自然な分布、待ち時間）をモデル化します。

---

## 関連ページ

- [二項分布（発展編）](distributions-binomial.md)
- [ポアソン分布（発展編）](distributions-poisson.md)
- [正規分布（発展編）](distributions-normal.md)
- [指数分布（発展編）](distributions-exponential.md)
- [統計（発展編）](statistics.md)
