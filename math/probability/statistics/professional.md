---
title: 統計
description: "推定論・検定論・ベイズ統計"
goal: "フィッシャー情報量・クラメール＝ラオ下界を理解し、ネイマン＝ピアソンの補題とベイズ推定の枠組みを説明できるようになる"
tags: [math,probability,statistics]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 確率
    path: /math/probability/index.md
  - title: 統計
    path: /math/probability/statistics/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 統計（標準）
    path: /math/probability/statistics/standard.md
  - title: 確率分布（専門）
    path: /math/probability/distributions/professional.md
  - title: 積分（専門）
    path: /math/analysis/integrals/professional.md
---

## 十分統計量

**定義**：$X_1, \ldots, X_n \sim f(x; \theta)$ のとき、統計量 $T = T(X_1, \ldots, X_n)$ が $\theta$ の**十分統計量**であるとは、$T$ が与えられたもとでの標本の条件付き分布が $\theta$ に依存しないことです。

**因子化定理**（ネイマン＝フィッシャー）：$T$ が十分統計量 $\iff$ 尤度が $f(x_1,\ldots,x_n;\theta) = g(T(x);\theta)h(x)$ と分解できる。

---

## フィッシャー情報量とクラメール＝ラオ下界

**フィッシャー情報量**：

$$I(\theta) = E\left[\left(\frac{\partial}{\partial\theta} \log f(X; \theta)\right)^2\right] = -E\left[\frac{\partial^2}{\partial\theta^2} \log f(X; \theta)\right]$$

**クラメール＝ラオ下界**：不偏推定量 $\hat{\theta}$ の分散の下界：

$$\mathrm{Var}(\hat{\theta}) \geq \frac{1}{nI(\theta)}$$

この下界を達成する推定量を**有効推定量**といいます。指数型分布族では最尤推定量が有効推定量になります。

---

## ネイマン＝ピアソンの補題

$H_0: \theta = \theta_0$ vs $H_1: \theta = \theta_1$ の単純仮説検定において、\
有意水準 $\alpha$ のもとで検出力を最大化する検定（**最強力検定**）は**尤度比検定**です：

$$\Lambda(x) = \frac{f(x; \theta_1)}{f(x; \theta_0)} > k \text{ のとき } H_0 \text{ を棄却}$$

この補題は検定理論の出発点であり、複合仮説への拡張（一様最強力検定）の基礎となります。

---

## ベイズ統計

**事前分布** $p(\theta)$（データ観測前の $\theta$ の信念）と**尤度** $p(x \mid \theta)$ から**事後分布**を求めます：

$$p(\theta \mid x) = \frac{p(x \mid \theta) p(\theta)}{p(x)} \propto p(x \mid \theta) p(\theta)$$

**点推定**：事後平均 $E[\theta \mid x]$ または MAP 推定 $\arg\max p(\theta \mid x)$。

**共役事前分布**：事前・事後が同じ分布族に属する場合。

| 尤度 | 共役事前 | 事後 |
|------|---------|------|
| $\mathrm{Binomial}(n,p)$ | $\mathrm{Beta}(\alpha,\beta)$ | $\mathrm{Beta}(\alpha+k, \beta+n-k)$ |
| $\mathrm{Poisson}(\lambda)$ | $\mathrm{Gamma}(\alpha,\beta)$ | $\mathrm{Gamma}(\alpha+\sum x_i, \beta+n)$ |
| $N(\mu, \sigma^2)$ | $N(\mu_0, \tau^2)$ | $N(\mu_n, \sigma_n^2)$ |

**参考文献**：Casella, G. & Berger, R. L. (2002). *Statistical Inference* (2nd ed.). Duxbury.

---

## 関連ページ

- [統計（標準）](standard.md)
- [確率分布（専門）](../distributions/professional.md)
- [確率（専門）](../probability/professional.md)
