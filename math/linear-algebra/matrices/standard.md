---
title: 行列
description: "数を格子状に並べた構造"
tags: [math,linear-algebra,matrices]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 線形代数
    url: /math/linear-algebra/index.html
  - title: 行列
    url: /math/linear-algebra/matrices/standard.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
  - level: professional
    url: professional.html
level: standard
requires:
  - title: ベクトル
    url: professional.md
  - title: 等号・等式
    url: professional.md
---



数を格子状に並べたものが**行列**です。
連立方程式をまとめて扱ったり、空間の変換を表したりします。

## このページで扱うこと
- 行列の定義と基本演算
- 逆行列と連立方程式への応用
- 行列式の意味

---

## 行列とは

$$A = \begin{pmatrix}1 & 2 \\ 3 & 4\end{pmatrix}$$

$m$ 行 $n$ 列の数の表です。

---

## 足し算・スカラー倍

同じサイズの行列は成分ごとに足せます。

---

## 行列の積

$$\begin{pmatrix}1&2\\3&4\end{pmatrix}\begin{pmatrix}5\\6\end{pmatrix} = \begin{pmatrix}17\\39\end{pmatrix}$$

注意：$AB \neq BA$（順序を入れ替えると一般に変わる）

---

## 連立方程式と行列

$$\begin{cases}2x + y = 5 \\ x - y = 1\end{cases} \iff \begin{pmatrix}2&1\\1&-1\end{pmatrix}\begin{pmatrix}x\\y\end{pmatrix} = \begin{pmatrix}5\\1\end{pmatrix}$$

---

## 逆行列

$AB = I$ を満たす $B$ が逆行列 $A^{-1}$ です。

2 次行列：

$$\begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1} = \frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$$

---

## 行列式

$$\det\begin{pmatrix}a&b\\c&d\end{pmatrix} = ad - bc$$

$\det(A) = 0$ のとき逆行列は存在しません。

---

## 関連ページ

- [ベクトル](professional.md)
- [行列（専門）](professional.md) — スペクトル定理・SVD
