---
title: 指数関数
description: "倍々で増える関数"
tags: [math,functions,exponential]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/functions/index.md
  - title: 指数関数
    path: /math/functions/exponential/standard.md
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
  - title: 一次関数
    path: /math/functions/linear/introduction.md
---

## 定義

底 $a > 0$、$a \neq 1$ の**指数関数**：

$$f(x) = a^x$$

$x$ が整数のとき $a^n = a \times a \times \cdots \times a$（$n$ 回掛ける）が原点的な意味ですが、\
有理数・実数へと自然に拡張されます。

---

## グラフの特徴

| | $a > 1$ | $0 < a < 1$ |
|--|---------|-------------|
| 形 | 右上がり（指数的増加） | 右下がり（指数的減衰） |
| $y$ 切片 | $(0, 1)$ | $(0, 1)$ |
| 漸近線 | $y = 0$（$x \to -\infty$） | $y = 0$（$x \to +\infty$） |

**共通の性質**：
- すべての $x$ で $a^x > 0$（決して負にならない）
- $a^0 = 1$（底が何であれ $y$ 切片は 1）

---

## 指数法則

$$a^m \times a^n = a^{m+n}$$
$$(a^m)^n = a^{mn}$$
$$a^{-n} = \frac{1}{a^n}$$
$$a^{1/n} = \sqrt[n]{a}$$

**例**：$2^3 \times 2^4 = 2^7 = 128$、$(2^3)^2 = 2^6 = 64$

---

## ネイピア数 $e$

$$e = \lim_{n\to\infty}\left(1 + \frac{1}{n}\right)^n \approx 2.71828\ldots$$

$e$ は**微分しても変わらない**という特別な性質を持ちます：

$$\frac{d}{dx} e^x = e^x$$

これが自然現象（成長・減衰）の数理モデルで $e$ が頻繁に登場する理由です。

---

## 指数方程式と不等式

**底を揃えて解く**：

$$4^x = 8 \implies (2^2)^x = 2^3 \implies 2x = 3 \implies x = \frac{3}{2}$$

**底が $1$ より大きいとき不等号の向きはそのまま**：

$$2^x > 2^3 \iff x > 3$$

**底が $0$ と $1$ の間のとき不等号の向きが逆**：

$$\left(\frac{1}{2}\right)^x > \left(\frac{1}{2}\right)^3 \iff x < 3$$

---

## 関連ページ

- [対数関数](../logarithmic/introduction.md)
- [微分](../derivatives/introduction.md)
