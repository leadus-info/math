---
title: 一次関数
description: "直線のグラフと傾き"
tags: [math,functions,linear]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 関数
    path: /math/functions/index.html
  - title: 一次関数
    path: /math/functions/linear/standard.html
levels:
  - level: 入門
    path: introduction.html
  - level: 標準
  - level: 専門
    path: professional.html
level: 標準
requires:
  - title: 四則演算
    path: professional.md
  - title: 等号・等式
    path: /math/math-language/equations/introduction
---




> この記事は [入門](introduction.md) の続きです。先に入門を読むことを推奨します。

$x$ が 1 増えるたびに $y$ が一定量だけ変化する——それが**一次関数**です。
グラフは必ず直線になります。

## このページで扱うこと
- 一次関数の定義（傾き・切片）
- グラフの読み方・書き方
- 連立方程式（2 直線の交点）

---

## 定義

$$f(x) = ax + b$$

- $a$：**傾き**（$x$ が 1 増えると $y$ が $a$ 増える）
- $b$：**$y$ 切片**（$x = 0$ のときの $y$ の値）

---

## グラフの特徴

- $a > 0$：右上がり
- $a < 0$：右下がり
- $a = 0$：水平線 $y = b$

---

## 直線の方程式

| 場面 | 式 |
|------|----|
| 傾きと $y$ 切片がわかる | $y = ax + b$ |
| 1 点と傾きがわかる | $y - y_1 = a(x - x_1)$ |
| 2 点がわかる | 傾きを計算してから上の式へ |

**傾きの計算**：

$$a = \frac{y_2 - y_1}{x_2 - x_1}$$

---

## 連立方程式（2 直線の交点）

$$\begin{cases}y = 2x + 1 \\ y = -x + 4\end{cases} \implies 2x + 1 = -x + 4 \implies x = 1,\ y = 3$$

---

## 関連ページ

- [二次関数](professional.md)
- [微分](professional.md) — 傾きの一般化
- [一次関数（専門）](professional.md) — アフィン写像・最小二乗法
