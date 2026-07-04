---
title: 行列式
description: "変換による面積・体積の拡大率"
goal: "行列式の定義と幾何学的な意味を理解できるようになる"
tags: [math, linear-algebra, matrices]
stage: 発展編
subject: 線形代数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 発展編
    path: /math/bachelor/index.md
  - title: 行列式
    path: /math/bachelor/linear-algebra/matrices-determinant.md
requires:
  - title: 行列の積
    path: matrices-product.md
---

## 行列式の定義

正方行列 $A$ の**行列式** $\det(A)$：

$$\det\begin{pmatrix}a&b\\c&d\end{pmatrix} = ad - bc$$

**幾何学的意味**：$A$ が表す変換で面積が $|\det(A)|$ 倍になる（符号は向きの反転を表す）。$\det(A) = 0 \iff$ 逆行列が存在しない（変換が次元を下げる）。

---

## まとめ

行列式は、行列が表す線形変換によって面積・体積が何倍に拡大されるかを表す量で、$0$ になるかどうかが逆行列の存在を左右します。

---

## 関連ページ

- [行列の積（発展編）](matrices-product.md)
- [逆行列（発展編）](matrices-inverse.md)
