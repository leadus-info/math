---
title: 小数
description: "小数の演算・分数との変換・数の体系"
goal: "小数と分数の相互変換、小数の四則演算、有理数と無理数の区別を理解し、数の体系の全体像を説明できるようになる"
tags: [math,numbers,decimals]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 小数
    path: /math/numbers/decimals/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 分数（標準）
    path: /math/numbers/fractions/standard.md
  - title: 小数（入門）
    path: /math/numbers/decimals/introduction.md
---

## 分数から小数への変換

分数を小数に変換するには、分子を分母で割ります。

$$\frac{3}{8} = 3 \div 8 = 0.375$$

割り算の余りが $0$ になれば有限小数、余りが繰り返し始めれば循環小数です。

分母を素因数分解したとき、$2$ と $5$ 以外の素因数を含まなければ有限小数になります。

**例**：$\frac{3}{8}$。$8 = 2^3$ なので有限小数。$\frac{1}{6}$。$6 = 2 \times 3$ で $3$ を含むので循環小数（$0.1\overline{6}$）。

---

## 循環小数から分数への変換

循環小数を分数に戻す方法があります。

$x = 0.\overline{27} = 0.272727\ldots$ とおきます。繰り返す桁数が2桁なので $100$ を掛けます。

$$100x = 27.272727\ldots$$

元の式を引くと、

$$100x - x = 27, \quad 99x = 27, \quad x = \frac{27}{99} = \frac{3}{11}$$

一般に、循環する部分の桁数が $n$ なら $10^n$ を掛けて引き算します。

---

## 小数の四則演算

小数の足し算・引き算は、小数点の位置を揃えて計算します。

$$1.25 + 0.3 = 1.25 + 0.30 = 1.55$$

掛け算は、小数点を無視して整数として掛け、小数点以下の桁数の合計だけ小数点を戻します。

$$1.2 \times 0.03 = 12 \times 3 \times \frac{1}{10} \times \frac{1}{100} = 36 \times \frac{1}{1000} = 0.036$$

割り算は、割る数が整数になるまで両方の小数点をずらします。

$$1.44 \div 1.2 = 14.4 \div 12 = 1.2$$

---

## 無理数

小数（入門）で、無限不循環小数は分数で表せないことを見ました。このような数を**無理数**といいます。

$\sqrt{2}$ が無理数であることは、背理法で示せます。$\sqrt{2} = \frac{a}{b}$（既約分数）と仮定すると $2b^2 = a^2$ であり、$a$ は偶数です。$a = 2k$ とおくと $2b^2 = 4k^2$、$b^2 = 2k^2$ で $b$ も偶数。これは既約分数の仮定に矛盾します。

---

## 数の体系

ここまでに登場した数の包含関係をまとめます。

$$\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R}$$

- $\mathbb{N}$（自然数）：$1, 2, 3, \ldots$
- $\mathbb{Z}$（整数）：自然数に $0$ と負数を加えたもの
- $\mathbb{Q}$（有理数）：整数の比 $\frac{a}{b}$ で表せる数。有限小数と循環小数。
- $\mathbb{R}$（実数）：有理数と無理数を合わせたもの。数直線上のすべての点。

有理数だけでは数直線に「穴」があります（$\sqrt{2}$ の位置に有理数はない）。無理数を加えて穴を埋めたものが実数です。

---

## 関連ページ

- [分数（標準）](../fractions/standard.md)
- [負数（標準）](../integers/standard.md)