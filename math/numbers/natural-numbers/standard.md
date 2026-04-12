---
title: 自然数
description: "自然数の定義と演算の構造"
goal: "自然数の演算法則を正確に述べ、除法の定理や素因数分解の一意性を用いた計算ができるようになる"
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
requires:
  - title: 自然数
    path: /math/numbers/natural-numbers/introduction.md
---

## 自然数の定義

$$\mathbb{N} = \{1, 2, 3, 4, 5, \ldots\}$$

自然数とは、$1$ から始まり $1$ ずつ増えていく数の集合です。任意の自然数 $n$ に対して $n+1$ も自然数であり、最大値は存在しません。

> **0を含めるかどうか：** 流儀によって異なります。このサイトでは $\mathbb{N} = \{1,2,3,\ldots\}$（0を含まない）を基本とします。0を含む場合は $\mathbb{N}_0 = \{0,1,2,3,\ldots\}$ と書いて区別します。

---

## 大小関係（全順序）

任意の自然数 $m, n$ について、$m < n$、$m = n$、$m > n$ のうちちょうど一つが成り立ちます。これを**三分律**といい、この性質を持つ順序を**全順序**と呼びます。

**定理（推移律）**：$a < b$ かつ $b < c$ ならば $a < c$。

証明：$a < b$ は $b = a + k$（$k \in \mathbb{N}$）、$b < c$ は $c = b + l$（$l \in \mathbb{N}$）と書けます。代入すると $c = a + (k + l)$ であり、$k + l \in \mathbb{N}$ なので $a < c$ です。$\square$

---

## 加法の性質

$a, b \in \mathbb{N}$ に対して $a + b \in \mathbb{N}$ です。これを「$\mathbb{N}$ は加法について**閉じている**」といいます。

加法は以下の法則を満たします。

**交換法則**：$a + b = b + a$

**結合法則**：$(a + b) + c = a + (b + c)$

結合法則により、$1 + 2 + 3 + 4$ のように括弧を省略して書けます。なお、$\mathbb{N}_0$ では $a + 0 = a$ が成り立ち、$0$ は加法の**単位元**です。

---

## 乗法の性質

掛け算は「同じ数を繰り返し足す操作」として定義されます。

$$a \times n = \underbrace{a + a + \cdots + a}_{n \text{ 個}}$$

$a, b \in \mathbb{N}$ に対して $a \times b \in \mathbb{N}$ であり、$\mathbb{N}$ は乗法についても閉じています。

**交換法則**：$a \times b = b \times a$

**結合法則**：$(a \times b) \times c = a \times (b \times c)$

**分配法則**：$a \times (b + c) = a \times b + a \times c$

分配法則は加法と乗法をつなぐ法則であり、展開や因数分解の根拠になります。

**例**（分配法則の活用）：$7 \times 13 = 7 \times (10 + 3) = 70 + 21 = 91$

**計算の優先順位**：乗法は加法より先に計算します。$(2 + 3) \times 4 = 20$ ですが、$2 + 3 \times 4 = 2 + 12 = 14$ です。

---

## 引き算と除法の限界

入門で見た「自然数ではできないこと」を正確に述べます。

$a - b$ が $\mathbb{N}$ に属するのは $a > b$ のときだけです。$a \leq b$ では答えが $\mathbb{N}$ の外に出るため、$\mathbb{N}$ は減法について閉じていません。

除法も同様に閉じていませんが、こちらは**商と余り**で完全に記述できます。

> **除法の定理**：任意の $a \in \mathbb{N}$、$b \in \mathbb{N}$ に対して、$a = b \times q + r$、$0 \leq r < b$ を満たす $q, r \in \mathbb{N}_0$ の組がただ一つ存在する。

**例**：$17 \div 5$ → $17 = 5 \times 3 + 2$ より、商 $q = 3$、余り $r = 2$。

除法の定理は「割り切れなくても、商と余りで必ず表せる」ことを保証します。ここから最大公約数や素因数分解の議論につながります。

---

## 素数と算術の基本定理

**定義**：$1$ より大きい自然数で、$1$ と自分自身以外に正の約数を持たないものを**素数**といいます。素数でない $2$ 以上の自然数を**合成数**といいます。

$$\text{素数}：2, 3, 5, 7, 11, 13, 17, 19, 23, \ldots$$

素数は自然数の「これ以上分解できない構成要素」です。

**定理（算術の基本定理）**：$1$ より大きい任意の自然数は、素数の積として順序を除いて一意に表せる。

$$12 = 2^2 \times 3, \quad 60 = 2^2 \times 3 \times 5, \quad 360 = 2^3 \times 3^2 \times 5$$

この定理は「分解のしかたは一通りしかない」と主張しています。$12 = 2 \times 6 = 3 \times 4$ のように途中経過は複数ありますが、最終的な素因数の組み合わせは $2^2 \times 3$ に一致します。

**応用例**（最大公約数）：$24 = 2^3 \times 3$、$36 = 2^2 \times 3^2$ の共通部分を取ると $\gcd(24, 36) = 2^2 \times 3 = 12$。

---

## 関連ページ

- [四則演算](../arithmetic/introduction.md) — 演算の体系的な扱い
- [負数](../negative-numbers/introduction.md) — 引き算の限界から生まれる数
- [分数](../fractions/introduction.md) — 割り算の限界から生まれる数