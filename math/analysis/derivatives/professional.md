---
title: 微分
description: "多変数微分・フレシェ微分・微分形式"
goal: "微分を厳密に定義し、主要な定理を証明できるようになる"
tags: [math,analysis,derivatives]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 解析
    path: /math/analysis/index.md
  - title: 微分
    path: /math/analysis/derivatives/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 微分
    path: /math/analysis/derivatives/introduction.md
  - title: 行列
    path: /math/linear-algebra/matrices/introduction.md
  - title: ベクトル
    path: /math/linear-algebra/vectors/introduction.md
---

## 微分可能性と連続性

**定義**：$f: \mathbb{R} \to \mathbb{R}$ が $x_0$ で微分可能とは、

$$f'(x_0) = \lim_{h \to 0} \frac{f(x_0+h) - f(x_0)}{h}$$

が存在することです。

**定理**：微分可能 $\Rightarrow$ 連続。逆は成り立ちません。

**反例（ワイエルシュトラス関数）**：$f(x) = \sum_{n=0}^{\infty} a^n \cos(b^n \pi x)$（$0 < a < 1$、$b$ 奇数、$ab > 1 + 3\pi/2$）は至る所連続だが至る所微分不可能です。

**参考文献**：Weierstrass, K. (1872). Über continuirliche Functionen eines reellen Arguments. *Monatsber. Königl. Preuss. Akad. Wiss. Berlin*, 71–74.

---

## 多変数微分

$f: \mathbb{R}^n \to \mathbb{R}$ の**偏微分**：

$$\frac{\partial f}{\partial x_i} = \lim_{h\to 0} \frac{f(x + he_i) - f(x)}{h}$$

**全微分可能**とは、線形写像 $A$ が存在して $f(x+h) = f(x) + Ah + o(\|h\|)$ が成り立つこと。

**全微分**：$df = \sum_i \dfrac{\partial f}{\partial x_i}dx_i$

$f: \mathbb{R}^n \to \mathbb{R}^m$ の微分は **ヤコビ行列** $Jf = \left(\dfrac{\partial f_i}{\partial x_j}\right)$ で表されます。

**連鎖律**：$J(g \circ f) = Jg \cdot Jf$

---

## フレシェ微分

バナッハ空間 $X, Y$ 上の写像 $F: X \to Y$ が $x_0$ で**フレシェ微分可能**とは、有界線形写像 $A: X \to Y$ が存在して、

$$\lim_{\|h\|\to 0} \frac{\|F(x_0+h) - F(x_0) - Ah\|}{\|h\|} = 0$$

が成り立つことです。$A$ を $DF(x_0)$ と書き、フレシェ微分といいます。

---

## 微分形式

$k$-形式：$\omega = \sum_{i_1 < \cdots < i_k} a_{i_1\ldots i_k}\,dx_{i_1} \wedge \cdots \wedge dx_{i_k}$

外微分 $d\omega$ は $(k+1)$-形式。**ストークスの定理**：$\displaystyle\int_{\partial M}\omega = \int_M d\omega$

これはグリーンの定理・発散定理・古典的ストークスの定理を統一します。

**参考文献**：Spivak, M. (1965). *Calculus on Manifolds*. Benjamin.

---

## 関連ページ

- [微分（標準）](standard.md)
- [積分（専門）](../integrals/professional.md)
