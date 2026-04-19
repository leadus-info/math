---
title: 三角関数
description: "フーリエ級数・フーリエ変換・球面調和関数"
goal: "三角関数を厳密に定義し、主要な定理を証明できるようになる"
tags: [math,functions,trigonometric]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/analysis/index.md
  - title: 三角関数
    path: /math/geometry/trigonometry/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 三角関数
    path: /math/geometry/trigonometry/introduction.md
  - title: 積分（専門）
    path: /math/analysis/integrals/professional.md
  - title: 複素関数
    path: /math/analysis/complex-analysis/introduction.md
---

## フーリエ級数

周期 $2\pi$ の関数 $f \in L^2([-\pi, \pi])$ を三角関数系で展開：

$$f(x) = \frac{a_0}{2} + \sum_{n=1}^\infty (a_n\cos nx + b_n\sin nx)$$

フーリエ係数：

$$a_n = \frac{1}{\pi}\int_{-\pi}^{\pi} f(x)\cos nx\,dx, \quad b_n = \frac{1}{\pi}\int_{-\pi}^{\pi} f(x)\sin nx\,dx$$

三角関数系 $\{1, \cos x, \sin x, \cos 2x, \sin 2x, \ldots\}$ は $L^2([-\pi,\pi])$ の完全正規直交系です。

---

## フーリエ変換

$$\hat{f}(\xi) = \int_{-\infty}^\infty f(x)e^{-2\pi i x\xi}\,dx$$

逆変換：$f(x) = \displaystyle\int_{-\infty}^\infty \hat{f}(\xi)e^{2\pi i x\xi}\,d\xi$

**畳み込み定理**：$\widehat{f * g} = \hat{f} \cdot \hat{g}$

**パーセバルの等式**：$\|f\|_{L^2} = \|\hat{f}\|_{L^2}$

---

## 球面調和関数

球面 $S^2$ 上のラプラス方程式 $\Delta u = 0$ の固有関数 $Y_l^m(\theta, \varphi)$（$l = 0, 1, 2, \ldots$、$|m| \leq l$）。量子力学での角運動量固有関数、地球物理学での重力場展開に使われます。

---

## 参考文献

Stein, E. M. & Shakarchi, R. (2003). *Fourier Analysis: An Introduction*. Princeton University Press.

---

## 関連ページ

- [三角関数（標準）](standard.md)
- [複素関数（専門）](../../analysis/complex-analysis/professional.md)
