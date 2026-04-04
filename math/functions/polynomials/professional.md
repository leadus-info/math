---
title: 多項式
description: "多項式環・代数幾何の入口・シューア多項式"
tags: [math,functions,polynomials]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 関数
    url: /math/functions/index.html
  - title: 多項式
    url: /math/functions/polynomials/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: 多項式
    url: /math/functions/polynomials/introduction
  - title: 代数（専門）
    url: ../../math-language/algebra/professional.md
  - title: 行列（専門）
    url: ../../linear-algebra/matrices/professional.md
---


> この記事は [標準](standard.md) の続きです。先に標準を読むことを推奨します。

多変数多項式・対称多項式・代数幾何の基礎を扱います。

## このページで扱うこと
- 多変数多項式と斉次多項式
- 対称多項式とシューア多項式
- 代数的多様体の入口

---

## 対称多項式

変数の置換で不変な多項式。基本対称多項式:

$$e_1 = \sum x_i,\quad e_2 = \sum_{i<j}x_ix_j,\quad e_k = \sum_{i_1<\cdots<i_k}x_{i_1}\cdots x_{i_k}$$

**基本定理**: 任意の対称多項式は $e_1, \ldots, e_n$ の多項式で一意に表せる。

---

## 代数的多様体

多項式の零点集合:

$$V(f_1, \ldots, f_k) = \{x \in \mathbb{A}^n : f_1(x) = \cdots = f_k(x) = 0\}$$

ヒルベルトの零点定理（ヌルシュテレンザッツ）と代数幾何学の出発点。

---

## 関連ページ

- [多項式](introduction.md)
- [等号・等式（専門）](../../math-language/equations/professional.md)
- [複素数（専門）](../../numbers/complex-numbers/professional.md)
