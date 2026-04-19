---
title: 不等号・不等式
description: "凸関数・重要不等式・最適化"
goal: "凸関数の定義とイェンセン不等式を理解し、ヘルダー不等式・コーシー＝シュワルツ不等式を証明できるようになる"
tags: [math,algebra,inequalities]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 代数
    path: /math/algebra/index.md
  - title: 不等号・不等式
    path: /math/algebra/inequalities/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 不等号・不等式（標準）
    path: /math/algebra/inequalities/standard.md
  - title: 微分（標準）
    path: /math/analysis/derivatives/standard.md
  - title: 積分（標準）
    path: /math/analysis/integrals/standard.md
---

## 凸関数

**定義**：$f: I \to \mathbb{R}$（$I$ は区間）が**凸**（convex）であるとは、任意の $x, y \in I$ と $\lambda \in [0,1]$ に対して

$$f(\lambda x + (1-\lambda)y) \leq \lambda f(x) + (1-\lambda)f(y)$$

が成り立つことです。幾何学的には「弦が曲線の上にある」ことを意味します。

**定理**：$f$ が $I$ 上で $2$ 回微分可能なとき、$f''(x) \geq 0$ ならば $f$ は凸です。

**例**：$f(x) = x^2$ は $f''(x) = 2 > 0$ なので凸。$f(x) = \ln x$ は $f''(x) = -1/x^2 < 0$ なので凹（concave）。

---

## イェンセン不等式

**定理**：$f$ が凸関数のとき、確率変数 $X$ に対して

$$f(E[X]) \leq E[f(X)]$$

離散版：$p_1 + \cdots + p_n = 1$、$p_i \geq 0$ のとき

$$f\left(\sum_{i=1}^n p_i x_i\right) \leq \sum_{i=1}^n p_i f(x_i)$$

AM-GM 不等式（不等号・不等式（標準）参照）は $f(x) = -\ln x$ がの凸性から導かれます。

---

## コーシー＝シュワルツ不等式

$$\left(\sum_{i=1}^n a_i b_i\right)^2 \leq \left(\sum_{i=1}^n a_i^2\right)\left(\sum_{i=1}^n b_i^2\right)$$

**証明**：任意の実数 $t$ に対して $\sum_i (a_i t + b_i)^2 \geq 0$ を展開すると $t$ の二次式 $At^2 + 2Bt + C \geq 0$（$A = \sum a_i^2$、$B = \sum a_i b_i$、$C = \sum b_i^2$）。判別式 $B^2 - AC \leq 0$。$\square$

---

## ヘルダー不等式

$\frac{1}{p} + \frac{1}{q} = 1$（$p, q > 1$）のとき、

$$\sum_{i=1}^n |a_i b_i| \leq \left(\sum_{i=1}^n |a_i|^p\right)^{1/p}\left(\sum_{i=1}^n |b_i|^q\right)^{1/q}$$

コーシー＝シュワルツ不等式は $p = q = 2$ の特殊ケースです。

証明は Young の不等式 $ab \leq \frac{a^p}{p} + \frac{b^q}{q}$（$a, b \geq 0$）から導きます。

**参考文献**：Hardy, G. H., Littlewood, J. E., & Pólya, G. (1952). *Inequalities* (2nd ed.). Cambridge University Press.

---

## 関連ページ

- [不等号・不等式（標準）](standard.md)
- [積分（専門）](../../analysis/integrals/professional.md)
- [確率（専門）](../../probability/probability/professional.md)
