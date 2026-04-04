---
title: 一次関数
description: "アフィン変換・線形写像・超平面"
tags: [math,functions,linear]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 関数
    path: /math/functions/index.html
  - title: 一次関数
    path: /math/functions/linear/professional.html
levels:
  - level: 入門
    path: introduction.html
  - level: 標準
    path: standard.html
  - level: 専門
level: 専門
requires:
  - title: 一次関数
    path: /math/functions/linear/introduction.html
  - title: 行列
    path: /math/linear-algebra/matrices/introduction.html
  - title: ベクトル
    path: /math/linear-algebra/vectors/introduction.html
---


## このページで扱うこと

アフィン写像・線形写像・$n$ 次元超平面を扱います。

- 線形写像とアフィン写像の違い
- $n$ 次元での一次関数（超平面）
- 最小二乗法との接続

---

## 線形写像とアフィン写像

**線形写像**: $f(\alpha x + \beta y) = \alpha f(x) + \beta f(y)$（原点を保つ）

**アフィン写像**: $f(x) = Ax + b$（線形写像 + 平行移動）

一次関数 $y = ax + b$ はアフィン写像（$b \neq 0$ のとき線形でない）。

---

## $n$ 次元超平面

$$\boldsymbol{w}^\top \boldsymbol{x} + b = 0 \quad (\boldsymbol{w}, \boldsymbol{x} \in \mathbb{R}^n)$$

点 $\boldsymbol{x}_0$ からの距離: $\dfrac{|\boldsymbol{w}^\top \boldsymbol{x}_0 + b|}{\|\boldsymbol{w}\|}$

---

## 最小二乗法

データ点 $(x_i, y_i)$ への最良の一次近似を求める:

$$\min_{a,b} \sum_i (y_i - ax_i - b)^2$$

解は正規方程式 $X^\top X \boldsymbol{\beta} = X^\top \boldsymbol{y}$ から得られます。

---

## 関連ページ

- [一次関数](introduction.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
- [確率（専門）](../../statistics/probability/professional.md)
