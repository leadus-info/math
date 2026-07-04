---
title: 確率分布
description: "指数型分布族・特性関数・多変量分布"
goal: "指数型分布族の定義と性質を述べ、特性関数・モーメント母関数を使って分布を特徴づけられるようになる"
tags: [math,probability,distributions]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 確率
    path: /math/probability/index.md
  - title: 確率分布
    path: /math/probability/distributions/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 確率分布（標準）
    path: /math/probability/distributions/standard.md
  - title: 確率（専門）
    path: /math/probability/probability/professional.md
  - title: 積分（専門）
    path: /math/analysis/integrals/professional.md
---

## モーメント母関数と特性関数

確率変数 $X$ の**モーメント母関数（MGF）**：

$$M_X(t) = E[e^{tX}] = \sum_{n=0}^\infty \frac{E[X^n]}{n!} t^n$$

$M_X(t)$ が $t=0$ の近傍で存在するとき $n$ 次モーメント $E[X^n] = M_X^{(n)}(0)$。

**特性関数**：$\varphi_X(t) = E[e^{itX}]$（常に存在、$|\varphi_X(t)| \leq 1$）

**逆転公式**：$f(x) = \frac{1}{2\pi}\int_{-\infty}^\infty e^{-itx} \varphi_X(t)\,dt$

特性関数は分布を一意に定め、独立な確率変数の和の分布計算（$\varphi_{X+Y} = \varphi_X \cdot \varphi_Y$）に有用です。

---

## 指数型分布族

多くの基本的な分布を統一的に扱う枠組み：

$$f(x; \theta) = h(x) \exp\left(\eta(\theta)^\top T(x) - A(\theta)\right)$$

- $T(x)$：十分統計量
- $\eta(\theta)$：自然パラメータ
- $A(\theta)$：対数分配関数（規格化定数の対数）

**例**：正規分布・ベルヌーイ分布・ポアソン分布・ガンマ分布はすべて指数型分布族。

**性質**：$E[T(X)] = \nabla A(\eta)$、$\mathrm{Cov}(T(X)) = \nabla^2 A(\eta)$（対数分配関数の勾配・ヘッセ行列で期待値・分散が得られる）。

機械学習の一般化線形モデル（GLM）の理論的基盤です。

---

## 多変量正規分布

$\boldsymbol{X} = (X_1, \ldots, X_n)^\top \sim N(\boldsymbol{\mu}, \Sigma)$

$$f(\boldsymbol{x}) = \frac{1}{(2\pi)^{n/2}|\Sigma|^{1/2}} \exp\left(-\frac{1}{2}(\boldsymbol{x}-\boldsymbol{\mu})^\top \Sigma^{-1} (\boldsymbol{x}-\boldsymbol{\mu})\right)$$

$\Sigma$（共分散行列）が正定値対称のとき密度が存在します。

**周辺分布**：$X_i \sim N(\mu_i, \Sigma_{ii})$（周辺分布も正規）

**条件付き分布**：$X_1 \mid X_2 = x_2$ も正規分布（線形回帰の理論的基礎）。

---

## 収束の概念

確率変数列 $\{X_n\}$ の収束には複数の種類があります。

| 収束 | 定義 |
|------|------|
| 概収束 | $P(\lim X_n = X) = 1$ |
| 確率収束 | $\forall \varepsilon > 0,\ P(|X_n - X| > \varepsilon) \to 0$ |
| $L^p$ 収束 | $E[|X_n - X|^p] \to 0$ |
| 分布収束 | $F_{X_n}(x) \to F_X(x)$（連続点で） |

包含関係：概収束 $\Rightarrow$ 確率収束 $\Rightarrow$ 分布収束（逆は一般に成立しない）。

**参考文献**：Billingsley, P. (1995). *Probability and Measure* (3rd ed.). Wiley.

---

## 関連ページ

- [確率分布（標準）](standard.md)
- [確率（専門）](../probability/professional.md)
- [積分（専門）](../../analysis/integrals/professional.md)
