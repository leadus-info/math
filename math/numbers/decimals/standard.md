---
title: 小数
description: "分数を小数点で表す"
difficulty: 1
tags: [math,numbers,decimals]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数
    href: /math/numbers/index.html
  - text: 小数
    href: /math/numbers/decimals/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---




# 小数
$0.5$、$3.14$、$0.333\ldots$——小数点を使って表す数が**小数**です。
分数と同じ量を、別の書き方で表したものです。

## このページで扱うこと
- 小数の仕組み
- 有限小数と無限小数の違い
- 分数との行き来

## 前提知識
- [自然数](../natural-numbers/standard.md)
- [分数](../fractions/standard.md)

---

## 小数の仕組み

小数点の右は「$\frac{1}{10}$の桁」「$\frac{1}{100}$の桁」と続きます。

$$3.14 = 3 + \frac{1}{10} + \frac{4}{100}$$

つまり「整数部 $3$」に「$10$ 分の $1$ の桁が $1$ つ分」と「$100$ 分の $1$ の桁が $4$ つ分」を足した数です。

---

## 3 種類の小数

| 種類 | 例 | どんな数？ |
|------|----|-----------|
| 有限小数 | $0.75$ | 桁数が有限で終わる |
| 循環小数 | $0.333\ldots = 0.\overline{3}$ | 同じパターンが繰り返す |
| 無限不循環小数 | $3.14159\ldots$（$\pi$） | 永遠に続き、繰り返しもない |

有限小数・循環小数は分数で表せます（**有理数**）。
$\pi$ や $\sqrt{2}$ のような無限不循環小数は分数では表せません（**無理数**）。

---

## 分数 → 小数

割り算をするだけです。

$$\frac{3}{4} = 3 \div 4 = 0.75$$

---

## 小数 → 分数（循環小数の場合）

$x = 0.\overline{27}$ を分数に直す方法：

$$x = 0.272727\ldots$$
$$100x = 27.272727\ldots$$
$$100x - x = 27$$
$$99x = 27 \implies x = \frac{27}{99} = \frac{3}{11}$$

---

## 数の広がり

$$\text{自然数} \subset \text{整数} \subset \text{有理数} \subset \text{実数}$$

実数 = 有理数（分数で表せる）＋ 無理数（分数で表せない）

---

## 関連ページ

- [分数](../fractions/standard.md)
- [負数](../negative-numbers/standard.md)
- [小数（発展）](../decimals/advanced.md) — より詳しく学ぶ
