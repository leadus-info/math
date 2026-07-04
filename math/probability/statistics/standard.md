---
title: 統計
description: "推定・検定・回帰分析"
goal: "点推定・区間推定・仮説検定の手順を理解し、単回帰分析を実行できるようになる"
tags: [math,probability,statistics]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 確率
    path: /math/probability/index.md
  - title: 統計
    path: /math/probability/statistics/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 統計（入門）
    path: /math/probability/statistics/introduction.md
  - title: 確率分布（標準）
    path: /math/probability/distributions/standard.md
---

## 記述統計

**標本平均**：$\bar{x} = \frac{1}{n}\sum_{i=1}^n x_i$

**標本分散**：$s^2 = \frac{1}{n-1}\sum_{i=1}^n (x_i - \bar{x})^2$（不偏分散、$n-1$ で割る）

**標本標準偏差**：$s = \sqrt{s^2}$

**相関係数**：$r = \frac{\sum(x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum(x_i-\bar{x})^2 \sum(y_i-\bar{y})^2}} \in [-1, 1]$

---

## 点推定と区間推定

**点推定**：標本から母数（母平均 $\mu$、母分散 $\sigma^2$ など）を1つの値で推定する。\
標本平均 $\bar{x}$ は母平均 $\mu$ の不偏推定量（$E[\bar{x}] = \mu$）。

**区間推定**：推定値の不確実性を「幅」で表す。

母平均の $95\%$ 信頼区間（母分散既知、$n$ 大）：

$$\bar{x} \pm 1.96 \cdot \frac{\sigma}{\sqrt{n}}$$

「この手続きを繰り返すと、$95\%$ の割合で真の $\mu$ を含む区間が得られる」という意味です。

---

## 仮説検定

**帰無仮説** $H_0$（否定したい仮説）と**対立仮説** $H_1$ を設定し、\
データが $H_0$ のもとでどれほど起こりにくいかを**$p$ 値**で測ります。

$p$ 値 $<$ 有意水準 $\alpha$（通常 $0.05$）のとき $H_0$ を**棄却**します。

**手順**：
1. $H_0$, $H_1$ を設定する
2. 検定統計量を計算する
3. $p$ 値を求める
4. $p < \alpha$ なら $H_0$ を棄却、さもなくば棄却しない

**例**：コインが公平か検定する。$H_0$：表の確率 $= 0.5$。10回中9回表が出た場合の $p$ 値は？\
$P(X \geq 9) = \binom{10}{9}(0.5)^{10} + \binom{10}{10}(0.5)^{10} = \frac{11}{1024} \approx 0.011 < 0.05$\
→ $H_0$ を棄却（有意水準 $5\%$ で）。

---

## 単回帰分析

$x$（説明変数）から $y$（目的変数）を予測するモデル：$y = \beta_0 + \beta_1 x + \varepsilon$

最小二乗法で係数を推定します：

$$\hat{\beta}_1 = \frac{\sum(x_i - \bar{x})(y_i - \bar{y})}{\sum(x_i - \bar{x})^2}, \quad \hat{\beta}_0 = \bar{y} - \hat{\beta}_1 \bar{x}$$

**決定係数** $R^2 = r^2 \ (0 \leq R^2 \leq 1)$：モデルがデータのばらつきを何割説明するか。

---

## 関連ページ

- [確率分布（標準）](../distributions/standard.md)
- [一次関数（専門）](../../specific-functions/linear/professional.md) — 最小二乗法の理論
- [統計（専門）](professional.md)
