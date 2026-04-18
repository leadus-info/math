---
title: 指数関数
description: "指数型分布族・母関数・行列指数関数"
goal: "指数関数を厳密に定義し、主要な定理を証明できるようになる"
tags: [math,functions,exponential]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/analysis/index.md
  - title: 指数関数
    path: /math/specific-functions/exponential/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 指数関数
    path: /math/specific-functions/exponential/introduction.md
  - title: 行列
    path: /math/linear-algebra/matrices/introduction.md
  - title: 積分
    path: /math/analysis/integrals/introduction.md
---

## 行列指数関数

**定義**：正方行列 $A$ に対して、

$$e^A = \sum_{n=0}^\infty \frac{A^n}{n!} = I + A + \frac{A^2}{2!} + \cdots$$

この級数はすべての正方行列に対して収束します。

**性質**：
- $e^0 = I$
- $AB = BA$ のとき $e^{A+B} = e^A e^B$（非可換では一般に成立しない）
- $(e^A)^{-1} = e^{-A}$

---

## 線形常微分方程式への応用

$\dot{\boldsymbol{x}} = A\boldsymbol{x}$（$A$ は定数行列）の解：

$$\boldsymbol{x}(t) = e^{At}\boldsymbol{x}(0)$$

$A$ が対角化可能なら $e^{At}$ は固有値・固有ベクトルで明示的に計算できます。

---

## ラプラス変換

**定義**：$\mathcal{L}\{f(t)\}(s) = \displaystyle\int_0^\infty f(t)e^{-st}\,dt$

$$\mathcal{L}\{f'(t)\}(s) = s\mathcal{L}\{f\}(s) - f(0)$$

微分・積分を代数演算に変換し、常微分方程式の初期値問題を代数方程式に帰着させます。制御工学・信号処理で広く使われます。

---

## 指数型分布族

$$p(x; \theta) = h(x)\exp(\eta(\theta)T(x) - A(\theta))$$

正規分布・ポアソン分布・ガンマ分布などを統一する枠組み。$A(\theta)$ は規格化のための関数（対数分配関数）。

**参考文献**：Hirsch, M. W., Smale, S., & Devaney, R. L. (2013). *Differential Equations, Dynamical Systems, and an Introduction to Chaos* (3rd ed.). Academic Press.

---

## 関連ページ

- [指数関数（標準）](standard.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
