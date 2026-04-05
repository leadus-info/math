---
title: 分数
description: "割り切れないときに使う数と割り算"
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
  - title: 自然数
    path: /math/numbers/natural-numbers/introduction.md
  - title: 負数
    path: /math/numbers/negative-numbers/introduction.md
---

## 有理数の定義

整数 $a$ と $0$ でない整数 $b$ の組 $(a, b)$ に対して\
$(a, b) \sim (c, d) \iff ad = bc$\
という同値関係を定め、同値類を**分数** $\frac{a}{b}$ と書きます。

$$\mathbb{Q} = \left\{ \frac{a}{b} \;\middle|\; a \in \mathbb{Z},\, b \in \mathbb{Z} \setminus \{0\} \right\}$$

この集合を**有理数**といいます。$\mathbb{Z} \subset \mathbb{Q}$（整数は $b=1$ とすれば有理数）。

---

## 約分と既約分数

**定義**：$\frac{a}{b}$ と $\frac{c}{d}$ が等しいとは $ad = bc$ が成り立つことです。

$\gcd(a, b) = 1$ のとき $\frac{a}{b}$ を**既約分数**といいます。\
任意の分数は約分によって既約分数に一意に変形できます。

$$\frac{12}{18} = \frac{12 \div 6}{18 \div 6} = \frac{2}{3} \quad (\gcd(12,18)=6)$$

---

## 四則演算

**加法・減法**（通分して計算）：

$$\frac{a}{b} + \frac{c}{d} = \frac{ad + bc}{bd}$$

**例**：$\frac{1}{4} + \frac{1}{6} = \frac{6 + 4}{24} = \frac{10}{24} = \frac{5}{12}$

**乗法**：

$$\frac{a}{b} \times \frac{c}{d} = \frac{ac}{bd}$$

**除法**：割る数の逆数を掛けます。

$$\frac{a}{b} \div \frac{c}{d} = \frac{a}{b} \times \frac{d}{c} = \frac{ad}{bc} \quad (c \neq 0)$$

**なぜひっくり返して掛けるか？**\
$\frac{a}{b} \div \frac{c}{d} = x$ とおくと $\frac{a}{b} = x \times \frac{c}{d}$。\
両辺に $\frac{d}{c}$ を掛けると $x = \frac{a}{b} \times \frac{d}{c}$。

---

## 有理数の稠密性

任意の二つの有理数 $p < q$ の間には、必ず別の有理数が存在します。

**証明**：$\frac{p+q}{2} \in \mathbb{Q}$ であり、$p < \frac{p+q}{2} < q$。

これを稠密性といいます。つまり有理数はどこまでも「隙間なく」並んでいます。\
しかし実は有理数では埋まらない「穴」があり、それが無理数です（$\sqrt{2} \notin \mathbb{Q}$）。

---

## 小数との関係

**定理**：有理数は有限小数または循環小数として表せます（逆も成立）。

$\frac{3}{4} = 0.75$（有限小数）、$\frac{1}{3} = 0.333\ldots = 0.\overline{3}$（循環小数）

**循環小数→分数の変換例**：\
$x = 0.\overline{27} = 0.272727\ldots$ とおくと\
$100x = 27.\overline{27}$ なので $99x = 27$、よって $x = \frac{27}{99} = \frac{3}{11}$。

---

## 例題

**例題1**：$\frac{5}{6} - \frac{3}{8}$ を計算してください。\
最小公倍数は $\text{lcm}(6,8) = 24$。\
$\frac{5}{6} = \frac{20}{24}$、$\frac{3}{8} = \frac{9}{24}$ なので $\frac{20-9}{24} = \frac{11}{24}$。

**例題2**：$\frac{2}{3} \div \frac{4}{9}$ を計算してください。\
$\frac{2}{3} \times \frac{9}{4} = \frac{18}{12} = \frac{3}{2}$。

---

## 関連ページ

- [小数](../decimals/introduction.md)
- [負数](../negative-numbers/introduction.md)
