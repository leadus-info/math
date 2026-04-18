---
title: 場合の数
description: "順列・組み合わせ・二項定理"
goal: "順列・組み合わせの公式を導出し、二項定理を使って場合の数を計算できるようになる"
tags: [math,statistics,counting]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 統計・確率
    path: /math/statistics/index.md
  - title: 場合の数
    path: /math/statistics/counting/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 場合の数（入門）
    path: /math/statistics/counting/introduction.md
  - title: 自然数（標準）
    path: /math/numbers/natural-numbers/standard.md
---

## 階乗

$n!$（$n$ の**階乗**）は $1$ から $n$ までのすべての整数の積です。

$$n! = n \times (n-1) \times \cdots \times 2 \times 1$$

$$0! = 1, \quad 1! = 1, \quad 5! = 120, \quad 10! = 3628800$$

---

## 順列

$n$ 個から $r$ 個を順番を区別して選ぶ場合の数（**順列**）：

$$_nP_r = \frac{n!}{(n-r)!} = n(n-1)\cdots(n-r+1)$$

**例**：5人から3人を「1位・2位・3位」に：$_5P_3 = 5 \times 4 \times 3 = 60$

**導出**：1位の選び方は5通り、2位は残り4通り、3位は残り3通り。$5 \times 4 \times 3 = 60$。

---

## 組み合わせ

$n$ 個から $r$ 個を順番を区別せず選ぶ場合の数（**組み合わせ**）：

$$\binom{n}{r} = \frac{n!}{r!(n-r)!} = \frac{_nP_r}{r!}$$

**例**：5人から3人のチームを選ぶ：$\binom{5}{3} = \frac{60}{6} = 10$

順列を $r!$ で割るのは、$r$ 個の選択物の並べ方（$r!$ 通り）が同一視されるためです。

**性質**：$\binom{n}{r} = \binom{n}{n-r}$（選ぶのと選ばないのを入れ替えても同じ）

---

## 二項定理

$$(a + b)^n = \sum_{k=0}^n \binom{n}{k} a^{n-k} b^k$$

**例**：$(a+b)^3 = a^3 + 3a^2b + 3ab^2 + b^3$

係数 $\binom{3}{0}=1$, $\binom{3}{1}=3$, $\binom{3}{2}=3$, $\binom{3}{3}=1$。

**応用**：$(1+x)^n = 1 + nx + \binom{n}{2}x^2 + \cdots$（$|x|$ が小さいとき近似に使う）

---

## 重複組み合わせ

$n$ 種類から重複を許して $r$ 個選ぶ場合の数：

$$\binom{n+r-1}{r}$$

**例**：りんご・みかん・ぶどうから3個選ぶ（同じ種類を複数可）：$\binom{3+3-1}{3} = \binom{5}{3} = 10$

---

## 関連ページ

- [確率（標準）](../probability/standard.md)
- [場合の数（専門）](professional.md)
