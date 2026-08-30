---
title: 二項分布
description: "n回の独立試行での成功回数が従う二項分布の定義と期待値・分散を、ベルヌーイ確率変数の和として厳密に導出し、その使いどころを解説する"
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

[二項分布](../../advanced/probability/binomial-distribution.md)では期待値・分散を直感的な理解にとどめましたが、本記事では成功・失敗を表す確率変数の和として捉え直し、厳密に導出し直します。

コインを10回投げて表が出る回数のように、$n$ 回の独立な試行で各回成功確率 $p$ のとき、成功回数 $X$ の分布：

$$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k} \quad (k = 0, 1, \ldots, n)$$

$$E[X] = np, \quad \mathrm{Var}(X) = np(1-p)$$

**例**：コイン10回投げて表が出る回数は $B(10, 0.5)$。$E[X] = 5$、$\mathrm{Var}(X) = 2.5$。

二項分布が当てはまるのは、各試行が独立で、結果が「成功」「失敗」の2値に定まり、成功確率 $p$ と試行回数 $n$ が固定されている場合です。例えば、不良品率 $p$ の製品ラインから $n$ 個を抜き取って検査したときの不良品数や、賛成率 $p$ の集団から無作為に $n$ 人を選んでアンケートを取ったときの賛成人数も、この条件を満たすため $B(n, p)$ に従います。

---

## ベルヌーイ確率変数の和としての導出

$E[X] = np$、$\mathrm{Var}(X) = np(1-p)$ は、定義の和を直接計算する代わりに、$X$ を成功・失敗を表す確率変数の和として捉えると簡潔に導けます。成功なら $1$、失敗なら $0$ の値を取る確率変数のことを**ベルヌーイ確率変数**といいます。$i$ 回目の試行の成功・失敗を表すベルヌーイ確率変数を

$$X_i = \begin{cases}1 & (i \text{ 回目が成功}) \\ 0 & (i \text{ 回目が失敗})\end{cases}, \qquad X = X_1 + X_2 + \cdots + X_n$$

とすると、まず $E[X_i] = 1\times p + 0\times(1-p) = p$ です。また $E[X_i^2] = 1^2\times p + 0^2\times(1-p) = p$ なので、$\mathrm{Var}(X_i) = E[X_i^2] - (E[X_i])^2 = p - p^2 = p(1-p)$ となります。期待値は独立性を仮定しなくても和に分解できる（**期待値の線形性**）ので、

$$E[X] = \sum_{i=1}^n E[X_i] = np$$

が直ちに従います。一方、分散は一般には和に分解できませんが、$X_1, \ldots, X_n$ が**独立**なので、

$$\mathrm{Var}(X) = \sum_{i=1}^n \mathrm{Var}(X_i) = np(1-p)$$

が成り立ちます。ここで使っているのは「独立な確率変数の分散は和に分解できる」という性質で、以下のように証明できます。

**定義**（独立性）：確率変数 $X, Y$ が**独立**であるとは、任意の $x, y$ について $P(X=x, Y=y) = P(X=x)P(Y=y)$ が成り立つことをいいます。

**定理**：$X, Y$ が独立な確率変数のとき、$\mathrm{Var}(X+Y) = \mathrm{Var}(X) + \mathrm{Var}(Y)$ が成り立つ。

**証明**：分散の定義と期待値の線形性から

$(X+Y)^2$ と $(E[X+Y])^2$ をそれぞれ展開すると

$$E[(X+Y)^2] = E[X^2+2XY+Y^2] = E[X^2]+2E[XY]+E[Y^2]$$

$$(E[X+Y])^2 = (E[X]+E[Y])^2 = (E[X])^2+2E[X]E[Y]+(E[Y])^2$$

なので、分散の定義 $\mathrm{Var}(X+Y)=E[(X+Y)^2]-(E[X+Y])^2$ に代入して同類項を整理すると

$$\mathrm{Var}(X+Y) = \{E[X^2]-(E[X])^2\} + \{E[Y^2]-(E[Y])^2\} + 2\{E[XY]-E[X]E[Y]\}$$

$$= \mathrm{Var}(X) + \mathrm{Var}(Y) + 2\{E[XY]-E[X]E[Y]\}$$

が成り立つ。$X, Y$ が独立であることから、$P(X=x,Y=y)=P(X=x)P(Y=y)$ を用いて

$$E[XY] = \sum_x\sum_y xy\,P(X=x,Y=y) = \sum_x\sum_y xy\,P(X=x)P(Y=y)$$

ここで、内側の $y$ についての和の中では $xP(X=x)$ は $y$ に依存しない定数として和の外に出せるので

$$\sum_x\sum_y xy\,P(X=x)P(Y=y) = \sum_x xP(X=x)\Big(\sum_y yP(Y=y)\Big) = \Big(\sum_x xP(X=x)\Big)\Big(\sum_y yP(Y=y)\Big) = E[X]E[Y]$$

なので $E[XY]-E[X]E[Y]=0$。したがって $\mathrm{Var}(X+Y)=\mathrm{Var}(X)+\mathrm{Var}(Y)$。$\square$

$X_1, \ldots, X_n$ は互いに独立なので、部分和 $S_{n-1} = X_1 + \cdots + X_{n-1}$ と $X_n$ もまた独立であり、上の2変数の場合の証明を数学的帰納法で繰り返し適用すると、$\mathrm{Var}(X_1+\cdots+X_n) = \sum_{i=1}^n \mathrm{Var}(X_i)$ が成り立つことが示せます。こうして先ほどの $\mathrm{Var}(X) = \sum_{i=1}^n \mathrm{Var}(X_i) = np(1-p)$ が正当化されました。組合せ論的な和 $\sum_k k\binom{n}{k}p^k(1-p)^{n-k}$ を直接計算するより、この分解の方がはるかに見通しがよいことに注意してください。

---

## まとめ

二項分布は、$n$回の独立な試行における成功回数の分布で、期待値は $np$、分散は $np(1-p)$ です。これらは、二項分布に従う確率変数をベルヌーイ確率変数の和として分解し、期待値の線形性と分散の独立性からの加法性を使うと簡潔に導出できます。

---

## 関連ページ

- [ポアソン分布](distributions-poisson.md)
