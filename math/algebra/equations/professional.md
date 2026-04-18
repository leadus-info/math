---
title: 等号・等式
description: "方程式論・代数方程式の根の構造"
goal: "ヴィエタの公式を導出でき、代数学の基本定理と5次方程式の非可解性の意味を説明できるようになる"
tags: [math,math-language,equations]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数学の言語
    path: /math/algebra/index.md
  - title: 等号・等式
    path: /math/algebra/equations/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 等号・等式（標準）
    path: /math/algebra/equations/standard.md
  - title: 多項式（専門）
    path: /math/algebra/polynomials/professional.md
  - title: 複素数（専門）
    path: /math/numbers/complex-numbers/professional.md
---

## ヴィエタの公式

$n$ 次方程式 $a_n x^n + a_{n-1}x^{n-1} + \cdots + a_0 = 0$ の根を $\alpha_1, \ldots, \alpha_n$ とすると、根と係数の間に以下の関係が成り立ちます。

$$\sum_{i=1}^{n} \alpha_i = -\frac{a_{n-1}}{a_n}, \quad \sum_{i<j} \alpha_i \alpha_j = \frac{a_{n-2}}{a_n}, \quad \ldots, \quad \prod_{i=1}^{n} \alpha_i = (-1)^n \frac{a_0}{a_n}$$

一般に、根の $k$ 次基本対称式は $(-1)^k \frac{a_{n-k}}{a_n}$ に等しくなります。

これは $a_n(x - \alpha_1)(x - \alpha_2) \cdots (x - \alpha_n)$ を展開して係数を比較することで証明できます。

**例**（二次方程式）：$x^2 + bx + c = 0$ の2根 $\alpha, \beta$ に対して $\alpha + \beta = -b$、$\alpha\beta = c$。

---

## 代数学の基本定理との関係

複素数（専門）で述べた代数学の基本定理により、$n$ 次複素係数多項式は $\mathbb{C}$ 内に（重複を込めて）$n$ 個の根を持ちます。

$$p(z) = a_n(z - \alpha_1)(z - \alpha_2) \cdots (z - \alpha_n)$$

等号・等式（標準）で扱った二次方程式の判別式 $D < 0$ のケース（実数解なし）は、複素数の範囲では常に解を持つということです。

---

## 5次方程式の非可解性

等号・等式（標準）では二次方程式の解の公式を見ました。三次・四次方程式にも（より複雑ですが）根号による解の公式が存在します。

しかし、一般の5次以上の方程式は根号だけでは解けません。

**定理（アーベル・ルフィニ）**：一般の $n \geq 5$ 次方程式に対して、係数の四則演算と根号のみで表せる解の公式は存在しない。

この理由を体の自己同型群（**ガロア群**）の言葉で説明するのがガロア理論です。方程式のガロア群が可解群であることと、方程式が根号で解けることが同値であり、$n \geq 5$ の一般の場合は対称群 $S_n$ が可解群でないことから従います。

**参考文献**：Stewart, I. (2015). *Galois Theory* (4th ed.). CRC Press.

---

## 関連ページ

- [等号・等式（標準）](standard.md)
- [複素数（専門）](../../numbers/complex-numbers/professional.md)
- [多項式（専門）](../polynomials/professional.md)
- [代数（専門）](../expressions/professional.md)