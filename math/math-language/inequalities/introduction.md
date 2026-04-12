---
title: 不等号・不等式
description: "大小関係を記号で表す"
tags: [math,math-language,inequalities]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数学の言語
    path: /math/math-language/index.md
  - title: 不等号・不等式
    path: /math/math-language/inequalities/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 等号・等式
    path: /math/math-language/equations/introduction.md
  - title: 負数
    path: /math/numbers/negative-numbers/introduction.md
---

## 「大きい」「小さい」を記号で表す

5 個のりんごと 3 個のみかん、どちらが多いでしょう？\
りんごの方が多い——この「大小関係」を記号で表したのが**不等号**です。

$$5 > 3 \quad \text{（5 は 3 より大きい）}$$
$$3 < 5 \quad \text{（3 は 5 より小さい）}$$

---

## 4 種類の不等号

| 記号 | 意味 | 例 |
|------|------|----|
| $a > b$ | $a$ は $b$ より大きい | $7 > 4$ |
| $a < b$ | $a$ は $b$ より小さい | $2 < 9$ |
| $a \geq b$ | $a$ は $b$ 以上（$b$ と等しいかそれより大きい） | $5 \geq 5$、$6 \geq 5$ |
| $a \leq b$ | $a$ は $b$ 以下（$b$ と等しいかそれより小さい） | $3 \leq 3$、$2 \leq 3$ |

「以上・以下」は「ちょうど等しい場合も含む」ところが「より大きい・より小さい」と違います。

---

## 方程式との違い

方程式 $x + 2 = 5$ の解は $x = 3$ という**1 つの値**でした。

不等式 $x + 2 > 5$ を解くと……\
$x > 3$——「3 より大きい数すべて」が答えです。\
解が 1 つではなく、**範囲**になります。

---

## 大小を変えると何が起きるか

両辺に同じ数を足しても大小は変わりません。

$$3 < 5 \implies 3 + 10 < 5 + 10 \quad (13 < 15)$$

でも、**負の数を掛けると大小が逆転します**。\
なぜかというと、数直線で「$-1$ 倍」すると左右が入れ替わるためです。

$$3 < 5 \implies -3 > -5$$

この「逆転する」という点が不等式の扱いで最も注意が必要なところです。

---

## 関連ページ

- [等号・等式](../equations/introduction.md)
- [必要・十分条件](../conditions/introduction.md)
