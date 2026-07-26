---
title: 確率分布
description: "確率変数の値の広がり方を表す確率分布について、確率質量関数・確率密度関数の定義と期待値・分散の計算方法、離散分布と連続分布の違いを解説する"
goal: "確率質量関数・確率密度関数の枠組みを理解し、離散分布・連続分布の違いを説明できるようになる"
tags: [math, probability, distributions]
stage: bachelor
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

**確率質量関数（PMF）**：$p(x) = P(X = x)$。条件は $p(x) \geq 0$、$\sum_x p(x) = 1$。**例**：サイコロの出目$X$なら $p(1)=p(2)=\cdots=p(6)=\dfrac16$。

**期待値**：$E[X] = \sum_x x \cdot p(x)$

**分散**：$\mathrm{Var}(X) = E[(X - E[X])^2] = E[X^2] - (E[X])^2$

---

## 連続確率分布

**確率密度関数（PDF）**：$f(x) \geq 0$、$\int_{-\infty}^{\infty} f(x)\,dx = 1$ を満たす関数で、

$$P(a \leq X \leq b) = \int_a^b f(x)\,dx, \qquad E[X] = \int_{-\infty}^{\infty} x f(x)\,dx$$

**例**：区間$[0,1]$上の一様分布は $f(x)=1$（$0\leq x\leq1$）、それ以外は$f(x)=0$。$P(0.2\leq X\leq0.5)=\int_{0.2}^{0.5}1\,dx=0.3$。

連続分布では、特定の1点$a$をとる確率は $P(X=a)=\int_a^a f(x)\,dx=0$ になります（積分区間の幅が0だから）。離散分布ではサイコロの目のように1点の確率が正の値を持つのに対し、連続分布では「ある区間に入る確率」だけが意味を持ち、1点そのものの確率は常に0になる、という点が離散分布との本質的な違いです。確率密度関数の値$f(a)$自体は0でなくてもよく、あくまで「その点の近くでの確率の込み具合（密度）」を表しています。

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
