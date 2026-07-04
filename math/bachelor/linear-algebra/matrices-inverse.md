---
title: 逆行列
description: "変換を打ち消す操作"
goal: "逆行列の意味と2次行列の逆行列の公式を理解し、連立方程式を解く手段として使えるようになる"
tags: [math, linear-algebra, matrices]
stage: 発展編
subject: 線形代数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 発展編
    path: /math/bachelor/index.md
  - title: 逆行列
    path: /math/bachelor/linear-algebra/matrices-inverse.md
requires:
  - title: 行列式
    path: matrices-determinant.md
---

## 逆行列の定義

$AB = BA = I$（単位行列）を満たす $B$ を $A^{-1}$（逆行列）といいます。

$$\begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1} = \frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$$

連立方程式 $A\boldsymbol{x} = \boldsymbol{b}$ は、$\det(A) \neq 0$ のとき $\boldsymbol{x} = A^{-1}\boldsymbol{b}$ で解けます。

---

## まとめ

逆行列は、掛けると単位行列になる「変換を打ち消す」行列です。行列式が0でないときにのみ存在し、連立方程式を解く手段としても使えます。

---

## 関連ページ

- [行列式（発展編）](matrices-determinant.md)
- [固有値（発展編）](/math/bachelor/linear-algebra/eigenvalues.md)
