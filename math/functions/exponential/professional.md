---
title: 指数関数（専門）
description: "指数型分布族・母関数・行列指数関数"
difficulty: 5
tags: [math,functions,exponential,professional]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 指数関数（専門）
    href: /math/functions/exponential/professional.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
    href: advanced.html
  - text: 専門
---








# 指数関数（発展）
行列指数関数・指数型分布族・ラプラス変換を扱います。

## このページで扱うこと
- 行列指数関数 $e^A$ と常微分方程式
- 指数型分布族（統計）
- ラプラス変換

## 前提知識
- [指数関数](../exponential/standard.md)
- [行列](../../linear-algebra/matrices/standard.md)
- [積分](../calculus/integrals/standard.md)

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

- [指数関数](../exponential/standard.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
- [確率（専門）](../../statistics/probability/professional.md)
