---
title: 不等号・不等式
description: "凸不等式・関数不等式・最適化理論との接続"
tags: [math,math-language,inequalities]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 数学の言語
    url: /math/math-language/index.html
  - title: 不等号・不等式
    url: /math/math-language/inequalities/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: 不等号・不等式
    url: /math/math-language/inequalities/introduction
  - title: 微分
    url: /math/functions/derivatives/introduction
  - title: 積分
    url: /math/functions/integrals/introduction
---


> この記事は [標準](standard.md) の続きです。先に標準を読むことを推奨します。

凸関数・イェンセン不等式・最適化理論との接続を扱います。

## このページで扱うこと
- 凸関数とイェンセン不等式
- ヘルダー不等式・ミンコフスキー不等式
- KKT条件と最適化

---

## 凸関数

$f$ が凸 $\iff$ $f(\lambda x + (1-\lambda)y) \leq \lambda f(x) + (1-\lambda)f(y)$

$f''(x) \geq 0$ ならば凸（2階微分による判定）。

---

## イェンセン不等式

$f$ が凸, 確率変数 $X$ について:

$$f(E[X]) \leq E[f(X)]$$

---

## ヘルダー不等式

$\frac{1}{p} + \frac{1}{q} = 1$（$p,q > 1$）のとき:

$$\sum_i |a_i b_i| \leq \left(\sum_i |a_i|^p\right)^{1/p}\left(\sum_i |b_i|^q\right)^{1/q}$$

コーシー・シュワルツ不等式は $p = q = 2$ の特殊ケース。

---

## KKT条件

制約付き最適化 $\min f(x)$ s.t. $g_i(x) \leq 0$ の最適解での必要条件（ラグランジュ乗数法の拡張）。

---

## 関連ページ

- [不等号・不等式](introduction.md)
- [積分（専門）](../../functions/integrals/professional.md)
- [確率（専門）](../../statistics/probability/professional.md)
