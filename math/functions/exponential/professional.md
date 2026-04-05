---
title: 指数関数
description: "指数型分布族・母関数・行列指数関数"
tags: [math,functions,exponential]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/functions/index.md
  - title: 指数関数
    path: /math/functions/exponential/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 指数関数
    path: /math/functions/exponential/introduction.md
  - title: 行列
    path: /math/linear-algebra/matrices/introduction.md
  - title: 積分
    path: /math/functions/integrals/introduction.md
---

## 行列指数関数

正方行列 $A$ に対して**行列指数関数**を定義します：

$$e^A = \sum_{n=0}^{\infty}\frac{A^n}{n!} = I + A + \frac{A^2}{2!} + \frac{A^3}{3!} + \cdots$$

この級数はすべての正方行列に対して収束します。

**主な性質**：
- $e^0 = I$（単位行列）
- $AB = BA$ ならば $e^{A+B} = e^A e^B$（非可換の場合は成立しない）
- $e^A$ は常に可逆で $(e^A)^{-1} = e^{-A}$

---

## 常微分方程式への応用

線形常微分方程式系 $\dot{\boldsymbol{x}} = A\boldsymbol{x}$（$A$ は定数行列）の解：

$$\boldsymbol{x}(t) = e^{At}\boldsymbol{x}(0)$$

これは1次元の場合 $\dot{x} = ax$ の解 $x(t) = e^{at}x(0)$ の自然な行列版です。

**例**：調和振動子 $\ddot{u} = -\omega^2 u$ は\
$\dot{\boldsymbol{x}} = \begin{pmatrix}0&1\\-\omega^2&0\end{pmatrix}\boldsymbol{x}$ と書け、\
解は $e^{At}$ で表されます。これが $\sin$、$\cos$ と結びつきます。

---

## ラプラス変換

$$\mathcal{L}\{f(t)\}(s) = \int_0^{\infty} f(t)e^{-st}\,dt$$

微分・積分の操作が代数的演算に変換されます：

$$\mathcal{L}\{f'(t)\}(s) = s\mathcal{L}\{f\}(s) - f(0)$$

常微分方程式の初期値問題を代数方程式に変換し、逆変換で解を復元します。\
制御工学・信号処理で広く使われます。

**参考文献**：Hirsch, M. W., Smale, S., & Devaney, R. L. (2013). *Differential Equations, Dynamical Systems, and an Introduction to Chaos* (3rd ed.). Academic Press.

---

## 関連ページ

- [指数関数](standard.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
- [確率（専門）](../../statistics/probability/professional.md)
