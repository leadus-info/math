---
title: 一次関数
description: "アフィン変換・線形写像・超平面"
goal: "一次関数を厳密に定義し、主要な定理を証明できるようになる"
tags: [math,specific-functions,linear]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 具体的な関数
    path: /math/specific-functions/index.md
  - title: 一次関数
    path: /math/specific-functions/linear/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 一次関数
    path: /math/specific-functions/linear/introduction.md
  - title: 行列
    path: /math/linear-algebra/matrices/introduction.md
  - title: ベクトル
    path: /math/linear-algebra/vectors/introduction.md
---

## アフィン写像と線形写像

**定義**：$f: \mathbb{R}^n \to \mathbb{R}^m$ が**線形写像**とは $f(\alpha x + \beta y) = \alpha f(x) + \beta f(y)$ が成り立つこと。

**定義**：$f(x) = Ax + b$（$A$ は行列、$b$ はベクトル）を**アフィン写像**といいます。$b = 0$ なら線形写像。

1変数の一次関数 $y = ax + b$ は $\mathbb{R} \to \mathbb{R}$ のアフィン写像です。$b \neq 0$ なら線形写像ではありません（$f(0) = b \neq 0$）。

---

## $n$ 次元の超平面

$$\boldsymbol{w}^\top \boldsymbol{x} + b = 0 \quad (\boldsymbol{w}, \boldsymbol{x} \in \mathbb{R}^n)$$

これは $n-1$ 次元の**超平面**（hyplerplane）です。1次元なら点、2次元なら直線、3次元なら通常の平面。

点 $\boldsymbol{x}_0$ から超平面までの距離：$\dfrac{|\boldsymbol{w}^\top \boldsymbol{x}_0 + b|}{\|\boldsymbol{w}\|}$

---

## 最小二乗法

データ点 $(x_i, y_i)$ への最良の線形近似を求める問題：

$$\min_{a,b} \sum_{i=1}^n (y_i - ax_i - b)^2$$

行列形式 $X\boldsymbol{\beta} = \boldsymbol{y}$ に書き換えると、正規方程式 $X^\top X\boldsymbol{\beta} = X^\top \boldsymbol{y}$ の解が最小二乗解です。$X^\top X$ が正則なら $\boldsymbol{\beta} = (X^\top X)^{-1}X^\top \boldsymbol{y}$。

---

## 参考文献

Strang, G. (2016). *Introduction to Linear Algebra* (5th ed.). Wellesley-Cambridge Press.

---

## 関連ページ

- [一次関数（標準）](standard.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
