---
title: 分数
description: "割り切れないときに使う数と割り算"
tags: [math,numbers,fractions]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 数
    path: /math/numbers/index.html
  - title: 分数
    path: /math/numbers/fractions/standard.html
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
  - title: 負数
    path: /math/numbers/negative-numbers/introduction
---




> この記事は [入門](introduction.md) の続きです。先に入門を読むことを推奨します。

1 個のケーキを 3 人で等しく分けると、1 人の分は「3 分の 1」です。  
[自然数](professional.md)の章で見たように、「5 割る 2」は自然数の中では答えが出ません。  
この「割り切れない」を解決するために分数を導入します。

## このページで扱うこと
- 割り算（除法）の定義
- 分数の意味と書き方
- 約分・通分
- 分数の四則演算

---

## 割り算（除法）

「$a$ を $b$ 個に等分したときの 1 つ分」が割り算の意味です。

$$6 \div 2 = 3 \quad \text{（6 を 2 等分すると 3）}$$

自然数の中では割り切れないことがあります。

$$5 \div 2 = \ ? \quad \text{（自然数の中に答えがない）}$$

この答えを表すために**分数**を使います。

$$5 \div 2 = \frac{5}{2}$$

---

## 分数とは

$$\frac{a}{b} \quad (b \neq 0)$$

上の数 $a$ を**分子**、下の数 $b$ を**分母**といいます。  
$\frac{3}{4}$ は「4 等分したうちの 3 つ分」、つまり $3 \div 4$ の答えです。

---

## 約分

分子と分母を同じ数で割っても、値は変わりません。

$$\frac{12}{18} = \frac{12 \div 6}{18 \div 6} = \frac{2}{3}$$

これを**約分**といいます。これ以上約分できない形を**既約分数**といいます。

---

## 通分（分母を揃える）

分母が違う分数を足したり引いたりするには、分母を揃える**通分**が必要です。

$$\frac{1}{4} + \frac{1}{6} = \frac{3}{12} + \frac{2}{12} = \frac{5}{12}$$

---

## 分数の掛け算・割り算

**掛け算**：分子どうし、分母どうしをそれぞれ掛けます。

$$\frac{a}{b} \times \frac{c}{d} = \frac{a \times c}{b \times d}$$

**割り算**：割る分数をひっくり返して掛けます。

$$\frac{a}{b} \div \frac{c}{d} = \frac{a}{b} \times \frac{d}{c} = \frac{a \times d}{b \times c}$$

---

## 小数との関係

分数は小数で表すこともできます。

$$\frac{3}{4} = 0.75, \quad \frac{1}{3} = 0.333\ldots$$

$\frac{1}{3}$ のように割り切れない場合、小数は永遠に続きます（**循環小数**）。  
詳しくは[小数](professional.md)で扱います。

---

## 関連ページ

- [小数](professional.md) — 分数の別の書き方
- [負数](professional.md) — 負の分数（$-\frac{3}{4}$ など）
- [乗法・べき乗](professional.md) — 掛け算をさらに詳しく
- [分数（専門）](professional.md) — 有理数の代数的構造
