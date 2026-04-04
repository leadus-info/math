---
title: 二次関数
description: "二次形式・固有値との接続・円錐曲線"
tags: [math,functions,quadratic]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 二次関数
    href: /math/functions/quadratic/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: 二次関数
    url: \1/introduction.md
  - title: 行列
    url: \1/introduction.md
  - title: ベクトル
    url: \1/introduction.md
---









# 二次関数（発展）
二次形式・円錐曲線・行列の固有値との関係を扱います。

## このページで扱うこと
- 二次形式と正値性
- 円錐曲線（楕円・双曲線・放物線）の統一的な扱い
- 最適化との接続（ヘッセ行列）

---

## 二次形式

$$Q(\boldsymbol{x}) = \boldsymbol{x}^\top A \boldsymbol{x} = \sum_{i,j} a_{ij} x_i x_j$$

$A$ が対称行列のとき、固有値の符号が $Q$ の正値性を決定します。

---

## 円錐曲線

$$Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$$

判別式 $B^2 - 4AC$ の符号で分類:

| $B^2 - 4AC$ | 曲線 |
|-------------|------|
| $< 0$ | 楕円（円含む） |
| $= 0$ | 放物線 |
| $> 0$ | 双曲線 |

---

## ヘッセ行列と極値

$f: \mathbb{R}^n \to \mathbb{R}$ の極値判定:

$$H_f = \left(\frac{\partial^2 f}{\partial x_i \partial x_j}\right)$$

$H_f$ が正定値 → 極小、負定値 → 極大

---

## 関連ページ

- [二次関数](introduction.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
- [多項式（専門）](../polynomials/professional.md)
