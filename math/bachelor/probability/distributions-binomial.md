---
title: 二項分布
description: "n回の独立試行での成功回数の分布"
goal: "二項分布の定義と期待値・分散を、ベルヌーイ確率変数の和として厳密に導出し、使いどころを説明できるようになる"
tags: [math, probability, distributions]
stage: bachelor
subject: 確率
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 二項分布
    path: distributions-binomial.md
requires:
  - title: 確率分布
    path: distributions.md
  - title: 二項分布
    path: ../../advanced/probability/binomial-distribution.md
---

## $B(n, p)$

コインを10回投げて表が出る回数のように、$n$ 回の独立な試行で各回成功確率 $p$ のとき、成功回数 $X$ の分布：

$$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k} \quad (k = 0, 1, \ldots, n)$$

$$E[X] = np, \quad \mathrm{Var}(X) = np(1-p)$$

**例**：コイン10回投げて表が出る回数は $B(10, 0.5)$。$E[X] = 5$、$\mathrm{Var}(X) = 2.5$。

---

## ベルヌーイ確率変数の和としての導出

$E[X] = np$、$\mathrm{Var}(X) = np(1-p)$ は、定義の和を直接計算する代わりに、$X$ を**ベルヌーイ確率変数**の和として捉えると簡潔に導けます。$i$ 回目の試行の成功・失敗を表す確率変数を

$$X_i = \begin{cases}1 & (i \text{ 回目が成功}) \\ 0 & (i \text{ 回目が失敗})\end{cases}, \qquad X = X_1 + X_2 + \cdots + X_n$$

とすると、各 $X_i$ は $E[X_i] = p$、$\mathrm{Var}(X_i) = p(1-p)$ を満たします。期待値は独立性を仮定しなくても和に分解できる（**期待値の線形性**）ので、

$$E[X] = \sum_{i=1}^n E[X_i] = np$$

が直ちに従います。一方、分散は一般には和に分解できませんが、$X_1, \ldots, X_n$ が**独立**なので、

$$\mathrm{Var}(X) = \sum_{i=1}^n \mathrm{Var}(X_i) = np(1-p)$$

が成り立ちます（独立な確率変数の分散は和に分解できる、という性質を使っています）。組合せ論的な和 $\sum_k k\binom{n}{k}p^k(1-p)^{n-k}$ を直接計算するより、この分解の方がはるかに見通しがよいことに注意してください。

---

## まとめ

二項分布は、$n$回の独立な試行における成功回数の分布で、期待値は $np$、分散は $np(1-p)$ です。これらは、二項分布に従う確率変数をベルヌーイ確率変数の和として分解し、期待値の線形性と分散の独立性からの加法性を使うと簡潔に導出できます。

---

## 関連ページ

- [ポアソン分布（発展編）](distributions-poisson.md)
