---
title: 負数
description: "整数環の代数的構造"
goal: "整数環の構成と性質を厳密に述べ、主イデアル整域としての構造を説明できるようになる"
tags: [math,numbers,negative-numbers]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 負数
    path: /math/numbers/negative-numbers/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 負数（標準）
    path: /math/numbers/negative-numbers/standard.md
  - title: 自然数（専門）
    path: /math/numbers/natural-numbers/professional.md
  - title: 集合
    path: /math/math-language/sets/introduction.md
---

## $\mathbb{N}$ からの $\mathbb{Z}$ の構成

自然数 $\mathbb{N}$ から整数 $\mathbb{Z}$ を厳密に構成します。

$\mathbb{N} \times \mathbb{N}$ 上に同値関係 $(a, b) \sim (c, d) \iff a + d = b + c$ を定めます。直感的には $(a, b)$ が $a - b$ を表しています。

この同値関係の下での同値類全体を $\mathbb{Z}$ とし、演算を次で定義します。

$$[(a,b)] + [(c,d)] = [(a+c, b+d)]$$
$$[(a,b)] \cdot [(c,d)] = [(ac+bd, ad+bc)]$$

これらが well-defined であること（代表元の取り方によらないこと）は、同値関係の定義から直接確認できます。

$n \in \mathbb{N}$ は $[(n+1, 1)]$ と同一視し、$0 = [(1, 1)]$、$-n = [(1, n+1)]$ とします。

---

## 整数環の性質

上の構成により、$\mathbb{Z}$ は以下の性質を持つ**可換環**です。

- 加法の単位元：$0$（$a + 0 = a$）
- 乗法の単位元：$1$（$a \times 1 = a$）
- 加法の逆元が常に存在：$a + (-a) = 0$
- 交換法則・結合法則・分配法則が成立

さらに $\mathbb{Z}$ は零因子を持たない**整域（integral domain）**です。

$$ab = 0 \implies a = 0 \text{ または } b = 0$$

**証明**：$a \neq 0$ かつ $b \neq 0$ と仮定します。$|ab| = |a||b|$（標準レベルで示した絶対値の性質）であり、$|a| \geq 1$、$|b| \geq 1$ なので $|ab| \geq 1 > 0$。よって $ab \neq 0$ です。$\square$

---

## 整列性と主イデアル整域

**定理**：$\mathbb{Z}$ の空でない部分集合が下に有界ならば、最小元を持つ。

これは $\mathbb{N}$ の整列原理から従います。

$\mathbb{Z}$ のイデアルはすべて単一の元で生成される**主イデアル**です。

$$n\mathbb{Z} = \{\ldots, -2n, -n, 0, n, 2n, \ldots\}$$

**定理**：$\mathbb{Z}$ の任意のイデアル $I$ は $I = n\mathbb{Z}$ の形で表される。

証明：$I = \{0\}$ のとき $n = 0$ で成立。$I \neq \{0\}$ のとき、$I$ に含まれる正の整数の最小値を $n$ とします（$a \in I$、$a \neq 0$ ならば $|a| \in I$ なので正の元が存在）。任意の $m \in I$ に対して除法の定理より $m = nq + r$（$0 \leq r < n$）。$r = m - nq \in I$ かつ $r < n$ なので $n$ の最小性より $r = 0$。よって $I \subset n\mathbb{Z}$。$n \in I$ より $n\mathbb{Z} \subset I$。$\square$

**系**：$\gcd(a, b)$ はイデアル $a\mathbb{Z} + b\mathbb{Z}$ の生成元です。ベズーの等式 $ax + by = \gcd(a,b)$ はこのイデアルの言い換えです。

---

## 剰余環 $\mathbb{Z}/n\mathbb{Z}$

主イデアル $n\mathbb{Z}$ による剰余環は

$$\mathbb{Z}/n\mathbb{Z} = \{[0], [1], \ldots, [n-1]\}$$

であり、$n$ 個の元からなる有限環です。

**定理**：$\mathbb{Z}/n\mathbb{Z}$ が体であるための必要十分条件は、$n$ が素数であることです。

証明：$n = p$（素数）のとき、$[a] \neq [0]$ ならば $\gcd(a, p) = 1$ なので、ベズーの等式より $ax + py = 1$。よって $[a][x] = [1]$ であり $[a]$ は逆元を持ちます。逆に $n$ が合成数ならば $n = ab$（$1 < a, b < n$）と書けて $[a][b] = [0]$ となるので零因子が存在し、体ではありません。$\square$

**参考文献**：Hungerford, T. W. (1974). *Algebra*. Springer.

---

## 関連ページ

- [負数（標準）](standard.md)
- [自然数（専門）](../natural-numbers/professional.md)
- [集合（専門）](../../math-language/sets/professional.md)