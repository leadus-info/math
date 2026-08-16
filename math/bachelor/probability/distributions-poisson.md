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

**例**：単位時間あたり平均3件の電話がかかってくる窓口で、ある単位時間にちょうど5件かかってくる確率は $P(X=5)=\dfrac{3^5e^{-3}}{5!}=\dfrac{243e^{-3}}{120}\approx0.101$。

---

## 二項分布の極限としての導出

$n$ が大きく $p$ が小さい二項分布 $B(n,p)$ は、$\lambda=np$（すなわち $p=\lambda/n$）を固定して $n\to\infty$ とすると、ポアソン分布 $\mathrm{Po}(\lambda)$ に収束します。

**証明**：$p=\lambda/n$ を $B(n,p)$ の確率質量関数に代入すると、

$$P(X=k)=\binom{n}{k}\left(\frac\lambda n\right)^k\left(1-\frac\lambda n\right)^{n-k} = \frac{n(n-1)\cdots(n-k+1)}{k!}\cdot\frac{\lambda^k}{n^k}\cdot\left(1-\frac\lambda n\right)^{n-k}$$

$n\to\infty$ のとき、$\dfrac{n(n-1)\cdots(n-k+1)}{n^k}=1\times\left(1-\dfrac1n\right)\times\cdots\times\left(1-\dfrac{k-1}n\right)\to1$（$k$ は固定なので分子の各因数が1に近づく）。また $\left(1-\dfrac\lambda n\right)^{n-k}=\left(1-\dfrac\lambda n\right)^n\times\left(1-\dfrac\lambda n\right)^{-k}$ において、後者は $n\to\infty$ で $1$ に近づき、前者はネイピア数の定義の変形から $\left(1-\dfrac\lambda n\right)^n\to e^{-\lambda}$ となることが知られています。

これらを組み合わせると、

$$P(X=k) \to 1\times\frac{\lambda^k}{k!}\times e^{-\lambda} = \frac{\lambda^k e^{-\lambda}}{k!}$$

となり、これはちょうどポアソン分布の確率質量関数です。$\blacksquare$

---

## まとめ

ポアソン分布は、単位時間あたりまれにしか起きない事象の発生回数を表す分布です。$\lambda=np$を固定して$n\to\infty$とすると、二項分布$B(n,p)$の確率質量関数がポアソン分布の確率質量関数に収束することが、極限の計算から証明できます。

---

## 関連ページ

- [正規分布](distributions-normal.md)
