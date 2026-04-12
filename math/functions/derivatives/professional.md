---
title: 微分
description: "多変数微分・フレシェ微分・微分形式"
tags: [math,operations,derivatives]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数の操作
    path: /math/functions/index.md
  - title: 微分
    path: /math/functions/derivatives/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 微分
    path: /math/functions/derivatives/introduction.md
  - title: 行列
    path: /math/linear-algebra/matrices/introduction.md
  - title: ベクトル
    path: /math/linear-algebra/vectors/introduction.md
---

## 偏微分と全微分

$f: \mathbb{R}^n \to \mathbb{R}$ に対して:

$$\frac{\partial f}{\partial x_i} = \lim_{h\to 0}\frac{f(x + he_i) - f(x)}{h}$$

**全微分**: $df = \sum_i \frac{\partial f}{\partial x_i}dx_i$

---

## ヤコビ行列

$f: \mathbb{R}^n \to \mathbb{R}^m$ の微分は $m \times n$ 行列:

$$Jf = \begin{pmatrix} \partial f_i / \partial x_j \end{pmatrix}$$

**連鎖律**: $J(g \circ f) = Jg \cdot Jf$

---

## フレシェ微分

バナッハ空間 $X, Y$ 上の写像 $F: X \to Y$ が $x_0$ でフレシェ微分可能とは、線形写像 $A: X \to Y$ が存在して:

$$\lim_{\|h\| \to 0}\frac{\|F(x_0 + h) - F(x_0) - Ah\|}{\|h\|} = 0$$

---

## 微分形式

$k$-形式: $\omega = \sum_{i_1 < \cdots < i_k} a_{i_1\ldots i_k}\,dx_{i_1} \wedge \cdots \wedge dx_{i_k}$

**外微分**: $d\omega$（$(k+1)$-形式）

ストークスの定理: $\int_{\partial M}\omega = \int_M d\omega$

---

## 関連ページ

- [微分](introduction.md)
- [積分（専門）](../integrals/professional.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
- [複素関数](introduction.md)
