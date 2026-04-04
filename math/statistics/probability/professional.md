---
title: 確率
description: "測度論的確率論・確率過程・大数の法則"
tags: [math,statistics,probability]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 統計・確率
    path: /math/statistics/index.html
  - title: 確率
    path: /math/statistics/probability/professional.html
levels:
  - level: introduction
    path: introduction.html
  - level: standard
    path: standard.html
  - level: professional
level: professional
requires:
  - title: 確率
    path: /math/statistics/probability/introduction
  - title: 積分（専門）
    path: ../../functions/integrals/professional.md
  - title: 数列（専門）
    path: ../../functions/sequences/professional.md
---



> この記事は [標準](standard.md) の続きです。先に標準を読むことを推奨します。

測度論的確率論・確率過程・中心極限定理を扱います。

## このページで扱うこと
- 測度論的確率論（コルモゴロフの公理の完全版）
- 大数の法則と中心極限定理
- 確率過程（ブラウン運動・マルコフ連鎖）

---

## 測度論的確率論

確率空間 $(\Omega, \mathcal{F}, P)$: 標本空間・$\sigma$-代数・確率測度の三つ組。

確率変数 $X: \Omega \to \mathbb{R}$ は可測写像。

---

## 大数の法則（強）

$$P\left(\lim_{n\to\infty}\frac{S_n}{n} = \mu\right) = 1$$

---

## 中心極限定理

$$\frac{S_n - n\mu}{\sqrt{n}\sigma} \xrightarrow{d} N(0,1)$$

---

## ブラウン運動

連続時間確率過程 $\{B_t\}$: 独立増分・$B_t \sim N(0, t)$・連続な標本路。

確率微分方程式 $dX_t = \mu(X_t)dt + \sigma(X_t)dB_t$（イトー積分）。

---

## 関連ページ

- [確率](introduction.md)
- [積分（専門）](../../functions/integrals/professional.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
