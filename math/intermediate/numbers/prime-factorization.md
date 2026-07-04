---
title: 素因数分解
description: "自然数を素数の積として表す"
goal: "素数の意味を理解し、自然数を素因数分解できるようになる"
tags: [math, numbers, prime-factorization]
stage: 中級編
subject: 数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 中級編
    path: /math/intermediate/index.md
  - title: 素因数分解
    path: /math/intermediate/numbers/prime-factorization.md
requires:
  - title: 倍数と約数
    path: /math/beginner/numbers/multiples-divisors.md
---

## 素数とは

$1$ と自分自身以外に約数を持たない、$1$より大きい自然数を**素数**といいます。$2, 3, 5, 7, 11, 13, \ldots$ が素数です。

$4$ は $1, 2, 4$ という約数を持つので素数ではありません。$1$ より大きい自然数は、素数か、素数でない数（複数の約数を持つ数）のどちらかに分けられます。

---

## 素因数分解

素数でない自然数は、より小さい自然数どうしの積に分解できます。

$$12 = 2 \times 6 = 2 \times 2 \times 3$$

これ以上分解できなくなるまで繰り返すと、最終的にすべて素数の積になります。これを**素因数分解**といい、使われる素数を**素因数**といいます。

$$12 = 2^2 \times 3$$

---

## 分解の仕方はいつも同じ結果になる

$12$ を分解する順序を変えてみましょう。$12 = 3 \times 4 = 3 \times 2 \times 2$ でも、並べ替えれば $2 \times 2 \times 3$ と同じです。

どの順番で分解しても、最終的にたどり着く素因数の組み合わせはただ一通りに決まります。これは自然数の重要な性質です。

**例**：$60$ を素因数分解する。$60 = 2 \times 30 = 2 \times 2 \times 15 = 2 \times 2 \times 3 \times 5$。よって $60 = 2^2 \times 3 \times 5$。

---

## まとめ

素数は $1$ と自分自身以外に約数を持たない数です。自然数を素数だけの積の形に分解することを素因数分解といい、分解の結果は順序を除いてただ一通りに決まります。

---

## 関連ページ

- [ユークリッドの互除法（応用編）](/math/advanced/numbers/euclidean-algorithm.md)
