---
title: 負数
description: "整数環の代数的構造"
goal: "整数環の公理的な性質を理解し、イデアル・剰余環の構造を説明できるようになる"
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
  - title: 集合（入門）
    path: /math/math-language/sets/introduction.md
---

## $\mathbb{Z}$ の構成

自然数 $\mathbb{N}$ から整数 $\mathbb{Z}$ を構成します。$\mathbb{N} \times \mathbb{N}$ 上の同値関係

$$(a, b) \sim (c, d) \iff a + d = b + c$$

による同値類の集合として $\mathbb{Z}$ を定義します。直感的には $(a, b)$ は「$a - b$」を表します。

演算は以下のように定義されます。

$$[(a,b)] + [(c,d)] = [(a+c, b+d)]$$
$$[(a,b)] \times [(c,d)] = [(ac+bd, ad+bc)]$$

これらが同値類の代表元の取り方によらないこと（well-defined 性）を確認する必要があります。

---

## 整数環

$\mathbb{Z}$ は加法と乗法について以下の性質を持ちます。

- 加法について可換群：結合法則、交換法則、単位元 $0$、逆元 $-a$
- 乗法について可換モノイド：結合法則、交換法則、単位元 $1$
- 分配法則：$a(b + c) = ab + ac$

これらの性質を合わせて、$\mathbb{Z}$ は**可換環（commutative ring）**です。

さらに $\mathbb{Z}$ は零因子を持ちません。

$$ab = 0 \implies a = 0 \text{ または } b = 0$$

零因子を持たない可換環を**整域（integral domain）**といいます。

負数（標準）で前提とした符号規則は、環の公理から証明できます。$(-1) \times a = -a$ の証明：$a + (-1) \times a = 1 \times a + (-1) \times a = (1 + (-1)) \times a = 0 \times a = 0$。よって $(-1) \times a$ は $a$ の加法逆元 $-a$ です。$\square$

---

## イデアルと主イデアル整域

**定義**：$\mathbb{Z}$ の部分集合 $I$ が**イデアル**であるとは、$I$ が加法について部分群であり、任意の $a \in I$、$z \in \mathbb{Z}$ に対して $za \in I$ が成り立つことです。

$\mathbb{Z}$ のイデアルはすべて**主イデアル**（単一の元で生成されるイデアル）です。

$$n\mathbb{Z} = \{nk \mid k \in \mathbb{Z}\} = \{\ldots, -2n, -n, 0, n, 2n, \ldots\}$$

**定理**：$\mathbb{Z}$ は主イデアル整域（PID）である。

証明：$I$ を $\mathbb{Z}$ の $\{0\}$ でないイデアルとします。$I$ に属する正の整数のうち最小のものを $d$ とします（整列原理）。任意の $a \in I$ に対して除法の定理より $a = dq + r$（$0 \leq r < d$）。$r = a - dq \in I$ であり $r < d$ なので $r = 0$。よって $I = d\mathbb{Z}$。$\square$

$\gcd(a, b)$ はイデアル $a\mathbb{Z} + b\mathbb{Z}$ の生成元に対応します。自然数（専門）で示したベズーの等式 $ax + by = \gcd(a,b)$ はこの視点から自然に理解できます。

---

## 剰余環 $\mathbb{Z}/n\mathbb{Z}$

イデアル $n\mathbb{Z}$ による剰余環を定義します。

$$\mathbb{Z}/n\mathbb{Z} = \{[0], [1], \ldots, [n-1]\}$$

ここで $[a] = \{a + nk \mid k \in \mathbb{Z}\}$ は $a$ を含む剰余類です。

**定理**：$n$ が素数のとき $\mathbb{Z}/n\mathbb{Z}$ は**体**（すべての非零元が乗法逆元を持つ）。$n$ が合成数のとき $\mathbb{Z}/n\mathbb{Z}$ は零因子を持ち、体ではない。

**例**：$\mathbb{Z}/5\mathbb{Z}$ は体です。$[2] \times [3] = [6] = [1]$ なので $[2]$ の逆元は $[3]$ です。

$\mathbb{Z}/6\mathbb{Z}$ は体ではありません。$[2] \times [3] = [6] = [0]$ なので $[2]$ と $[3]$ は零因子です。

**参考文献**：Hungerford, T. W. (1974). *Algebra*. Springer.

---

## 関連ページ

- [負数（標準）](standard.md)
- [自然数（専門）](../natural-numbers/professional.md)
- [集合（専門）](../../math-language/sets/professional.md)