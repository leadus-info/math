---
title: 三角関数（専門）
description: "フーリエ級数・フーリエ変換・球面調和関数"
difficulty: 6
tags: [math,functions,trigonometric,professional]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 三角関数（専門）
    href: /math/functions/trigonometric/professional.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
    href: advanced.html
  - text: 専門
---








# 三角関数（発展）
フーリエ解析・変換・球面調和関数を扱います。

## このページで扱うこと
- フーリエ級数展開
- フーリエ変換とその性質
- 球面調和関数の概要

## 前提知識
- [三角関数](../trigonometric/standard.md)
- [積分（専門）](../calculus/integrals/professional.md)
- [複素関数](../calculus/complex-functions/standard.md)

---

## フーリエ級数

周期 $2\pi$ の関数を三角関数の無限和で表します。

$$f(x) = \frac{a_0}{2} + \sum_{n=1}^{\infty}(a_n \cos nx + b_n \sin nx)$$

$$a_n = \frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\cos nx\,dx,\quad b_n = \frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\sin nx\,dx$$

---

## フーリエ変換

$$\hat{f}(\xi) = \int_{-\infty}^{\infty}f(x)e^{-2\pi i x\xi}\,dx$$

逆変換: $f(x) = \int_{-\infty}^{\infty}\hat{f}(\xi)e^{2\pi i x\xi}\,d\xi$

畳み込み定理: $\widehat{f*g} = \hat{f}\cdot\hat{g}$

---

## 球面調和関数

$S^2$ 上のラプラス方程式の固有関数 $Y_l^m(\theta, \varphi)$（量子力学・地球物理学で重要）。

---

## 関連ページ

- [三角関数](../trigonometric/standard.md)
- [複素関数](../calculus/complex-functions/standard.md)
- [積分（専門）](../calculus/integrals/professional.md)
