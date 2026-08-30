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
  - title: ポアソン分布
    path: distributions-poisson.md
---

## $\mathrm{Exp}(\lambda)$

単位時間あたり平均$\lambda$回（$\lambda>0$）起きる事象について、次の事象が起きるまでの待ち時間$X$が従う分布を指数分布$\mathrm{Exp}(\lambda)$という。$\lambda$は事象が起きる頻度を表すパラメータであり、生起率と呼ばれる。例えば、平均して1時間に3件の問い合わせが来る窓口では、次の問い合わせまでの待ち時間は$\mathrm{Exp}(3)$（時間単位）に従う。

**密度関数の導出**：事象の発生が互いに独立に起こり、単位時間あたりの発生率が常に一定であると仮定すると、時間$x$の間の発生回数$N_x$は$\mathrm{Po}(\lambda x)$に従う。「次の事象までの待ち時間$X$が$x$を超える」ことは「時間$x$の間に事象が1回も起きない」ことと同値だから、

$$P(X>x) = P(N_x=0) = \frac{(\lambda x)^0 e^{-\lambda x}}{0!} = e^{-\lambda x} \quad (x \geq 0)$$

この$P(X>x)$を生存関数という。事象$\{X\leq x\}$は$\{X>x\}$の余事象であるから、累積分布関数は$F(x)=P(X\leq x)=1-P(X>x)=1-e^{-\lambda x}$である。これを微分すると密度関数

$$f(x) = F'(x) = \lambda e^{-\lambda x} \quad (x \geq 0)$$

が得られる。このとき期待値と分散は

$$E[X] = \frac{1}{\lambda}, \qquad \mathrm{Var}(X) = \frac{1}{\lambda^2}$$

である（導出は後述）。

**期待値の導出**：部分積分を使うと、

$$E[X]=\int_0^\infty x\lambda e^{-\lambda x}\,dx = \Bigl[-xe^{-\lambda x}\Bigr]_0^\infty+\int_0^\infty e^{-\lambda x}\,dx$$

指数関数$e^{-\lambda x}$は$x\to\infty$のとき任意の多項式よりも速く0に収束するため、$xe^{-\lambda x}\to0$である。よって

$$E[X] = \left[-\frac{1}{\lambda}e^{-\lambda x}\right]_0^\infty=\frac1\lambda$$

**分散の導出**：同様に部分積分を用いると、

$$E[X^2]=\int_0^\infty x^2\lambda e^{-\lambda x}\,dx = \Bigl[-x^2e^{-\lambda x}\Bigr]_0^\infty+\int_0^\infty 2xe^{-\lambda x}\,dx$$

$E[X]$の導出と同様の理由により $x^2e^{-\lambda x}\to0$（$x\to\infty$）なので境界項は0であり、

$$E[X^2] = \int_0^\infty 2xe^{-\lambda x}\,dx = \frac{2}{\lambda}\int_0^\infty x\lambda e^{-\lambda x}\,dx = \frac{2}{\lambda}E[X] = \frac{2}{\lambda^2}$$

したがって

$$\mathrm{Var}(X) = E[X^2]-(E[X])^2 = \frac{2}{\lambda^2}-\frac{1}{\lambda^2} = \frac{1}{\lambda^2}$$

**無記憶性**：$P(X > s + t \mid X > s) = P(X > t)$（すでに $s$ 待った事実が、追加の待ち時間の分布に影響しない）。

**証明**：条件付き確率の定義より $P(X>s+t \mid X>s) = \dfrac{P(X>s+t\cap X>s)}{P(X>s)}$ である。ここで $t\geq0$ より $s+t\geq s$ であり、$X>s+t$ ならば $X>s$ も成り立つ。したがって $\{X>s+t\}\subset\{X>s\}$ が成り立つ。このとき、事象$X>s+t\cap X>s$は事象$X>s+t$と同値であり、$P(X>s+t\cap X>s)=P(X>s+t)$ となる。したがって

$$P(X>s+t \mid X>s) = \frac{P(X>s+t)}{P(X>s)}$$

前述の生存関数 $P(X>x)=e^{-\lambda x}$ より、

$$P(X>s+t \mid X>s) = \frac{e^{-\lambda(s+t)}}{e^{-\lambda s}} = e^{-\lambda t} = P(X>t)$$

$\blacksquare$

> [!NOTE]
> 指数分布は、無記憶性を持つ唯一の連続分布であることが知られている。離散分布では、幾何分布が同様の無記憶性を持つ。

---

## まとめ

指数分布は、ポアソン過程における待ち時間を表す分布で、期待値$\frac1\lambda$・分散$\frac{1}{\lambda^2}$は累積分布関数を部分積分することで導出できます。無記憶性（過去の経過時間が今後の待ち時間の分布に影響しない）という特徴的な性質は、条件付き確率の定義から直接証明できます。

---

## 関連ページ

- [確率分布](distributions.md)
