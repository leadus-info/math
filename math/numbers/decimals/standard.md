---
title: 小数
description: "分数を 10 の積み重ねで表す"
tags: [math,numbers,decimals]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 数
    path: /math/numbers/index.html
  - title: 小数
    path: /math/numbers/decimals/standard.html
levels:
  - level: 入門
    path: introduction.html
  - level: 標準
  - level: 専門
    path: professional.html
level: 標準
requires:
  - title: 自然数
    path: /math/numbers/natural-numbers/introduction
  - title: 分数
    path: /math/numbers/fractions/introduction
---

## このページで扱うこと

「0.5」や「3.14」——小数点を使って表す数が**小数**です。
分数と同じ量を、別の書き方で表したものです。

- 小数の仕組み
- 有限小数・循環小数・割り切れない小数
- 分数との変換

---

## 小数の仕組み

小数点の右の桁は、10 分の 1、100 分の 1……と続きます。

$$3.14 = 3 + \frac{1}{10} + \frac{4}{100}$$

---

## 3 種類の小数

| 種類 | 例 | 特徴 |
|------|----|------|
| 有限小数 | $0.75$ | いつか終わる |
| 循環小数 | $0.333\ldots$ | 同じ数字が繰り返す |
| 無限不循環小数 | $3.14159\ldots$ (円周率) | 永遠に繰り返さない |

有限小数と循環小数は分数で表せます。
円周率 $\pi$ や $\sqrt{2}$ は分数では表せません（**無理数**）。

---

## 分数 → 小数

割り算をするだけです。

$$\frac{3}{4} = 3 \div 4 = 0.75$$

---

## 循環小数 → 分数

$x = 0.\overline{27}$ とおくと、

$$100x = 27.\overline{27} \implies 99x = 27 \implies x = \frac{27}{99} = \frac{3}{11}$$

---

## 数の広がり

$$\text{自然数} \subset \text{整数} \subset \text{有理数} \subset \text{実数}$$

---

## 関連ページ

- [分数](professional.md)
- [負数](professional.md)
- [小数（専門）](professional.md) — 実数の厳密な構成
