---
title: 行列
description: "数を格子状に並べた行列を、連立方程式の係数をまとめる表現とベクトルを変換する操作という2つの視点から定義し、加法・スカラー倍の計算方法を扱う"
goal: "行列を連立方程式の表現・線形変換の両面から理解し、加法・スカラー倍を計算できるようになる"
tags: [math, linear-algebra, matrices]
stage: bachelor
subject: 線形代数
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 行列
    path: matrices.md
requires:
  - title: ベクトル
    path: vectors.md
  - title: 連立方程式
    path: ../../intermediate/algebra/equations-simultaneous.md
---

## 数を格子状に並べる

$$\begin{pmatrix} 2 & 1 \\ 1 & -1 \end{pmatrix}$$

こんな「数の表」が**行列**です。横の並びを「行」、縦の並びを「列」と呼びます。連立方程式

$$\begin{cases} 2x + y = 5 \\ x - y = 1 \end{cases}$$

の解き方は[連立方程式](../../intermediate/algebra/equations-simultaneous.md)で扱いました。この係数を取り出すと $\begin{pmatrix} 2 & 1 \\ 1 & -1 \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 5 \\ 1 \end{pmatrix}$ と書けます。掛け算の具体的な計算方法は[行列の積](matrices-product.md)で扱うので、ここでは結果だけを先に見せています。

2本でも100本でも同じ形で書けるのが行列の強みです。

同じ行列でも、連立方程式の係数として読めば数の表ですが、ベクトルに掛ける計算として読めば「変換する操作」にもなります。行列はこの見方によって、回転・拡大縮小・反転をすべて統一的に表せます。

**例**：平面上のベクトルを反時計回りに90°回転させる変換は $\begin{pmatrix}0&-1\\1&0\end{pmatrix}$ で表されます。行列の各列は、基本ベクトルがそれぞれ移った先を表しています。基本ベクトルを$e_1=(1,0)$、$e_2=(0,1)$とすると、1列目の$(0,1)$は$e_1$の移動先、2列目の$(-1,0)$は$e_2$の移動先です。実際に $\begin{pmatrix}0&-1\\1&0\end{pmatrix}\begin{pmatrix}1\\0\end{pmatrix}=\begin{pmatrix}0\\1\end{pmatrix}$ のように、$x$軸方向のベクトル$(1,0)$を$y$軸方向の$(0,1)$に移します。

---

## 行列の定義と基本演算

$m$ 行 $n$ 列の行列は数を $m \times n$ の格子に並べたもので、$(i, j)$ 成分を $a_{ij}$ と書きます。

**加法**（同じサイズ同士）：成分ごとに足します。$(A+B)_{ij} = a_{ij} + b_{ij}$ **例**：$\begin{pmatrix}2&1\\1&-1\end{pmatrix}+\begin{pmatrix}0&3\\-2&1\end{pmatrix}=\begin{pmatrix}2&4\\-1&0\end{pmatrix}$

**スカラー倍**：すべての成分に定数を掛けます。$(cA)_{ij} = c\,a_{ij}$ **例**：$3\begin{pmatrix}2&1\\1&-1\end{pmatrix}=\begin{pmatrix}6&3\\3&-3\end{pmatrix}$

---

## まとめ

行列は「数を格子状に並べた構造」で、連立方程式をひとつの式で表す道具であると同時に、ベクトルを変換する操作でもあります。加法・スカラー倍は成分ごとに計算します。

---

## 関連ページ

- [行列の積](matrices-product.md)
- [行列式](matrices-determinant.md)
- [逆行列](matrices-inverse.md)
