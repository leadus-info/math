---
title: 分数
description: "分数の四則演算と有理数"
goal: "通分・約分・四則演算・逆数の概念を理解し、分数を自在に計算できるようになる"
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
  - title: 負数（入門）
    path: /math/numbers/negative-numbers/introduction.md
  - title: 分数（入門）
    path: /math/numbers/fractions/introduction.md
---

## 有理数

整数 $a$ と $0$ でない整数 $b$ を使って $\frac{a}{b}$ と書ける数を**有理数**といいます。有理数全体の集合を $\mathbb{Q}$ と書きます。

$$\mathbb{Q} = \left\{ \frac{a}{b} \;\middle|\; a \in \mathbb{Z},\, b \in \mathbb{Z},\, b \neq 0 \right\}$$

整数は $b = 1$ とすれば有理数として書けるので、$\mathbb{Z} \subset \mathbb{Q}$ です。

---

## 分数が等しいとは

分数（入門）で $\frac{1}{2} = \frac{2}{4}$ を見ました。一般に、$\frac{a}{b}$ と $\frac{c}{d}$ が等しいとは、

$$ad = bc$$

が成り立つことです。

**例**：$\frac{3}{4} = \frac{6}{8}$ は $3 \times 8 = 4 \times 6 = 24$ で確認できます。

---

## 約分と既約分数

分母と分子を共通の約数で割ることを**約分**といいます。分母と分子の最大公約数で割ると、これ以上約分できない形になります。この形を**既約分数**といいます。

$$\frac{12}{18} = \frac{12 \div 6}{18 \div 6} = \frac{2}{3}$$

$\gcd(12, 18) = 6$ なので、6で割れば既約分数 $\frac{2}{3}$ になります。

---

## 通分——分母を揃える

分数（入門）では、分母が同じ分数の足し算を見ました。分母が違う場合は、まず分母を同じ数に揃えます。これを**通分**といいます。

$\frac{1}{4}$ と $\frac{1}{6}$ を足してみましょう。$4$ と $6$ の最小公倍数は $12$ なので、分母を $12$ に揃えます。

$$\frac{1}{4} = \frac{1 \times 3}{4 \times 3} = \frac{3}{12}, \quad \frac{1}{6} = \frac{1 \times 2}{6 \times 2} = \frac{2}{12}$$

$$\frac{1}{4} + \frac{1}{6} = \frac{3}{12} + \frac{2}{12} = \frac{5}{12}$$

一般に、

$$\frac{a}{b} + \frac{c}{d} = \frac{ad + bc}{bd}$$

引き算も同様です。

$$\frac{a}{b} - \frac{c}{d} = \frac{ad - bc}{bd}$$

**例**：$\frac{5}{6} - \frac{3}{8}$。最小公倍数は $24$。$\frac{5}{6} = \frac{20}{24}$、$\frac{3}{8} = \frac{9}{24}$。$\frac{20 - 9}{24} = \frac{11}{24}$。

---

## 掛け算

分数の掛け算は、分子同士・分母同士を掛けます。

$$\frac{a}{b} \times \frac{c}{d} = \frac{a \times c}{b \times d}$$

**例**：$\frac{2}{3} \times \frac{3}{5} = \frac{6}{15} = \frac{2}{5}$

---

## 逆数と割り算

$\frac{2}{3}$ に $\frac{3}{2}$ を掛けると $\frac{6}{6} = 1$ になります。このように、掛けると $1$ になるもう一方の数を**逆数**といいます。$\frac{a}{b}$ の逆数は $\frac{b}{a}$ です（$a \neq 0$）。

割り算は、割る数の逆数を掛ける操作です。

$$\frac{a}{b} \div \frac{c}{d} = \frac{a}{b} \times \frac{d}{c} = \frac{ad}{bc} \quad (c \neq 0)$$

なぜ「ひっくり返して掛ける」のか。$\frac{a}{b} \div \frac{c}{d} = x$ とおくと $\frac{a}{b} = x \times \frac{c}{d}$ です。両辺に $\frac{d}{c}$ を掛けると $x = \frac{a}{b} \times \frac{d}{c}$ が得られます。

**例**：$\frac{2}{3} \div \frac{4}{9} = \frac{2}{3} \times \frac{9}{4} = \frac{18}{12} = \frac{3}{2}$

---

## 小数との関係

分数（入門）で、分数と小数は同じ量の別の書き方であることを見ました。

$$\frac{3}{4} = 0.75 \quad \text{（有限小数）}$$
$$\frac{1}{3} = 0.333\ldots = 0.\overline{3} \quad \text{（循環小数）}$$

有理数は必ず有限小数か循環小数のどちらかで表せます（逆も成り立ちます）。

循環小数を分数に戻す方法もあります。$x = 0.\overline{27} = 0.272727\ldots$ とおくと $100x = 27.\overline{27}$ なので $99x = 27$、よって $x = \frac{27}{99} = \frac{3}{11}$。

---

## 関連ページ

- [自然数（標準）](../natural-numbers/standard.md) — 約数・倍数・最大公約数
- [小数（入門）](../decimals/introduction.md)
- [負数（標準）](../negative-numbers/standard.md)