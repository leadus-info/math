---
title: 二次関数
description: "二次形式・固有値との接続・円錐曲線"
goal: "二次関数を厳密に定義し、主要な定理を証明できるようになる"
tags: [math,functions,quadratic]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/analysis/index.md
  - title: 二次関数
    path: /math/specific-functions/quadratic/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 二次関数
    path: /math/specific-functions/quadratic/introduction.md
  - title: 行列
    path: /math/linear-algebra/matrices/introduction.md
  - title: ベクトル
    path: /math/linear-algebra/vectors/introduction.md
---

## 二次形式

**定義**：$Q(\boldsymbol{x}) = \boldsymbol{x}^\top A\boldsymbol{x}$（$A$ は対称行列）を**二次形式**といいます。

$A$ の固有値の符号で分類：
- すべての固有値 $> 0$：**正定値**
- すべての固有値 $\geq 0$：**半正定値**
- 正・負両方の固有値：**不定値**

---

## ヘッセ行列と極値

$f: \mathbb{R}^n \to \mathbb{R}$ の二階偏微分からなる行列：

$$H_f = \left(\frac{\partial^2 f}{\partial x_i \partial x_j}\right)$$

$\nabla f = 0$ の点での $H_f$ の定値性で極値を判定：
- 正定値 → 極小
- 負定値 → 極大
- 不定値 → 鞍点

---

## 円錐曲線の分類

$$Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$$

判別式 $\Delta = B^2 - 4AC$ で分類：

| $\Delta < 0$ | 楕円（円を含む） |
| $\Delta = 0$ | 放物線 |
| $\Delta > 0$ | 双曲線 |

---

## 参考文献

Apostol, T. M. (1969). *Calculus* Vol. 2 (2nd ed.). Wiley.

---

## 関連ページ

- [二次関数（標準）](standard.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
