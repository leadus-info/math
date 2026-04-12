---
title: 分数
description: "分数の演算規則と有理数"
goal: "分数の四則演算を正確に行い、有理数が除法について閉じていることを説明できるようになる"
tags: [math,numbers,fractions]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 分数
    path: /math/numbers/fractions/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 自然数（標準）
    path: /math/numbers/natural-numbers/standard.md
  - title: 負数（標準）
    path: /math/numbers/negative-numbers/standard.md
  - title: 分数
    path: /math/numbers/fractions/introduction.md
---

## 有理数の定義

整数 $a$ と $0$ でない整数 $b$ に対して、$\frac{a}{b}$ を**分数**と呼びます。分数全体の集合を**有理数**といいます。

$$\mathbb{Q} = \left\{ \frac{a}{b} \;\middle|\; a \in \mathbb{Z},\, b \in \mathbb{Z} \setminus \{0\} \right\}$$

整数は $b = 1$ とすれば有理数とみなせるので $\mathbb{Z} \subset \mathbb{Q}$ です。

---

## 分数の相等と約分

$\frac{a}{b}$ と $\frac{c}{d}$ が等しいとは $ad = bc$ が成り立つことです。

$$\frac{2}{4} = \frac{1}{2} \quad (2 \times 2 = 4 \times 1)$$

$\gcd(a, b) = 1$ のとき $\frac{a}{b}$ を**既約分数**といいます。任意の分数は分母と分子を最大公約数で割ることで、既約分数に一意に変形できます。

$$\frac{12}{18} = \frac{12 \div 6}{18 \div 6} = \frac{2}{3} \quad (\gcd(12,18)=6)$$

---

## 加法・減法（通分）

分母が異なる分数を足すには、分母を揃えます（**通分**）。

$$\frac{a}{b} + \frac{c}{d} = \frac{ad + bc}{bd}$$

**例**：$\frac{1}{4} + \frac{1}{6}$

最小公倍数 $\text{lcm}(4,6) = 12$ を使うと

$$\frac{1}{4} = \frac{3}{12}, \quad \frac{1}{6} = \frac{2}{12}, \quad \frac{1}{4} + \frac{1}{6} = \frac{3 + 2}{12} = \frac{5}{12}$$

減法も同様です。$\frac{5}{6} - \frac{3}{8} = \frac{20}{24} - \frac{9}{24} = \frac{11}{24}$。

---

## 乗法

分数の掛け算は分子同士・分母同士を掛けます。

$$\frac{a}{b} \times \frac{c}{d} = \frac{ac}{bd}$$

**例**：$\frac{2}{3} \times \frac{5}{7} = \frac{10}{21}$

---

## 除法と逆数

$\frac{a}{b}$（$a \neq 0$）に対して、$\frac{a}{b} \times \frac{b}{a} = 1$ を満たす $\frac{b}{a}$ を**逆数**といいます。

分数の割り算は、割る数の逆数を掛けることで定義します。

$$\frac{a}{b} \div \frac{c}{d} = \frac{a}{b} \times \frac{d}{c} = \frac{ad}{bc} \quad (c \neq 0)$$

**なぜひっくり返して掛けるか？** $\frac{a}{b} \div \frac{c}{d} = x$ とおくと $x \times \frac{c}{d} = \frac{a}{b}$ です。両辺に $\frac{d}{c}$ を掛けると $x = \frac{a}{b} \times \frac{d}{c}$ が得られます。

**例**：$\frac{2}{3} \div \frac{4}{9} = \frac{2}{3} \times \frac{9}{4} = \frac{18}{12} = \frac{3}{2}$

逆数の存在により、$\mathbb{Q}$ では $0$ 以外による除法が常に可能です。自然数では割り算が閉じていませんでしたが、有理数では閉じています。

---

## 小数との関係

**定理**：有理数は有限小数または循環小数として表せます（逆も成立）。

$\frac{3}{4} = 0.75$（有限小数）、$\frac{1}{3} = 0.333\ldots = 0.\overline{3}$（循環小数）

**循環小数→分数の変換例**：$x = 0.\overline{27} = 0.272727\ldots$ とおくと $100x = 27.\overline{27}$ なので $99x = 27$、よって $x = \frac{27}{99} = \frac{3}{11}$。

---

## 関連ページ

- [小数](../decimals/introduction.md)
- [負数（標準）](../negative-numbers/standard.md)
- [自然数（標準）](../natural-numbers/standard.md)