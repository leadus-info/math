---
title: 指数関数
description: "倍々で増える関数"
tags: [math,functions,exponential]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 関数
    url: /math/functions/index.html
  - title: 指数関数
    url: /math/functions/exponential/standard.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
  - level: professional
    url: professional.html
level: standard
requires:
  - title: 四則演算
    url: professional.md
  - title: 一次関数
    url: professional.md
---



1、2、4、8、16……倍々で増えていく変化を表す関数です。

## このページで扱うこと
- 指数関数の定義とグラフ
- ネイピア数 $e$ の意味
- 指数方程式の解き方

---

## 定義

$$f(x) = a^x \quad (a > 0,\ a \neq 1)$$

---

## グラフの特徴

| | $a > 1$ | $0 < a < 1$ |
|-|---------|-------------|
| 形 | 右上がり | 右下がり |
| $y$ 切片 | $(0,\ 1)$ | $(0,\ 1)$ |
| 漸近線 | $y = 0$ | $y = 0$ |

$y$ 切片はどんな底でも $(0,\ 1)$ です（$a^0 = 1$ のため）。

---

## 指数法則

$$a^m \times a^n = a^{m+n}, \qquad (a^m)^n = a^{mn}$$

---

## ネイピア数 $e$

$$e \approx 2.718\ldots$$

微分しても形が変わらない特別な底です：

$$\frac{d}{dx} e^x = e^x$$

---

## 指数方程式

底を揃えて解きます。

$$2^x = 8 = 2^3 \implies x = 3$$

底が揃わないときは対数を使います。

---

## 関連ページ

- [対数関数](professional.md)
- [微分](professional.md)
- [指数関数（専門）](professional.md)
