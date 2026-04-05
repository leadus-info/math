---
title: 自然数
description: "自然数の厳密な構成・ペアノ公理・数論的性質"
tags: [math,numbers,natural-numbers]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 自然数
    path: /math/numbers/natural-numbers/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 自然数
    path: /math/numbers/natural-numbers/introduction.md
  - title: 必要・十分条件
    path: /math/math-language/conditions/introduction.md
  - title: 集合
    path: /math/math-language/sets/introduction.md
---

## ペアノ公理系

自然数を公理から構成します。以下の **ペアノの公理（PA）** を満たす集合 $\mathbb{N}$ と\
元 $1 \in \mathbb{N}$、写像 $S: \mathbb{N} \to \mathbb{N}$（後者写像）の組が自然数系です。

1. $1 \in \mathbb{N}$
2. 各 $n \in \mathbb{N}$ に対して後者 $S(n) \in \mathbb{N}$ が存在する
3. $S(n) = 1$ となる $n \in \mathbb{N}$ は存在しない（$1$ は誰の後者でもない）
4. $S(m) = S(n) \Rightarrow m = n$（$S$ は単射）
5. **帰納公理**：$M \subset \mathbb{N}$ が $1 \in M$ かつ $n \in M \Rightarrow S(n) \in M$ を満たすならば $M = \mathbb{N}$

加法は帰納的に定義します：$a + 1 := S(a)$、$a + S(n) := S(a + n)$。\
乗法も同様：$a \times 1 := a$、$a \times S(n) := (a \times n) + a$。

これらの定義から交換法則・結合法則・分配法則がすべて証明できます。

**参考文献**：Peano, G. (1889). *Arithmetices principia, nova methodo exposita*. Bocca.

---

## 整除論

**定義**：$b \mid a$ とは、$a = bq$ を満たす $q \in \mathbb{N}_0$ が存在することです。\
$b$ を $a$ の**約数**、$a$ を $b$ の**倍数**といいます。

**定理（除法の定理）**：任意の $a \in \mathbb{N}_0$、$b \in \mathbb{N}$ に対して\
$a = bq + r$、$0 \leq r < b$ を満たす $q, r \in \mathbb{N}_0$ の組がただ一つ存在します。

証明：存在は整列原理（$\mathbb{N}$ の任意の空でない部分集合は最小元を持つ）から従い、\
一意性は差を取ることで確認できます。

---

## ユークリッドの互除法とベズーの等式

**アルゴリズム（ユークリッドの互除法）**：\
$a = bq_1 + r_1$、$b = r_1 q_2 + r_2$、$r_1 = r_2 q_3 + r_3$、…\
余りが $0$ になったとき最後の非零余りが $\gcd(a,b)$ です。

$$\gcd(48, 18):\quad 48 = 18 \times 2 + 12,\quad 18 = 12 \times 1 + 6,\quad 12 = 6 \times 2 + 0$$

よって $\gcd(48, 18) = 6$。計算量は $O(\log \min(a,b))$ です。

**定理（ベズーの等式）**：任意の $a, b \in \mathbb{N}$ に対して\
$ax + by = \gcd(a,b)$ を満たす整数 $x, y$ が存在します。

証明：$S = \{ax + by \mid x, y \in \mathbb{Z},\ ax+by > 0\}$ の最小元が $\gcd(a,b)$ に一致することを示します。

**系**：$\gcd(a,b) = 1$（互いに素）$\iff$ $ax + by = 1$ を満たす整数 $x, y$ が存在する。

---

## 算術の基本定理

**定理**：$n > 1$ の任意の自然数は素数の積として順序を除いて一意に表せます。

**存在の証明**（強い帰納法）：$n = 2$ は素数なので成立。$n > 2$ で $2, \ldots, n-1$ について成立を仮定します。\
$n$ が素数なら自明。合成数なら $n = ab$（$1 < a, b < n$）と書けるので帰納仮定より各因数が素因数分解を持ちます。

**一意性の証明**（ユークリッドの補題による）：\
**補題**：素数 $p$ に対し $p \mid ab \Rightarrow p \mid a$ または $p \mid b$。\
補題の証明：$p \nmid a$ ならば $\gcd(p, a) = 1$ なのでベズーの等式より $px + ay = 1$。\
両辺に $b$ を掛けると $pbx + aby = b$、$p \mid ab$ より $p \mid b$。

**参考文献**：Hardy, G. H. & Wright, E. M. (1979). *An Introduction to the Theory of Numbers* (5th ed.). Oxford University Press.

---

## 合同算術とフェルマーの小定理

**定義**：$m \mid (a - b)$ のとき $a \equiv b \pmod{m}$ と書きます（$m$ を**法**といいます）。

合同は同値関係であり、加法・乗法と整合します。\
$\mathbb{Z}/m\mathbb{Z}$（剰余環）はこの同値類の環です。

**定理（フェルマーの小定理）**：素数 $p$ と $p \nmid a$ を満たす整数 $a$ に対して\
$$a^{p-1} \equiv 1 \pmod{p}$$

証明の方針：$\{a, 2a, \ldots, (p-1)a\}$ が $\pmod{p}$ で $\{1, 2, \ldots, p-1\}$ の置換になることを利用します。

**応用**：RSA暗号の正当性証明に使われます。

**参考文献**：Ireland, K. & Rosen, M. (1990). *A Classical Introduction to Modern Number Theory* (2nd ed.). Springer.

---

## 関連ページ

- [自然数](standard.md)
- [集合（専門）](../../math-language/sets/professional.md)
- [必要・十分条件（専門）](../../math-language/conditions/professional.md)
