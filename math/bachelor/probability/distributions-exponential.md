---
title: 指数分布
description: "事象の発生が独立かつ一定の頻度で起こるときの次の事象までの待ち時間が従う指数分布の定義・期待値・分散と、過去の経過時間に依存しない無記憶性という性質を解説する"
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

**定義**：$\lambda>0$ とする。密度関数が

$$f(x) = \begin{cases} \lambda e^{-\lambda x} & (x \geq 0) \\ 0 & (x < 0) \end{cases}$$

である連続分布を、パラメータ $\lambda$ の**指数分布** $\mathrm{Exp}(\lambda)$ という。

この分布は、次のような待ち時間を表す分布として現れる。事象が互いに独立に起こり、単位時間あたりの発生率が常に一定の $\lambda$ で、微小時間に2件以上が同時に起こらないとする。このとき、次の事象が起きるまでの待ち時間 $X$ は $\mathrm{Exp}(\lambda)$ に従う（下で導出する）。$\lambda$ は事象が起きる頻度を表し、**生起率**と呼ばれる。例えば、問い合わせがこの仮定を満たして平均1時間に3件来る窓口では、次の問い合わせまでの待ち時間は $\mathrm{Exp}(3)$（時間単位）に従う。ただし、平均頻度が $\lambda$ であるだけでは指数分布になるとは限らない（例えば、ちょうど20分おきに規則正しく来る場合は、平均は1時間に3件でも待ち時間は指数分布に従わない）。上の独立性などの仮定が必要である。

**密度関数の導出**：上の仮定のもとでは、時間 $x$ の間の平均発生回数は $\lambda x$ 回で、時間 $x$ の間の発生回数 $N_x$ はポアソン分布 $\mathrm{Po}(\lambda x)$ に従うことが知られている（この仮定を満たす事象の発生の仕方を**ポアソン過程**という。前提記事の、単位時間で $\mathrm{Po}(\lambda)$ に従うことを、長さ $x$ の時間に広げたものである。ここでは証明せずに用いる）。「次の事象までの待ち時間$X$が$x$を超える」ことは「時間$x$の間に事象が1回も起きない」ことと同値である（事象が時刻$x$までに1回も起きなければ、次の事象は必ず$x$より後に起こるため）。したがって、

$$P(X>x) = P(N_x=0) = \frac{(\lambda x)^0 e^{-\lambda x}}{0!} = e^{-\lambda x} \quad (x \geq 0)$$

この$P(X>x)$を生存関数という。事象$\{X\leq x\}$は$\{X>x\}$の余事象であるから、累積分布関数は$F(x)=P(X\leq x)=1-P(X>x)=1-e^{-\lambda x}$である。これを微分すると密度関数

$$f(x) = F'(x) = \lambda e^{-\lambda x} \quad (x \geq 0)$$

が得られ、上の定義と一致する（待ち時間は負にならないので、$x<0$ では $F(x)=0$、$f(x)=0$ である）。このとき期待値と分散は

$$E[X] = \frac{1}{\lambda}, \qquad \mathrm{Var}(X) = \frac{1}{\lambda^2}$$

である（導出は後述）。

**期待値の導出**：部分積分を使うと、

$$E[X]=\int_0^\infty x\lambda e^{-\lambda x}\,dx = \Bigl[-xe^{-\lambda x}\Bigr]_0^\infty+\int_0^\infty e^{-\lambda x}\,dx$$

指数関数$e^{-\lambda x}$は$x\to\infty$のとき任意の多項式よりも速く0に収束するため（ロピタルの定理などから従う既知の事実であり、ここでは証明の対象としない）、$xe^{-\lambda x}\to0$である。よって

$$E[X] = \left[-\frac{1}{\lambda}e^{-\lambda x}\right]_0^\infty=\frac1\lambda$$

**分散の導出**：同様に部分積分を用いると、

$$E[X^2]=\int_0^\infty x^2\lambda e^{-\lambda x}\,dx = \Bigl[-x^2e^{-\lambda x}\Bigr]_0^\infty+\int_0^\infty 2xe^{-\lambda x}\,dx$$

$E[X]$の導出と同様の理由により $x^2e^{-\lambda x}\to0$（$x\to\infty$）なので境界項は0であり、

$$E[X^2] = \int_0^\infty 2xe^{-\lambda x}\,dx$$

ここで、$\lambda$で割って掛け直すことで、被積分関数を$E[X]$の積分の形（$E[X]=\int_0^\infty x\lambda e^{-\lambda x}\,dx$）に帰着させる。

$$E[X^2] = \frac{2}{\lambda}\int_0^\infty x\lambda e^{-\lambda x}\,dx = \frac{2}{\lambda}E[X] = \frac{2}{\lambda^2}$$

（最後の等号では$E[X]=\frac1\lambda$、すなわち前節「期待値の導出」の結果を用いた。）

したがって

$$\mathrm{Var}(X) = E[X^2]-(E[X])^2 = \frac{2}{\lambda^2}-\frac{1}{\lambda^2} = \frac{1}{\lambda^2}$$

**無記憶性**：任意の $s, t \geq 0$ に対して

$$P(X > s + t \mid X > s) = P(X > t)$$

が成り立つ。左辺は、すでに $s$ だけ待って事象がまだ起きていないという条件のもとで、そこからさらに $t$ より長く待つ確率である。右辺は、待ち始めた時点から $t$ より長く待つ確率である。この2つが等しいので、すでに $s$ 待ったかどうかは、そこから先の待ち時間の分布に影響しない。

**証明**：$P(X>s)=e^{-\lambda s}>0$ なので、条件付き確率が定義できる。条件付き確率の定義より

$$P(X>s+t \mid X>s) = \frac{P(X>s+t\cap X>s)}{P(X>s)}$$

である。ここで $t\geq0$ より $s+t\geq s$ であり、$X>s+t$ ならば $X>s$ も成り立つ。したがって

$$\{X>s+t\}\subset\{X>s\}$$

が成り立つ。このとき、事象$X>s+t\cap X>s$は事象$X>s+t$と同値であり、$P(X>s+t\cap X>s)=P(X>s+t)$ となる。したがって

$$P(X>s+t \mid X>s) = \frac{P(X>s+t)}{P(X>s)}$$

前述の生存関数 $P(X>x)=e^{-\lambda x}$ より、

$$P(X>s+t \mid X>s) = \frac{e^{-\lambda(s+t)}}{e^{-\lambda s}} = e^{-\lambda t} = P(X>t)$$

$\blacksquare$

> [!NOTE]
> 指数分布は、無記憶性を持つ唯一の連続分布であることが知られている。これは、無記憶性の定義と同値な関数方程式$P(X>s+t)=P(X>s)P(X>t)$（指数型のコーシーの関数方程式）に由来する。
>
> この関数方程式の解は、（生存関数が単調減少であることから）指数関数に限られることが知られているが、詳細な証明は割愛する。
>
> 離散分布では、幾何分布が同様の無記憶性を持つ。幾何分布は、各試行の成功確率が一定で、初めて成功するまでの試行回数が従う離散分布である。

---

## まとめ

指数分布は、事象の発生が独立かつ一定の頻度で起こるときの待ち時間を表す分布で、期待値$\frac1\lambda$・分散$\frac{1}{\lambda^2}$は、密度関数 $f(x)=\lambda e^{-\lambda x}$ に $x$(分散では $x^2$)を掛けたものを部分積分することで導出できます。無記憶性（過去の経過時間が今後の待ち時間の分布に影響しない）という特徴的な性質は、条件付き確率の定義から直接証明できます。

---

## 関連ページ

- [確率分布](distributions.md)
