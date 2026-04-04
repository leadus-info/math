---
title: 極限
description: "ε-δ論法・一様収束・位相的極限"
tags: [math,operations,limits]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 関数の操作
    path: /math/functions/index.html
  - title: 極限
    path: /math/functions/limits/professional.html
levels:
  - level: 入門
    path: introduction.html
  - level: 標準
    path: standard.html
  - level: 専門
level: 専門
requires:
  - title: 極限
    path: /math/functions/limits/introduction
  - title: 集合（専門）
    path: ../../../math-language/sets/professional.md
  - title: 小数（専門）
    path: ../../../numbers/decimals/professional.md
---




> この記事は [標準](standard.md) の続きです。先に標準を読むことを推奨します。

$\varepsilon$-$\delta$ 論法・一様収束・位相的な極限の定式化を扱います。

## このページで扱うこと
- $\varepsilon$-$\delta$ による厳密な定義と証明例
- 点収束と一様収束の違い
- 位相空間における極限

---

## $\varepsilon$-$\delta$ 定義

$$\lim_{x \to a}f(x) = L \iff \forall \varepsilon > 0,\ \exists \delta > 0 \text{ s.t. } 0 < |x-a| < \delta \Rightarrow |f(x)-L| < \varepsilon$$

**証明例**: $\lim_{x \to 3}(2x-1) = 5$

$|2x-1-5| = 2|x-3| < \varepsilon$ ← $|x-3| < \varepsilon/2$ を選べばよいので $\delta = \varepsilon/2$。

---

## 点収束と一様収束

関数列 $\{f_n\}$ について:

**点収束**: 各 $x$ で $\lim_{n\to\infty}f_n(x) = f(x)$

**一様収束**: $\sup_x |f_n(x) - f(x)| \to 0$

一様収束は連続性・積分・微分の交換を正当化します。

$$f_n(x) = x^n \text{ on } [0,1] \text{ は点収束するが一様収束しない}$$

---

## コーシーの収束判定

数列 $\{a_n\}$ が収束する $\iff$ コーシー列である（$\mathbb{R}$ の完備性）:

$$\forall \varepsilon > 0,\ \exists N \text{ s.t. } m,n > N \Rightarrow |a_m - a_n| < \varepsilon$$

---

## 位相空間における極限

位相空間 $(X, \mathcal{T})$ での極限: 任意の開近傍 $U \ni L$ に対し、ある $\delta$ 以内の $x$ で $f(x) \in U$。

---

## 関連ページ

- [極限](introduction.md)
- [微分（専門）](../derivatives/professional.md)
- [小数（専門）](../../numbers/decimals/professional.md)
