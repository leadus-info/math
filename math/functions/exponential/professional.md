---
title: 指数関数
description: "指数型分布族・母関数・行列指数関数"
tags: [math,functions,exponential]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 関数
    url: /math/functions/index.html
  - title: 指数関数
    url: /math/functions/exponential/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: 指数関数
    url: /math/functions/exponential/introduction
  - title: 行列
    url: /math/linear-algebra/matrices/introduction
  - title: 積分
    url: /math/functions/integrals/introduction
---


> この記事は [標準](standard.md) の続きです。先に標準を読むことを推奨します。

行列指数関数・指数型分布族・ラプラス変換を扱います。

## このページで扱うこと
- 行列指数関数 $e^A$ と常微分方程式
- 指数型分布族（統計）
- ラプラス変換

---

## 行列指数関数

$$e^A = \sum_{n=0}^{\infty}\frac{A^n}{n!}$$

線形常微分方程式 $\dot{x} = Ax$ の解: $x(t) = e^{At}x(0)$

---

## ラプラス変換

$$\mathcal{L}\{f(t)\}(s) = \int_0^{\infty} f(t)e^{-st}\,dt$$

微分・積分を代数的操作に変換します（工学での制御理論に必須）。

---

## 指数型分布族

$$p(x;\theta) = h(x)\exp(\eta(\theta)T(x) - A(\theta))$$

正規分布・ポアソン分布・ベルヌーイ分布を統一する枠組み。

---

## 関連ページ

- [指数関数](introduction.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
- [確率（専門）](../../statistics/probability/professional.md)
