---
title: 一次関数
description: "直線のグラフと傾き"
tags: [math,functions,linear]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/functions/index.md
  - title: 一次関数
    path: /math/functions/linear/standard.md
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
    path: /math/math-language/equations/introduction.md
---

## 一次関数の定義

$x$ が 1 増えるたびに $y$ が一定量だけ変化する関数が**一次関数**です。

$$f(x) = ax + b$$

- $a$：**傾き**（$x$ が 1 増えると $y$ が $a$ 増える）
- $b$：**$y$ 切片**（$x = 0$ のときの $y$ の値）

$a = 0$ のとき定数関数（水平線）、$b = 0$ のとき原点を通る直線です。

---

## グラフと傾きの意味

グラフは必ず直線になります。

- $a > 0$：右上がり（$x$ が増えると $y$ も増える）
- $a < 0$：右下がり（$x$ が増えると $y$ は減る）
- $|a|$ が大きいほど急な傾き

**傾きは変化率**：$x$ が $\Delta x$ 変化したとき $y$ は $a \cdot \Delta x$ 変化します。

---

## 直線の方程式のさまざまな表し方

| 場面 | 式 |
|------|-----|
| 傾きと $y$ 切片がわかる | $y = ax + b$ |
| 1点 $(x_1, y_1)$ と傾き $a$ がわかる | $y - y_1 = a(x - x_1)$ |
| 2点 $(x_1, y_1)$、$(x_2, y_2)$ がわかる | 傾き $a = \frac{y_2-y_1}{x_2-x_1}$ を計算してから点傾き形式へ |

**例題**：点 $(2, 5)$ と $(4, 9)$ を通る直線：\
傾き $a = \frac{9-5}{4-2} = 2$\
$y - 5 = 2(x - 2)$ より $y = 2x + 1$

---

## 2直線の交点（連立方程式）

$$\begin{cases}y = 2x + 1 \\ y = -x + 4\end{cases}$$

辺々引くと：$0 = 3x - 3$ より $x = 1$、$y = 3$。\
交点 $(1, 3)$ で2直線が交わります。

**交点がない場合**：2直線の傾きが同じで切片が異なるとき（平行）。\
**交点が無数にある場合**：2直線の式が完全に同じとき（同一直線）。

---

## 関連ページ

- [二次関数](../quadratic/introduction.md)
- [直線](../../geometry/line/introduction.md)
- [微分](../derivatives/introduction.md) — 傾きの一般化
