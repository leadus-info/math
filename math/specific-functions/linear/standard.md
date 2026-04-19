---
title: 一次関数
description: "直線のグラフと傾き"
goal: "一次関数の定義・主要な定理・代表的な計算を理解し、後続のトピックに進める基礎を身につける"
tags: [math,specific-functions,linear]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 具体的な関数
    path: /math/specific-functions/index.md
  - title: 一次関数
    path: /math/specific-functions/linear/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 四則演算
    path: professional.md
  - title: 等号・等式
    path: /math/algebra/equations/introduction.md
---

## 一次関数の定義

**定義**：$f(x) = ax + b$（$a, b$ は定数）を**一次関数**といいます。

- $a$：**傾き**（$x$ が1増えると $y$ が $a$ 増える）
- $b$：**$y$ 切片**（$x = 0$ のときの値）

$a > 0$ なら右上がり、$a < 0$ なら右下がり、$a = 0$ なら水平線（定数関数）。

---

## 直線の方程式の書き方

| 与えられた情報 | 式 |
|-------------|-----|
| 傾き $a$ と $y$ 切片 $b$ | $y = ax + b$ |
| 点 $(x_1, y_1)$ と傾き $a$ | $y - y_1 = a(x - x_1)$ |
| 2点 $(x_1, y_1)$、$(x_2, y_2)$ | 傾き $a = \dfrac{y_2-y_1}{x_2-x_1}$ を求めてから上へ |

**例題**：点 $(1, 2)$ と $(3, 6)$ を通る直線を求めます。

傾き $a = \dfrac{6-2}{3-1} = 2$、$y - 2 = 2(x-1)$ より $y = 2x$。

---

## 連立方程式と交点

2つの一次方程式を同時に満たす $(x, y)$ が2直線の交点です。

**例**：$\begin{cases}y = 2x + 1 \\ y = -x + 4\end{cases}$

$2x + 1 = -x + 4 \Rightarrow x = 1$、$y = 3$。交点 $(1, 3)$。

---

## 傾きと変化率

一次関数では傾き $a$ が「$x$ の変化量あたりの $y$ の変化量」を表します。これは後で学ぶ微分の先取りです。一次関数の場合、「瞬間の変化率」はどこでも一定で、常に $a$ です。

---

## 関連ページ

- [一次関数（入門）](introduction.md)
- [二次関数（標準）](../quadratic/standard.md)
- [微分（標準）](../../analysis/derivatives/standard.md)
