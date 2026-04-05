---
title: 自然数
description: "ものを数えるときに使う数"
tags: [math,numbers,natural-numbers]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 自然数
    path: /math/numbers/natural-numbers/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
---

## 自然数の定義

$$\mathbb{N} = \{1, 2, 3, 4, 5, \ldots\}$$

自然数とは、$1$ から始まり $1$ ずつ増えていく数の列全体です。\
任意の自然数 $n$ に対して $n+1$ も自然数であり、自然数には最大値が存在しません。

> **0を含めるかどうか：** 流儀によって異なります。このサイトでは $\mathbb{N} = \{1,2,3,\ldots\}$（0を含まない）を基本とします。\
> 0を含む場合は $\mathbb{N}_0 = \{0,1,2,3,\ldots\}$ と書いて区別します。

---

## 大小関係（全順序）

任意の自然数 $m, n$ について、次の三つのうちちょうど一つが成り立ちます。

$$m < n \quad \text{または} \quad m = n \quad \text{または} \quad m > n$$

これを**全順序**といいます。

**定理（推移律）**：$a < b$ かつ $b < c$ ならば $a < c$

証明の方針：$a < b$ は「$b = a + k$（$k \in \mathbb{N}$）」、$b < c$ は「$c = b + l$（$l \in \mathbb{N}$）」と書けるので\
$c = a + (k + l)$ となり $a < c$。

---

## 加法（足し算）

$a, b \in \mathbb{N}$ に対して $a + b \in \mathbb{N}$ が定まります（**加法について閉じている**）。

**交換法則**：$a + b = b + a$\
**結合法則**：$(a + b) + c = a + (b + c)$

結合法則のおかげで $1 + 2 + 3 + 4$ のように括弧なしで書けます。\
$\mathbb{N}_0$ では $a + 0 = a$ が成り立ち、$0$ は加法の**単位元**です。

---

## 乗法（掛け算）

掛け算は加法を使って次のように定義します。

$$a \times n = \underbrace{a + a + \cdots + a}_{n \text{ 個}}$$

$a, b \in \mathbb{N}$ に対して $a \times b \in \mathbb{N}$（**乗法について閉じている**）。

**交換法則**：$a \times b = b \times a$\
**結合法則**：$(a \times b) \times c = a \times (b \times c)$\
**分配法則**：$a \times (b + c) = a \times b + a \times c$

**例**（分配法則の計算）：\
$7 \times 13 = 7 \times (10 + 3) = 70 + 21 = 91$

分配法則は展開や因数分解の根拠となる最重要法則です。

**計算の優先順位**：乗法は加法より先に計算します。\
$(2 + 3) \times 4 = 20$ ですが $2 + 3 \times 4 = 2 + 12 = 14$ です。

---

## 引き算と除法の限界

$a - b$ が $\mathbb{N}$ に属するのは $a > b$ のときだけです。\
$a \leq b$ では答えが $\mathbb{N}$ の外に出るため**引き算は閉じていません**。

$a \div b$ が $\mathbb{N}$ に属するのは $b \mid a$（$b$ が $a$ を割り切る）のときだけです。\
割り切れない場合は**余り**を使って表します。

> **除法の定理**：任意の $a \in \mathbb{N}$、$b \in \mathbb{N}$ に対して、\
> $a = b \times q + r$、$0 \leq r < b$ を満たす $q, r \in \mathbb{N}_0$ がただ一組存在します。

**例**：$17 \div 5$\
$17 = 5 \times 3 + 2$ より、商 $q = 3$、余り $r = 2$。

---

## 素数と素因数分解

**定義**：$1$ より大きい自然数で、$1$ と自分自身以外に正の約数を持たないものを**素数**といいます。\
素数でない $2$ 以上の自然数を**合成数**といいます。

$$\text{素数}：2, 3, 5, 7, 11, 13, 17, 19, 23, \ldots$$

**定理（算術の基本定理）**：$1$ より大きい任意の自然数は、\
素数の積として順序を除いて一意に表せます。

$$12 = 2^2 \times 3, \quad 60 = 2^2 \times 3 \times 5, \quad 360 = 2^3 \times 3^2 \times 5$$

**例題**：$\gcd(24, 36)$（最大公約数）を素因数分解で求めます。\
$24 = 2^3 \times 3$、$36 = 2^2 \times 3^2$ より\
$\gcd(24, 36) = 2^2 \times 3 = 12$

---

## 関連ページ

- [乗法・べき乗](../arithmetic/introduction.md) — 掛け算のさらなる発展
- [負数](../negative-numbers/introduction.md) — 引き算の限界から生まれる数
- [分数](../fractions/introduction.md) — 割り算の限界から生まれる数
