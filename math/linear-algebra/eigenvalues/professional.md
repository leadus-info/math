---
title: 固有値
description: "ジョルダン標準形・スペクトル定理・特異値分解"
goal: "ジョルダン標準形の構造を述べ、スペクトル定理の証明の流れを説明し、SVDを固有値分解と関連づけられるようになる"
tags: [math,linear-algebra,eigenvalues]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 線形代数
    path: /math/linear-algebra/index.md
  - title: 固有値
    path: /math/linear-algebra/eigenvalues/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 固有値（標準）
    path: /math/linear-algebra/eigenvalues/standard.md
  - title: 行列（専門）
    path: /math/linear-algebra/matrices/professional.md
  - title: 線形写像（専門）
    path: /math/linear-algebra/linear-maps/professional.md
---

## ジョルダン標準形

すべての正方行列（複素数上）は**ジョルダン標準形**に変換できます：

$$A = PJP^{-1}, \quad J = \mathrm{diag}(J_{n_1}(\lambda_1), \ldots, J_{n_k}(\lambda_k))$$

各**ジョルダンブロック**：

$$J_m(\lambda) = \begin{pmatrix}\lambda & 1 & & \\ & \lambda & \ddots & \\ & & \ddots & 1 \\ & & & \lambda\end{pmatrix} \in M_m(\mathbb{C})$$

$A$ が対角化可能 $\iff$ すべてのジョルダンブロックのサイズが $1 \times 1$。

ジョルダン標準形は一意（ブロックの順序を除く）で、行列の不変量を完全に記述します。

---

## スペクトル定理

**定理**：実対称行列 $A$（$A = A^\top$）は直交行列 $Q$（$Q^\top Q = I$）によって対角化できます：

$$A = Q\Lambda Q^\top$$

すべての固有値は実数であり、異なる固有値に対応する固有ベクトルは直交します。

**証明の概略**：(1) 固有多項式は $\mathbb{C}$ 上に根を持つ（代数学の基本定理）。(2) 実対称行列の固有値はすべて実数（$\lambda \boldsymbol{v} = A\boldsymbol{v}$ の両辺と $\bar{\boldsymbol{v}}$ の内積をとる）。(3) 異なる固有値の固有ベクトルは直交（$\lambda_1 \neq \lambda_2$、$A\boldsymbol{u} = \lambda_1\boldsymbol{u}$、$A\boldsymbol{v} = \lambda_2\boldsymbol{v}$ から $\boldsymbol{u}^\top A\boldsymbol{v}$ を2通り計算）。(4) 帰納法で基底を構成。$\square$

**参考文献**：Axler, S. (2015). *Linear Algebra Done Right* (3rd ed.). Springer.

---

## 特異値分解（SVD）の固有値との関係

任意の $m \times n$ 行列 $A$ に対して $A = U\Sigma V^\top$（行列（専門）参照）。

**特異値**（$\sigma_i = \Sigma_{ii}$）と固有値の関係：

- $\sigma_i^2$ は $A^\top A$（または $AA^\top$）の固有値
- $V$ の列は $A^\top A$ の固有ベクトル（右特異ベクトル）
- $U$ の列は $AA^\top$ の固有ベクトル（左特異ベクトル）

$A$ が実対称半正定値なら特異値 $=$ 固有値（$U = V$）。

---

## 一般化固有値問題

$A\boldsymbol{v} = \lambda B\boldsymbol{v}$（$B$ 正定値）形式の問題は $B^{-1/2}AB^{-1/2}$ の通常の固有値問題に帰着できます。主成分分析（PCA）・線形判別分析・有限要素法に現れます。

**参考文献**：Golub, G. H. & Van Loan, C. F. (2013). *Matrix Computations* (4th ed.). Johns Hopkins University Press.

---

## 関連ページ

- [固有値（標準）](standard.md)
- [行列（専門）](../matrices/professional.md)
- [線形写像（専門）](../linear-maps/professional.md)
