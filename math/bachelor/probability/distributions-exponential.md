---
title: 指数分布
description: "ポアソン過程における次の事象までの待ち時間が従う指数分布の定義・期待値・分散と、過去の経過時間に依存しない無記憶性という性質を解説する"
goal: "指数分布の定義と無記憶性を理解できるようになる"
tags: [math, probability, distributions]
stage: bachelor
subject: 確率
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 指数分布
    path: distributions-exponential.md
requires:
  - title: 正規分布
    path: distributions-normal.md
---

## $\mathrm{Exp}(\lambda)$

ポアソン過程での待ち時間の分布：

$$f(x) = \lambda e^{-\lambda x} \quad (x \geq 0), \qquad E[X] = \frac{1}{\lambda}, \quad \mathrm{Var}(X) = \frac{1}{\lambda^2}$$

**期待値の導出**：累積分布関数は $P(X>x)=\int_x^\infty \lambda e^{-\lambda t}\,dt=e^{-\lambda x}$ です。部分積分を使うと、

$$E[X]=\int_0^\infty x\lambda e^{-\lambda x}\,dx = \Bigl[-xe^{-\lambda x}\Bigr]_0^\infty+\int_0^\infty e^{-\lambda x}\,dx = 0+\left[-\frac{1}{\lambda}e^{-\lambda x}\right]_0^\infty=\frac1\lambda$$

分散も同様の計算（$E[X^2]$ を部分積分で求めて $E[X^2]-(E[X])^2$ をとる）により $\mathrm{Var}(X)=\dfrac{1}{\lambda^2}$ が得られます。

**無記憶性**：$P(X > s + t \mid X > s) = P(X > t)$（すでに $s$ 待った事実が、追加の待ち時間の分布に影響しない）。

**証明**：条件付き確率の定義と $\{X>s+t\}\subset\{X>s\}$（$t\geq0$ なので）より $P(X>s+t\cap X>s)=P(X>s+t)$ に注意すると、

$$P(X>s+t \mid X>s) = \frac{P(X>s+t)}{P(X>s)} = \frac{e^{-\lambda(s+t)}}{e^{-\lambda s}} = e^{-\lambda t} = P(X>t)$$

$\blacksquare$

---

## まとめ

指数分布は、ポアソン過程における待ち時間を表す分布で、期待値$\frac1\lambda$・分散$\frac{1}{\lambda^2}$は累積分布関数を部分積分することで導出できます。無記憶性（過去の経過時間が今後の待ち時間の分布に影響しない）という特徴的な性質は、条件付き確率の定義から直接証明できます。

---

## 関連ページ

- [確率分布](distributions.md)
