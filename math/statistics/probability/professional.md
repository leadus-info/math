---
title: 確率
description: "測度論的確率・大数の法則・中心極限定理"
goal: "コルモゴロフの公理から確率空間を構成し、大数の法則と中心極限定理の内容を正確に述べられるようになる"
tags: [math,statistics,probability]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 統計・確率
    path: /math/statistics/index.md
  - title: 確率
    path: /math/statistics/probability/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 確率（標準）
    path: /math/statistics/probability/standard.md
  - title: 積分（専門）
    path: /math/functions/integrals/professional.md
---

## 測度論的確率論

**定義**：**確率空間**とは $( \Omega, \mathcal{F}, P )$ の三つ組で：

- $\Omega$：標本空間（起こりうるすべての結果の集合）
- $\mathcal{F}$：$\sigma$-代数（$\Omega$ の部分集合のうち「事象」とみなせるもの全体）
- $P: \mathcal{F} \to [0,1]$：確率測度（$P(\Omega)=1$、加算加法的）

**確率変数**：可測写像 $X: \Omega \to \mathbb{R}$（事象を実数に対応させる関数）

**期待値**：$E[X] = \int_\Omega X(\omega) \, dP(\omega)$（ルベーグ積分）

---

## 大数の法則

独立同分布（i.i.d.）の確率変数 $X_1, X_2, \ldots$（$E[X_i] = \mu$）に対して $S_n = X_1 + \cdots + X_n$ とすると：

**弱い大数の法則**：$\forall \varepsilon > 0$, $P\left(\left|\frac{S_n}{n} - \mu\right| > \varepsilon\right) \to 0$（$n \to \infty$）

**強い大数の法則**：$P\left(\lim_{n \to \infty} \frac{S_n}{n} = \mu\right) = 1$

強い大数の法則は「ほぼ確実に（概収束）」の意味で、弱い法則より強い主張です。

---

## 中心極限定理

$E[X_i] = \mu$、$\text{Var}(X_i) = \sigma^2 > 0$ のとき：

$$\frac{S_n - n\mu}{\sqrt{n} \sigma} \xrightarrow{d} N(0, 1) \quad (n \to \infty)$$

$\xrightarrow{d}$ は**分布収束**（法則収束）を表します。すなわち任意の $x$ に対して：

$$P\left(\frac{S_n - n\mu}{\sqrt{n}\sigma} \leq x\right) \to \Phi(x)$$

（$\Phi$ は標準正規分布の累積分布関数）

分布の形に依らず、平均・分散が有限ならば正規分布に収束します。これが統計的推測の理論的根拠です。

---

## 確率過程

**ブラウン運動**（ウィーナー過程）$\{B_t\}_{t \geq 0}$：

- $B_0 = 0$
- 独立増分：$s < t$ のとき $B_t - B_s \sim N(0, t-s)$
- ほぼ確実に連続な標本路

ブラウン運動は確率微分方程式（SDE）の理論の基礎となり、金融数学（ブラック＝ショールズ方程式）や物理学に応用されます。

**参考文献**：Billingsley, P. (1995). *Probability and Measure* (3rd ed.). Wiley.

---

## 関連ページ

- [確率（標準）](standard.md)
- [積分（専門）](../../functions/integrals/professional.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
