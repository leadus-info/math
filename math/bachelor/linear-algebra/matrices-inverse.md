---
title: 逆行列
description: "変換を打ち消す操作"
goal: "逆行列の意味と2次行列の逆行列の公式を理解し、余因子行列や掃き出し法によるn次正方行列の逆行列の求め方を説明し、連立方程式を解く手段として使えるようになる"
tags: [math, linear-algebra, matrices]
stage: bachelor
subject: 線形代数
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 逆行列
    path: matrices-inverse.md
requires:
  - title: 行列式
    path: matrices-determinant.md
---

## 逆行列の定義

$AB = BA = I$（単位行列）を満たす $B$ を $A^{-1}$（逆行列）といいます。

$$\begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1} = \frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$$

連立方程式 $A\boldsymbol{x} = \boldsymbol{b}$ は、$\det(A) \neq 0$ のとき $\boldsymbol{x} = A^{-1}\boldsymbol{b}$ で解けます。

---

## n次正方行列の逆行列：余因子行列

行列式（発展編）の余因子 $A_{ij}$ を並べた行列の転置を**余因子行列**（**随伴行列**）といい、次の公式で逆行列が求まります。

$$A^{-1} = \frac{1}{\det(A)}\,\mathrm{adj}(A), \qquad \mathrm{adj}(A) = \begin{pmatrix}A_{11} & A_{21} & \cdots \\ A_{12} & A_{22} & \cdots \\ \vdots & & \ddots\end{pmatrix}$$

（$2$ 次の場合、この公式は $\dfrac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$ に一致します。）余因子の計算量が $n$ が大きくなると急激に増えるため、実際の計算では次の**掃き出し法**がよく使われます。

**掃き出し法**：$(A \mid I)$ という $n \times 2n$ 行列を作り、行基本変形（行の入れ替え・定数倍・他の行への加算）を繰り返して左半分を単位行列 $I$ にすると、右半分が $A^{-1}$ になります。

---

## まとめ

逆行列は、掛けると単位行列になる「変換を打ち消す」行列です。行列式が0でないときにのみ存在し、余因子行列を使った公式や掃き出し法で求められ、連立方程式を解く手段としても使えます。

---

## 関連ページ

- [固有値（発展編）](eigenvalues.md)
