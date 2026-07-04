---
title: 有理数
description: "分数で表せる数"
goal: "有理数の定義を理解し、循環小数を分数に変換できるようになる"
tags: [math, numbers, real-numbers]
stage: 中級編
subject: 数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 中級編
    path: /math/intermediate/index.md
  - title: 有理数
    path: /math/intermediate/numbers/rational-numbers.md
requires:
  - title: 有理数と無理数
    path: rational-irrational.md
---

## 有理数の定義

整数 $a$ と $0$ でない整数 $b$ を使って $\dfrac{a}{b}$ と書ける数を**有理数**といいます。整数はすべて $b=1$ の場合として有理数に含まれ、有限小数・循環小数もすべて有理数です。

---

## 循環小数を分数に変換する

循環小数は、次のような計算で分数に戻すことができます。

$x = 0.\overline{27} = 0.272727\ldots$ とおきます。繰り返す桁数が2桁なので、両辺を100倍します。

$$100x = 27.272727\ldots$$

ここから元の式を引くと、小数部分がちょうど打ち消し合います。

$$100x - x = 27.272727\ldots - 0.272727\ldots$$
$$99x = 27$$
$$x = \frac{27}{99} = \frac{3}{11}$$

一般に、循環する部分の桁数が $n$ 桁なら $10^n$ を掛けてから元の式を引くことで、分数に変換できます。

**例**：$x = 0.1\overline{6} = 0.1666\ldots$ を分数にする。$10x = 1.666\ldots$、$100x = 16.666\ldots$ なので $100x - 10x = 15$、$90x = 15$、$x = \dfrac{15}{90} = \dfrac{1}{6}$。

---

## まとめ

有理数は整数の比 $\dfrac{a}{b}$ で表せる数です。循環小数は、桁をずらして引き算をすることで必ず分数に変換できます。

---

## 関連ページ

- [有理数と無理数（中級編）](rational-irrational.md)
- [無理数（中級編）](irrational-numbers.md)
