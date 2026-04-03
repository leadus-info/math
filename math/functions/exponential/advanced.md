---
title: 指数関数（発展）
description: "倍々で増える関数（発展）"
difficulty: 3
tags: [math,functions,exponential,advanced]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 指数関数（発展）
    href: /math/functions/exponential/advanced.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
  - text: 専門
    href: professional.html
---







# 指数関数
1、2、4、8、16……倍々で増えていく変化を表す関数です。

## このページで扱うこと
- 指数関数の定義とグラフ
- ネイピア数 $e$ の意味
- 指数方程式の解き方

## 前提知識
- [四則演算](professional.md) — べき乗
- [一次関数](professional.md) — 関数の基本

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
