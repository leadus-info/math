---
title: 多項式
description: "多項式環・代数幾何の入口・シューア多項式"
tags: [math,functions,polynomials]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/functions/index.md
  - title: 多項式
    path: /math/functions/polynomials/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 多項式
    path: /math/functions/polynomials/introduction.md
  - title: 代数（専門）
    path: ../../math-language/algebra/professional.md
  - title: 行列（専門）
    path: ../../linear-algebra/matrices/professional.md
---




## このページで扱うこと

多変数多項式・対称多項式・代数幾何の基礎を扱います。

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
