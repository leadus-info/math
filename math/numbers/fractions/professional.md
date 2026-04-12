---
title: 分数
description: "有理数体の構成と性質"
goal: "整数から同値類によって有理数体を構成する過程を説明でき、有理数の稠密性と可算性を証明できるようになる"
tags: [math,numbers,fractions]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 分数
    path: /math/numbers/fractions/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 分数（標準）
    path: /math/numbers/fractions/standard.md
  - title: 負数（専門）
    path: /math/numbers/negative-numbers/professional.md
  - title: 集合
    path: /math/math-language/sets/introduction.md
---

## 同値類による $\mathbb{Q}$ の構成

標準レベルでは $\frac{a}{b} = \frac{c}{d} \iff ad = bc$ を分数の相等として扱いました。ここではこれを同値関係として定式化し、$\mathbb{Q}$ を厳密に構成します。

$\mathbb{Z} \times (\mathbb{Z} \setminus \{0\})$ 上に同値関係を定義します。

$$(a, b) \sim (c, d) \iff ad = bc$$

$\sim$ が反射律・対称律・推移律を満たすことを確認します。反射律と対称律は自明。推移律は $(a,b) \sim (c,d)$ かつ $(c,d) \sim (e,f)$ のとき $ad = bc$、$cf = de$ より $adf = bcf = bde$ であり $d \neq 0$ なので $af = be$、すなわち $(a,b) \sim (e,f)$。$\square$

同値類 $[(a,b)]$ を $\frac{a}{b}$ と書き、同値類全体の集合を $\mathbb{Q}$ とします。

---

## $\mathbb{Q}$ 上の演算と体の構造

演算を次で定義します。

$$[(a,b)] + [(c,d)] = [(ad+bc, bd)]$$
$$[(a,b)] \cdot [(c,d)] = [(ac, bd)]$$

これらが well-defined であること（代表元の選び方によらないこと）は同値関係の定義から直接確認できます。

この演算の下で $\mathbb{Q}$ は**体（field）**です。すなわち以下を満たします。

- $(\mathbb{Q}, +)$ は可換群（単位元 $0 = [(0,1)]$、逆元 $-\frac{a}{b} = \frac{-a}{b}$）
- $(\mathbb{Q} \setminus \{0\}, \cdot)$ は可換群（単位元 $1 = [(1,1)]$、逆元 $(\frac{a}{b})^{-1} = \frac{b}{a}$（$a \neq 0$））
- 分配法則が成立

$\mathbb{Z}$ は環ではあるが体ではありませんでした（$2$ の乗法の逆元が $\mathbb{Z}$ に存在しない）。$\mathbb{Q}$ は $\mathbb{Z}$ の**商体**であり、整域から体を構成する一般的な手続き（分数体の構成）の特殊例です。

**参考文献**：Hungerford, T. W. (1974). *Algebra*. Springer.

---

## 稠密性

**定理**：任意の有理数 $p, q$（$p < q$）に対して、$p < r < q$ を満たす有理数 $r$ が存在する。

証明：$r = \frac{p + q}{2}$ とおきます。$p, q \in \mathbb{Q}$ より $r \in \mathbb{Q}$ であり、$p < r < q$ は明らかです。$\square$

稠密性を繰り返し適用することで、任意の二つの有理数の間に無限個の有理数が存在することがわかります。

しかし、$\mathbb{Q}$ は実数直線を埋め尽くしません。$x^2 = 2$ を満たす有理数は存在しないことが証明でき（$\sqrt{2} \notin \mathbb{Q}$）、有理数には「隙間」があります。この隙間を埋めるのが実数 $\mathbb{R}$ の構成です。

---

## 可算性

**定理**：$\mathbb{Q}$ は可算集合である（$|\mathbb{Q}| = |\mathbb{N}|$）。

証明の概略：正の有理数を格子 $\mathbb{N} \times \mathbb{N}$ の点 $(a, b) \mapsto \frac{a}{b}$ で表します。格子の対角線に沿ってジグザグに列挙し、既約でないもの（既出の有理数）を飛ばすことで、正の有理数と $\mathbb{N}$ の全単射が構成できます。$0$ と負の有理数を交互に挟めば $\mathbb{Q}$ 全体の全単射が得られます。

一方、$\mathbb{R}$ はカントールの対角線論法により非可算です。したがって $\mathbb{R} \setminus \mathbb{Q}$（無理数全体）も非可算であり、「ほとんどの」実数は無理数であるといえます。

**参考文献**：Rudin, W. (1976). *Principles of Mathematical Analysis* (3rd ed.). McGraw-Hill.

---

## 関連ページ

- [分数（標準）](standard.md)
- [負数（専門）](../negative-numbers/professional.md)
- [集合（専門）](../../math-language/sets/professional.md)