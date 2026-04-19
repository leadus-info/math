---
title: 三角関数
description: "複素指数関数・フーリエ級数・調和解析"
goal: "オイラーの公式から三角関数を複素指数関数として定義し直し、フーリエ級数展開の理論的枠組みを説明できるようになる"
tags: [math,specific-functions,trigonometric]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 具体的な関数
    path: /math/specific-functions/index.md
  - title: 三角関数
    path: /math/specific-functions/trigonometric/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 三角関数（標準）
    path: /math/specific-functions/trigonometric/standard.md
  - title: 複素解析（標準）
    path: /math/analysis/complex-analysis/standard.md
  - title: 積分（専門）
    path: /math/analysis/integrals/professional.md
---

## 複素指数関数による定義

複素数 $z = x + iy$ に対して：

$$e^z = e^x(\cos y + i\sin y)$$

特に純虚数 $i\theta$ のとき（**オイラーの公式**）：

$$e^{i\theta} = \cos\theta + i\sin\theta$$

この公式から三角関数を複素指数関数で表せます：

$$\cos\theta = \frac{e^{i\theta} + e^{-i\theta}}{2}, \quad \sin\theta = \frac{e^{i\theta} - e^{-i\theta}}{2i}$$

これにより三角関数の諸公式が指数法則から自動的に従います。加法定理は $e^{i(\alpha+\beta)} = e^{i\alpha}e^{i\beta}$ を展開するだけです。

---

## フーリエ級数

周期 $2\pi$ の（可積分な）関数 $f$ を三角関数の無限和で表します：

$$f(x) = \frac{a_0}{2} + \sum_{n=1}^{\infty}(a_n\cos nx + b_n\sin nx)$$

**フーリエ係数**：

$$a_n = \frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\cos nx\,dx, \quad b_n = \frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\sin nx\,dx$$

複素表示（$c_n = \frac{a_n - ib_n}{2}$、$c_{-n} = \bar{c}_n$）：

$$f(x) = \sum_{n=-\infty}^{\infty} c_n e^{inx}, \quad c_n = \frac{1}{2\pi}\int_{-\pi}^{\pi}f(x)e^{-inx}\,dx$$

---

## 収束定理

$f \in L^2([-\pi, \pi])$ のとき、フーリエ級数は $L^2$ の意味で収束します（パーセバルの等式）：

$$\frac{1}{\pi}\int_{-\pi}^{\pi}|f(x)|^2\,dx = \frac{a_0^2}{2} + \sum_{n=1}^{\infty}(a_n^2 + b_n^2) = \sum_{n=-\infty}^{\infty}|c_n|^2$$

$\{e^{inx}\}_{n \in \mathbb{Z}}$ は $L^2([-\pi,\pi])$ の完全正規直交系（ヒルベルト空間の基底）をなします。

---

## フーリエ変換

非周期関数への拡張：

$$\hat{f}(\xi) = \int_{-\infty}^{\infty}f(x)e^{-2\pi ix\xi}\,dx$$

**逆変換**：$f(x) = \int_{-\infty}^{\infty}\hat{f}(\xi)e^{2\pi ix\xi}\,d\xi$

**パーセバルの定理**：$\|f\|_{L^2} = \|\hat{f}\|_{L^2}$（等長写像）

**畳み込み定理**：$\widehat{f * g} = \hat{f} \cdot \hat{g}$

フーリエ変換は信号処理・偏微分方程式・量子力学の基礎をなします。

**参考文献**：Stein, E. M. & Shakarchi, R. (2003). *Fourier Analysis: An Introduction*. Princeton University Press.

---

## 関連ページ

- [三角関数（標準）](standard.md)
- [複素解析（標準）](../../analysis/complex-analysis/standard.md)
- [積分（専門）](../../analysis/integrals/professional.md)
