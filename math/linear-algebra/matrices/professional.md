---
title: 行列
description: "スペクトル定理・特異値分解・リー群"
goal: "スペクトル定理・SVDの内容を述べ、行列のなすリー群・リー代数の基本的な構造を説明できるようになる"
tags: [math,linear-algebra,matrices]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 線形代数
    path: /math/linear-algebra/index.md
  - title: 行列
    path: /math/linear-algebra/matrices/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 行列（標準）
    path: /math/linear-algebra/matrices/standard.md
  - title: ベクトル（専門）
    path: /math/linear-algebra/vectors/professional.md
---

## スペクトル定理

**定理**：実対称行列（$A = A^T$）は直交行列 $Q$（$Q^TQ = I$）によって対角化できます。

$$A = Q \Lambda Q^T$$

（$\Lambda$ は固有値を対角成分に持つ対角行列）

すべての固有値は実数であり、異なる固有値に対応する固有ベクトルは直交します。

**証明の方針**：固有多項式が $\mathbb{R}$ 上で（重複も込めて）$n$ 個の根を持つことをスペクトル射影を使って示します。

**参考文献**：Axler, S. (2015). *Linear Algebra Done Right* (3rd ed.). Springer.

---

## 特異値分解（SVD）

任意の $m \times n$ 行列 $A$ は：

$$A = U \Sigma V^T$$

と分解できます。ここで $U$（$m \times m$ 直交）、$\Sigma$（$m \times n$ 対角・非負）、$V$（$n \times n$ 直交）。

$\Sigma$ の対角成分 $\sigma_1 \geq \sigma_2 \geq \cdots \geq 0$ を**特異値**といいます。

**応用**：
- データ圧縮：上位 $k$ 個の特異値のみ保持（ランク $k$ 近似）
- 疑似逆行列：$A^+ = V \Sigma^+ U^T$（$\sigma_i \neq 0$ のとき $1/\sigma_i$、他は $0$）
- 推薦システム・自然言語処理（潜在意味解析）

---

## リー群とリー代数

行列のなす群の例：

| 群 | 定義 | 次元 |
|----|------|------|
| $GL(n, \mathbb{R})$ | 可逆実行列 | $n^2$ |
| $O(n)$ | 直交行列（$A^TA = I$） | $n(n-1)/2$ |
| $SO(n)$ | $\det = 1$ の直交行列 | $n(n-1)/2$ |
| $SL(n, \mathbb{R})$ | $\det = 1$ の実行列 | $n^2-1$ |

これらは多様体の構造も持つ**リー群**です。

単位元 $I$ での接空間が**リー代数** $\mathfrak{g}$ で、交換子積 $[A, B] = AB - BA$ が演算になります。

**指数写像** $\exp: \mathfrak{g} \to G$ はリー代数からリー群への自然な写像で、$\exp(A) = \sum_{n=0}^\infty \frac{A^n}{n!}$ で与えられます（行列指数関数）。

**参考文献**：Hall, B. C. (2015). *Lie Groups, Lie Algebras, and Representations* (2nd ed.). Springer.

---

## 関連ページ

- [行列（標準）](standard.md)
- [ベクトル（専門）](../vectors/professional.md)
