---
title: 自然数
description: "自然数の公理的構成と整数論の基礎"
goal: "ペアノ公理から自然数の演算を構成する過程を説明でき、算術の基本定理を厳密に証明できるようになる"
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
    path: /math/numbers/natural-numbers/standard.md
  - title: 必要・十分条件
    path: /math/math-language/conditions/introduction.md
  - title: 集合
    path: /math/math-language/sets/introduction.md
---

## ペアノ公理系

標準レベルでは自然数の演算法則を「成り立つもの」として扱いました。ここでは、なぜそれらが成り立つのかを、公理から出発して構成します。

以下の **ペアノの公理（PA）** を満たす集合 $\mathbb{N}$、元 $1 \in \mathbb{N}$、写像 $S: \mathbb{N} \to \mathbb{N}$（後者写像）の組を**自然数系**と呼びます。

1. $1 \in \mathbb{N}$
2. 各 $n \in \mathbb{N}$ に対して $S(n) \in \mathbb{N}$
3. $S(n) = 1$ となる $n \in \mathbb{N}$ は存在しない（$1$ は後者ではない）
4. $S(m) = S(n) \Rightarrow m = n$（$S$ は単射）
5. **帰納公理**：$M \subset \mathbb{N}$ が $1 \in M$ かつ $n \in M \Rightarrow S(n) \in M$ を満たすならば $M = \mathbb{N}$

公理5が数学的帰納法の根拠です。「$1$ で成り立ち、$n$ で成り立てば $S(n)$ でも成り立つ」性質は、すべての自然数で成り立ちます。

---

## 加法と乗法の構成

加法は帰納的に定義します。

$$a + 1 := S(a), \quad a + S(n) := S(a + n)$$

乗法も同様に定義します。

$$a \times 1 := a, \quad a \times S(n) := (a \times n) + a$$

これらの定義から、標準レベルで前提とした交換法則・結合法則・分配法則がすべて証明できます。例として加法の交換法則を示します。

**定理**：$a + b = b + a$

証明：$b$ に関する帰納法。$b = 1$ のとき $a + 1 = S(a)$ であり、$1 + a = a$（$a$ に関する帰納法で別途示す）の後者なので $a + 1 = 1 + a$。$b = n$ で成立を仮定すると $a + S(n) = S(a + n) = S(n + a) = n + S(a) = n + (a + 1) = n + (1 + a) = (n + 1) + a = S(n) + a$。$\square$

**参考文献**：Peano, G. (1889). *Arithmetices principia, nova methodo exposita*. Bocca.

---

## 整列原理と除法の定理

**定理（整列原理）**：$\mathbb{N}$ の任意の空でない部分集合は最小元を持つ。

整列原理は帰納公理（公理5）と同値であり、以降の証明で繰り返し用います。

**定理（除法の定理）**：任意の $a \in \mathbb{N}_0$、$b \in \mathbb{N}$ に対して、$a = bq + r$、$0 \leq r < b$ を満たす $q, r \in \mathbb{N}_0$ の組がただ一つ存在する。

存在の証明：$S = \{a - bk \mid k \in \mathbb{N}_0,\ a - bk \geq 0\}$ は空でない（$k = 0$ で $a \in S$）。整列原理より $S$ は最小元 $r$ を持ちます。対応する $k$ を $q$ とすれば $a = bq + r$。$r \geq b$ と仮定すると $r - b \geq 0$ で $r - b \in S$ となり $r$ の最小性に矛盾。よって $0 \leq r < b$。

一意性の証明：$a = bq_1 + r_1 = bq_2 + r_2$（$0 \leq r_1, r_2 < b$）とすると $b|q_1 - q_2| = |r_1 - r_2| < b$。よって $|q_1 - q_2| = 0$、すなわち $q_1 = q_2$、$r_1 = r_2$。$\square$

---

## ユークリッドの互除法とベズーの等式

**アルゴリズム（ユークリッドの互除法）**：除法の定理を繰り返し適用します。

$$a = bq_1 + r_1, \quad b = r_1 q_2 + r_2, \quad r_1 = r_2 q_3 + r_3, \quad \ldots$$

余り列 $r_1 > r_2 > r_3 > \cdots \geq 0$ は狭義単調減少な自然数列なので有限ステップで $0$ に到達します。最後の非零余りが $\gcd(a,b)$ です。計算量は $O(\log \min(a,b))$ です。

**定理（ベズーの等式）**：任意の $a, b \in \mathbb{N}$ に対して、$ax + by = \gcd(a,b)$ を満たす整数 $x, y$ が存在する。

証明：$S = \{ax + by \mid x, y \in \mathbb{Z},\ ax+by > 0\}$ とします。$S$ は空でなく（$a \in S$）、整列原理より最小元 $d$ を持ちます。$d \mid a$ を示します。除法の定理より $a = dq + r$（$0 \leq r < d$）。$d = ax_0 + by_0$ と書けるので $r = a - dq = a(1 - qx_0) + b(-qy_0)$。$r > 0$ ならば $r \in S$ で $d$ の最小性に矛盾。よって $r = 0$、$d \mid a$。同様に $d \mid b$。$a, b$ の任意の公約数 $c$ に対し $c \mid (ax_0 + by_0) = d$ なので $d = \gcd(a,b)$。$\square$

**系**：$\gcd(a,b) = 1 \iff ax + by = 1$ を満たす整数 $x, y$ が存在する。

---

## 算術の基本定理

**定理**：$n > 1$ の任意の自然数は素数の積として順序を除いて一意に表せる。

**存在の証明**（強い帰納法）：$n = 2$ は素数なので成立。$n > 2$ で $2, \ldots, n-1$ について成立を仮定します。$n$ が素数ならば自明。$n$ が合成数ならば $n = ab$（$1 < a, b < n$）と書けるので、帰納仮定より $a, b$ がそれぞれ素因数分解を持ち、それらの積が $n$ の素因数分解です。

**一意性の証明**：以下の補題を用います。

**補題（ユークリッドの補題）**：素数 $p$ に対し、$p \mid ab \Rightarrow p \mid a$ または $p \mid b$。

補題の証明：$p \nmid a$ と仮定します。$p$ が素数なので $\gcd(p, a) = 1$ です。ベズーの等式より $px + ay = 1$ を満たす整数 $x, y$ が存在します。両辺に $b$ を掛けると $pbx + aby = b$。$p \mid ab$ より $p \mid aby$、自明に $p \mid pbx$ なので $p \mid b$。$\square$

一意性の証明本体：$n = p_1 \cdots p_r = q_1 \cdots q_s$ とします。$p_1 \mid q_1 \cdots q_s$ にユークリッドの補題を繰り返し適用すると、ある $q_j$ に対して $p_1 \mid q_j$。$q_j$ は素数なので $p_1 = q_j$。両辺を $p_1$ で割り、帰納法により残りの因数も一致します。$\square$

**参考文献**：Hardy, G. H. & Wright, E. M. (1979). *An Introduction to the Theory of Numbers* (5th ed.). Oxford University Press.

---

## 関連ページ

- [自然数（標準）](standard.md)
- [集合（専門）](../../math-language/sets/professional.md)
- [必要・十分条件（専門）](../../math-language/conditions/professional.md)