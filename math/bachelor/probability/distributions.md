---
title: 確率分布
description: "確率変数の値の広がり方"
goal: "確率質量関数・確率密度関数を定義し、二項分布・ポアソン分布・正規分布・指数分布の性質と使いどころを説明できるようになる"
tags: [math, probability, distributions]
stage: 発展編
subject: 確率
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 発展編
    path: /math/bachelor/index.md
  - title: 確率分布
    path: /math/bachelor/probability/distributions.md
requires:
  - title: 確率
    path: /math/advanced/probability/probability.md
  - title: 積分
    path: /math/advanced/analysis/integrals.md
---

## 「何が出るか」を関数で表す

サイコロを1回振ったとき、出る目 $X$ は $1$ から $6$ のどれかで、各値の出やすさをまとめると「確率変数の値とその確率の対応」が得られます。これを**確率分布**といいます。「値 × その確率」を全部足したものが**期待値**（平均）です。

---

## 離散確率分布

**確率質量関数（PMF）**：$p(x) = P(X = x)$。条件は $p(x) \geq 0$、$\sum_x p(x) = 1$。

**期待値**：$E[X] = \sum_x x \cdot p(x)$

**分散**：$\mathrm{Var}(X) = E[(X - E[X])^2] = E[X^2] - (E[X])^2$

---

## 二項分布 $B(n, p)$

コインを10回投げて表が出る回数のように、$n$ 回の独立な試行で各回成功確率 $p$ のとき、成功回数 $X$ の分布：

$$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k} \quad (k = 0, 1, \ldots, n)$$

$$E[X] = np, \quad \mathrm{Var}(X) = np(1-p)$$

**例**：コイン10回投げて表が出る回数は $B(10, 0.5)$。$E[X] = 5$、$\mathrm{Var}(X) = 2.5$。

---

## ポアソン分布 $\mathrm{Po}(\lambda)$

単位時間あたり平均 $\lambda$ 回起きる事象の、ある単位時間での発生回数：

$$P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!} \quad (k = 0, 1, 2, \ldots)$$

$$E[X] = \lambda, \quad \mathrm{Var}(X) = \lambda$$

$n$ が大きく $p$ が小さい二項分布 $B(n,p)$（$\lambda = np$ 固定）の近似として現れます。

---

## 連続確率分布

**確率密度関数（PDF）**：$f(x) \geq 0$、$\int_{-\infty}^{\infty} f(x)\,dx = 1$ を満たす関数で、

$$P(a \leq X \leq b) = \int_a^b f(x)\,dx, \qquad E[X] = \int_{-\infty}^{\infty} x f(x)\,dx$$

---

## 正規分布 $N(\mu, \sigma^2)$

身長・テストの点数・測定誤差——自然界や社会の多くの量が従う、左右対称の釣り鐘型の分布です。

$$f(x) = \frac{1}{\sqrt{2\pi}\sigma} \exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right), \qquad E[X] = \mu, \quad \mathrm{Var}(X) = \sigma^2$$

**標準化**：$Z = \dfrac{X - \mu}{\sigma} \sim N(0, 1)$

**68-95-99.7則**：$\mu \pm \sigma$ に約68%、$\mu \pm 2\sigma$ に約95%、$\mu \pm 3\sigma$ に約99.7%のデータが入ります。「偏差値」はこの分布を使って計算されています。

---

## 指数分布 $\mathrm{Exp}(\lambda)$

ポアソン過程での待ち時間の分布：

$$f(x) = \lambda e^{-\lambda x} \quad (x \geq 0), \qquad E[X] = \frac{1}{\lambda}, \quad \mathrm{Var}(X) = \frac{1}{\lambda^2}$$

**無記憶性**：$P(X > s + t \mid X > s) = P(X > t)$（すでに $s$ 待った事実が、追加の待ち時間の分布に影響しない）。

---

## まとめ

確率分布は確率変数の値の広がり方を表します。離散分布は確率質量関数、連続分布は確率密度関数で記述され、二項分布・ポアソン分布・正規分布・指数分布はそれぞれ異なる状況（成功回数、まれな事象の発生回数、多くの量の自然な分布、待ち時間）をモデル化します。

---

## 関連ページ

- [統計（発展編）](statistics.md)
