---
title: 行列
description: "数を格子状に並べた構造"
difficulty: 2
tags: [math,linear-algebra,matrices]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 線形代数
    href: /math/linear-algebra/index.html
  - text: 行列
    href: /math/linear-algebra/matrices/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 行列
数を格子状に並べたものが**行列**です。
連立方程式をまとめて表したり、空間の変換（回転・拡大）を表したりできます。

## このページで扱うこと
- 行列の書き方と読み方
- 足し算・掛け算
- 逆行列と連立方程式

## 前提知識
- [ベクトル](../vectors/standard.md)
- [等号・等式](../../math-language/equations/standard.md)

---

## 行列とは？

$$A = \begin{pmatrix}1 & 2 \\ 3 & 4\end{pmatrix}$$

$2$ 行 $2$ 列の行列です。$(i,j)$ 成分は $i$ 行 $j$ 列の数です。

---

## 足し算

同じサイズの行列は成分ごとに足せます。

$$\begin{pmatrix}1&2\\3&4\end{pmatrix} + \begin{pmatrix}5&6\\7&8\end{pmatrix} = \begin{pmatrix}6&8\\10&12\end{pmatrix}$$

---

## 掛け算

$(AB)_{ij}$ は $A$ の $i$ 行と $B$ の $j$ 列の内積です。

$$\begin{pmatrix}1&2\\3&4\end{pmatrix}\begin{pmatrix}5\\6\end{pmatrix} = \begin{pmatrix}1 \times 5+2 \times 6\\3 \times 5+4 \times 6\end{pmatrix} = \begin{pmatrix}17\\39\end{pmatrix}$$

**注意**：$AB \neq BA$（順序を変えると一般に結果が変わる）

---

## 連立方程式を行列で書く

$$\begin{cases}2x + y = 5 \\ x - y = 1\end{cases} \iff \begin{pmatrix}2&1\\1&-1\end{pmatrix}\begin{pmatrix}x\\y\end{pmatrix} = \begin{pmatrix}5\\1\end{pmatrix}$$

---

## 逆行列

$AB = I$（単位行列）となる $B = A^{-1}$ を**逆行列**といいます。

$$\begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1} = \frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$$

$ad - bc = 0$ のとき逆行列は存在しません（$ad-bc$ を**行列式**という）。

---

## 関連ページ

- [ベクトル](../vectors/standard.md)
- [行列（発展）](../matrices/advanced.md) — より詳しく学ぶ
