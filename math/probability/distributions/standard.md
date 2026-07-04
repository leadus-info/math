---
title: 確率分布
description: "離散・連続分布の定義と代表的な分布"
goal: "確率質量関数・確率密度関数を定義し、二項分布・正規分布・ポアソン分布の性質と使いどころを説明できるようになる"
tags: [math,probability,distributions]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 確率
    path: /math/probability/index.md
  - title: 確率分布
    path: /math/probability/distributions/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 確率分布（入門）
    path: /math/probability/distributions/introduction.md
  - title: 積分（標準）
    path: /math/analysis/integrals/standard.md
---

## 離散確率分布

**確率質量関数（PMF）**：$p(x) = P(X = x)$

条件：$p(x) \geq 0$、$\sum_x p(x) = 1$

**期待値**：$E[X] = \sum_x x \cdot p(x)$

**分散**：$\mathrm{Var}(X) = E[(X - E[X])^2] = E[X^2] - (E[X])^2$

---

## 二項分布 $B(n, p)$

$n$ 回の独立な試行で各回成功確率 $p$ のとき、成功回数 $X$ の分布：

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

**確率密度関数（PDF）**：$f(x) \geq 0$、$\int_{-\infty}^{\infty} f(x)\,dx = 1$

$$P(a \leq X \leq b) = \int_a^b f(x)\,dx$$

**期待値**：$E[X] = \int_{-\infty}^{\infty} x f(x)\,dx$

---

## 正規分布 $N(\mu, \sigma^2)$

$$f(x) = \frac{1}{\sqrt{2\pi}\sigma} \exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right)$$

$$E[X] = \mu, \quad \mathrm{Var}(X) = \sigma^2$$

**標準化**：$Z = \frac{X - \mu}{\sigma} \sim N(0, 1)$

**68-95-99.7則**：$\mu \pm \sigma$ に約68%、$\mu \pm 2\sigma$ に約95%、$\mu \pm 3\sigma$ に約99.7%のデータが入ります。

---

## 指数分布 $\mathrm{Exp}(\lambda)$

ポアソン過程での待ち時間の分布：

$$f(x) = \lambda e^{-\lambda x} \quad (x \geq 0)$$

$$E[X] = \frac{1}{\lambda}, \quad \mathrm{Var}(X) = \frac{1}{\lambda^2}$$

**無記憶性**：$P(X > s + t \mid X > s) = P(X > t)$

---

## 関連ページ

- [確率（標準）](../probability/standard.md)
- [積分（標準）](../../analysis/integrals/standard.md)
- [確率分布（専門）](professional.md)
