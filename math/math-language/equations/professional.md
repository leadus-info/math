---
title: 等号・等式
description: "方程式論・代数方程式の根の構造"
tags: [math,math-language,equations]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 数学の言語
    path: /math/math-language/index.html
  - title: 等号・等式
    path: /math/math-language/equations/professional.html
levels:
  - level: 入門
    path: introduction.html
  - level: 標準
    path: standard.html
  - level: 専門
level: 専門
requires:
  - title: 等号・等式
    path: /math/math-language/equations/introduction.html
  - title: 多項式（専門）
    path: ../../functions/polynomials/professional.md
  - title: 複素数
    path: /math/numbers/complex-numbers/introduction.html
---


## このページで扱うこと

代数方程式の根の理論とガロア理論の入口を扱います。

- 代数方程式の根と係数の関係（ヴィエタの公式）
- 根の存在（代数学の基本定理）
- ガロア理論の概観

---

## ヴィエタの公式

$n$ 次方程式 $a_n x^n + \cdots + a_0 = 0$ の根 $\alpha_1, \ldots, \alpha_n$ について:

$$\sum_i \alpha_i = -\frac{a_{n-1}}{a_n},\quad \prod_i \alpha_i = (-1)^n \frac{a_0}{a_n}$$

---

## 代数学の基本定理

複素係数 $n$ 次多項式は $\mathbb{C}$ 内に（重複を込めて）ちょうど $n$ 個の根を持つ。

**証明の概略**: $|f(z)| \to \infty$ ($|z| \to \infty$) と最小値定理から導く。

---

## 5次方程式の非可解性

4次以下の代数方程式は根号で解けますが、一般の5次方程式は**根号では解けない**（アーベル・ルフィニの定理）。

この理由を体の自己同型群（ガロア群）の言葉で説明するのが**ガロア理論**です。

---

## 関連ページ

- [等号・等式](introduction.md)
- [多項式（専門）](../../functions/polynomials/professional.md)
- [複素数（専門）](../../numbers/complex-numbers/professional.md)
