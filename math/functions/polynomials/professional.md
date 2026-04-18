---
title: 多項式
description: "多項式環・代数幾何の入口・シューア多項式"
goal: "多項式を厳密に定義し、主要な定理を証明できるようになる"
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

## 多項式環 $F[x]$

体 $F$ 上の多項式全体 $F[x]$ は**主イデアル整域（PID）**です：すべてのイデアルが1元で生成されます。

$$F[x]/(f(x)) \quad \text{（$f$ が既約多項式のとき体の拡大）}$$

**例**：$\mathbb{R}[x]/(x^2+1) \cong \mathbb{C}$（実係数多項式を $x^2+1$ で割ると複素数体が現れる）

---

## 対称多項式

変数の任意の置換で不変な多項式が**対称多項式**。基本対称多項式：

$$e_1 = \sum x_i, \quad e_2 = \sum_{i<j} x_i x_j, \quad e_k = \sum_{i_1 < \cdots < i_k} x_{i_1}\cdots x_{i_k}$$

**定理**：任意の対称多項式は $e_1, \ldots, e_n$ の多項式として一意に書ける。

この定理は、方程式の根と係数の関係（ヴィエタの公式）の基礎になります。

---

## ガロア理論の概要

**定理（アーベル・ルフィニ）**：一般の5次以上の代数方程式は根号では解けない。

4次以下は解けます（2次の解の公式、3次・4次のカルダノ公式）。

5次以上が「解けない」理由をガロア群の言葉で説明するのが**ガロア理論**です。方程式 $f(x) = 0$ に対し、$f$ の分解体の自己同型群（ガロア群）が可解群でないとき根号では解けません。

---

## 代数的多様体の入口

多項式の共通零点集合：

$$V(f_1, \ldots, f_k) = \{x \in \mathbb{A}^n : f_1(x) = \cdots = f_k(x) = 0\}$$

**ヒルベルトの零点定理**：代数的閉体上でイデアルと多様体が対応します。

**参考文献**：Lang, S. (2002). *Algebra* (3rd ed.). Springer.

---

## 関連ページ

- [多項式（標準）](standard.md)
- [等号・等式（専門）](../../math-language/equations/professional.md)
