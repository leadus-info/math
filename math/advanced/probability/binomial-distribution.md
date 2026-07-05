---
title: 二項分布
description: "反復試行における成功回数の確率分布"
goal: "二項分布の確率・期待値・分散を求められるようになる"
tags: [math, probability, binomial-distribution]
stage: advanced
subject: 確率
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 応用編
    path: ../index.md
  - title: 二項分布
    path: binomial-distribution.md
requires:
  - title: 確率変数と確率分布
    path: random-variables.md
---

## 反復試行から生まれる確率分布

確率（応用編）で見た反復試行の確率を思い出しましょう。1回の試行で事象 $A$ が起こる確率が $p$ のとき、$n$ 回の独立な試行で $A$ がちょうど $k$ 回起こる確率は、

$$P(X=k) = \binom{n}{k}p^k(1-p)^{n-k} \quad (k=0,1,\ldots,n)$$

この確率変数 $X$（$n$回中、事象 $A$ が起こる回数）が従う確率分布を**二項分布**といい、$X \sim B(n,p)$ と表します。

**例**：コインを4回投げるとき、表が出る回数 $X$ は $B(4, 0.5)$ に従います。$P(X=2) = \binom{4}{2}(0.5)^2(0.5)^2 = 6\times0.0625=0.375$。

---

## 二項分布の期待値・分散

二項分布 $B(n,p)$ に従う確率変数 $X$ について、次が成り立ちます。

$$E(X) = np, \qquad V(X) = np(1-p), \qquad \sigma(X) = \sqrt{np(1-p)}$$

直感的には、1回の試行での期待値が $p$（1回あたり平均 $p$ 回起こる、と考える）なので、$n$回分では $np$ になる、という理解ができます（厳密には、各回の試行を表す確率変数の和として $X$ を捉え、期待値・分散が独立な確率変数の和で計算できることを使います）。

**例題**：さいころを720回投げるとき、1の目が出る回数の期待値と標準偏差を求める。$n=720$、$p=\dfrac16$。

$$E(X) = 720\times\frac16=120, \qquad \sigma(X)=\sqrt{720\times\frac16\times\frac56}=\sqrt{100}=10$$

---

## まとめ

二項分布 $B(n,p)$ は、独立な反復試行で事象が起こる回数を表す確率分布です。期待値は $np$、分散は $np(1-p)$ という簡潔な式で表され、試行回数が大きくなっても直接計算できます。

---

## 関連ページ

- [正規分布（応用編）](normal-distribution.md)
