---
title: 極限
description: "ε-δ論法・一様収束・位相的極限"
goal: "極限を厳密に定義し、主要な定理を証明できるようになる"
tags: [math,analysis,limits]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 解析
    path: /math/analysis/index.md
  - title: 極限
    path: /math/analysis/limits/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 極限
    path: /math/analysis/limits/introduction.md
  - title: 集合（専門）
    path: ../../../math-language/sets/professional.md
  - title: 小数（専門）
    path: ../../../numbers/decimals/professional.md
---

## $\varepsilon$-$\delta$ による厳密な定義

**定義（関数の極限）**：$\displaystyle\lim_{x\to a} f(x) = L$ とは、

$$\forall \varepsilon > 0,\ \exists \delta > 0 \text{ s.t. } 0 < |x - a| < \delta \Rightarrow |f(x) - L| < \varepsilon$$

**証明例**：$\displaystyle\lim_{x\to 3}(2x - 1) = 5$

$|2x-1-5| = 2|x-3| < \varepsilon$ ← $|x-3| < \varepsilon/2$。よって $\delta = \varepsilon/2$。$\square$

---

## 数列の極限の厳密な定義

**定義**：$\displaystyle\lim_{n\to\infty} a_n = L$ とは、

$$\forall \varepsilon > 0,\ \exists N \in \mathbb{N} \text{ s.t. } n > N \Rightarrow |a_n - L| < \varepsilon$$

---

## 点収束と一様収束

関数列 $\{f_n\}$ の収束に2種類あります。

**点収束**：各 $x$ で $\lim_{n\to\infty} f_n(x) = f(x)$

**一様収束**：$\sup_x |f_n(x) - f(x)| \to 0$

一様収束は「収束のスピードが全点で均一」を意味します。一様収束のもとでは連続性・積分・微分の交換が正当化されます。

**例（点収束だが一様収束しない）**：$f_n(x) = x^n$ on $[0,1]$。各点では $0$ か $1$ に収束しますが、一様には収束しません。

---

## コーシーの収束判定

**定理（実数の完備性）**：$\{a_n\}$ が収束する $\iff$ コーシー列（$\forall \varepsilon > 0,\ \exists N,\ m,n > N \Rightarrow |a_m - a_n| < \varepsilon$）。

---

## 位相空間における極限

距離空間 $(X, d)$ での極限：$\displaystyle\lim_{x\to a} f(x) = L$ は、$f^{-1}(B_\varepsilon(L)) \supset B_\delta(a) \setminus \{a\}$ と定式化されます。これは位相空間に一般化できます。

**参考文献**：Rudin, W. (1976). *Principles of Mathematical Analysis* (3rd ed.). McGraw-Hill.

---

## 関連ページ

- [極限（標準）](standard.md)
- [微分（専門）](../derivatives/professional.md)
