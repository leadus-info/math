---
title: 分数の割り算
description: "割る数の逆数を掛ける"
goal: "逆数の意味を理解し、分数÷整数、分数÷分数の計算ができるようになる"
tags: [math, numbers, fractions]
stage: 初級編
subject: 数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 初級編
    path: /math/beginner/index.md
  - title: 分数の割り算
    path: /math/beginner/numbers/fractions-division.md
requires:
  - title: 分数の掛け算
    path: fractions-multiplication.md
---

## 逆数

$\frac{2}{3}$ の分母と分子を入れ替えた $\frac{3}{2}$ を、$\frac{2}{3}$ の**逆数**といいます。ある分数とその逆数を掛けると、必ず1になります。

$$\frac{2}{3} \times \frac{3}{2} = \frac{6}{6} = 1$$

整数の逆数を考えるときは、整数を「分母が1の分数」とみなします。$3 = \frac{3}{1}$ の逆数は $\frac{1}{3}$ です。

---

## 分数÷整数

「$\frac{4}{5}\text{L}$ のジュースを2人で等しく分けると、1人分は？」

$$\frac{4}{5} \div 2$$

割る数の逆数を掛けると、割り算を掛け算に直せます。$2$ の逆数は $\frac{1}{2}$ なので、

$$\frac{4}{5} \div 2 = \frac{4}{5} \times \frac{1}{2} = \frac{4}{10} = \frac{2}{5}$$

---

## 分数÷分数

「$\frac{2}{3}\text{m}$ の棒の重さが $\frac{4}{5}\text{kg}$ のとき、1mあたりの重さは？」

$$\frac{4}{5} \div \frac{2}{3}$$

割る数 $\frac{2}{3}$ の逆数 $\frac{3}{2}$ を掛けます。

$$\frac{4}{5} \div \frac{2}{3} = \frac{4}{5} \times \frac{3}{2} = \frac{12}{10} = \frac{6}{5}$$

一般に、

$$\frac{a}{b} \div \frac{c}{d} = \frac{a}{b} \times \frac{d}{c} = \frac{a \times d}{b \times c}$$

なぜ「ひっくり返して掛ける」のか——$\frac{a}{b} \div \frac{c}{d} = x$ とおくと、$\frac{a}{b} = x \times \frac{c}{d}$ です。両辺に $\frac{d}{c}$ を掛けると、右辺は $x \times \frac{c}{d} \times \frac{d}{c} = x \times 1 = x$ となり、$x = \frac{a}{b} \times \frac{d}{c}$ が得られます。

---

## まとめ

分数の割り算は、割る数の逆数を掛ける操作に直せます。整数で割るときは、その整数を分母1の分数とみなして同じように計算できます。

---

## 関連ページ

- [分数の掛け算（初級編）](fractions-multiplication.md)
- [分数（初級編）](fractions.md)
