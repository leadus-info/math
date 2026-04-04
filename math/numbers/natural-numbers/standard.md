---
title: 自然数
description: "ものを数えるときに使う数"
tags: [math,numbers,natural-numbers]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 数
    url: /math/numbers/index.html
  - title: 自然数
    url: /math/numbers/natural-numbers/standard.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
  - level: professional
    url: professional.html
level: standard
---

自然数は $1, 2, 3, \ldots$ と続く、ものを数えるための数です。
このページでは、自然数の構造を数学的に観察します。

## 自然数の定義

$$\mathbb{N} = \{1, 2, 3, 4, 5, \ldots\}$$

「$\ldots$」は「この先も同じように続く」という意味です。
自然数には最大値が存在しません——どんな自然数 $n$ に対しても、$n+1$ という自然数が必ず存在します。

> **0を含めるかどうか？**
> 流儀によって異なります。このサイトでは $\mathbb{N} = \{1,2,3,\ldots\}$（0を含まない）を基本とし、
> 必要に応じて $\mathbb{N}_0 = \{0,1,2,3,\ldots\}$ と区別します。

---

## 大小関係

任意の二つの自然数 $m, n$ について

$$m < n \quad \text{または} \quad m = n \quad \text{または} \quad m > n$$

のどれか**一つだけ**が成り立ちます。これを**全順序**といいます。

**推移律**：$a < b$ かつ $b < c$ ならば $a < c$

---

## 足し算（加法）

$a, b \in \mathbb{N}$ に対して $a + b \in \mathbb{N}$ が定まります。
自然数どうしの和は必ず自然数になります（**加法について閉じている**）。

**交換法則**：$a + b = b + a$

**結合法則**：$(a + b) + c = a + (b + c)$

結合法則のおかげで $1 + 2 + 3$ のように括弧を省略して書けます。

---

## 掛け算（乗法）

掛け算は「同じ数を繰り返し足すこと」として定義できます。

$$a \times n = \underbrace{a + a + \cdots + a}_{n \text{ 回}}$$

自然数どうしの積も必ず自然数になります（**乗法について閉じている**）。

**交換法則**：$a \times b = b \times a$

**結合法則**：$(a \times b) \times c = a \times (b \times c)$

**分配法則**：$a \times (b + c) = a \times b + a \times c$

分配法則は足し算と掛け算をつなぐ最も重要な性質です。
例：$3 \times (4 + 5) = 3 \times 4 + 3 \times 5 = 12 + 15 = 27$

**計算の優先順位**：掛け算は足し算より先に計算します。
$(2 + 3) \times 4 = 20$ ですが $2 + 3 \times 4 = 14$ です。

---

## 引き算の限界

$a - b$ が自然数として存在するのは $a > b$ のときだけです。
$3 - 5$ のように $a < b$ の場合、自然数の中に答えがありません。

この限界を解決するために**負数**が導入されます。

---

## 割り算の限界

$a \div b$ が自然数として存在するのは「$b$ が $a$ を割り切る」場合だけです。
$5 \div 2$ のように割り切れない場合、自然数の中に答えがありません。

余りを使えば自然数の中で表せます：$5 = 2 \times 2 + 1$（商2、余り1）。
割り切れない場合に完全な答えを与えるために**分数**が導入されます。

---

## 素数と素因数分解

1より大きい自然数で、1と自分自身以外に約数を持たないものを**素数**といいます。

$$2, 3, 5, 7, 11, 13, 17, 19, \ldots$$

**算術の基本定理**：1より大きい任意の自然数は、素数の積として一通りに表せます（順序を除く）。

$$12 = 2^2 \times 3, \quad 60 = 2^2 \times 3 \times 5, \quad 100 = 2^2 \times 5^2$$

---

## 関連ページ

- [負数](../negative-numbers/introduction.md) — 引き算の限界から生まれる数
- [分数](../fractions/introduction.md) — 割り算の限界から生まれる数
- [乗法・べき乗](../arithmetic/introduction.md) — 掛け算をさらに発展させる
