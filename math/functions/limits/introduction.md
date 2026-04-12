---
title: 極限
description: "「限りなく近づく」とはどういうことか"
tags: [math,functions,calculus]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数の操作
    path: /math/functions/index.md
  - title: 極限
    path: /math/functions/limits/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 数列
    path: /math/functions/sequences/introduction.md
---

## 「限りなく近づく」とは

$\frac{1}{10} = 0.1$、$\frac{1}{100} = 0.01$、$\frac{1}{1000} = 0.001$……\
数を大きくするほど $\frac{1}{n}$ は 0 に近づいていきます。\
でも 0 にはなりません。

この「どこまでも近づいていく先」を**極限**といいます。

---

## 走れば追いつく

「アキレスが亀の10倍の速さで走っても追いつけない」\
というパラドックスがあります。

アキレスが10m進む間に亀は1m進み、\
その1m進む間に亀は0.1m進み……と無限に続くように見えます。

でも実際には追いつきます。\
$10 + 1 + 0.1 + 0.01 + \ldots$ という無限の和は、有限の距離になるからです。\
**無限個を足しても、有限の値になることがある**——これが極限の核心です。

---

## 近づく先がない場合

$1, 4, 9, 16, 25, \ldots$ は限りなく大きくなるばかりで、\
どこか一点に近づいていくわけではありません。\
こういう場合を「発散する」といいます。

---

## なぜ重要か

瞬間の速さ（微分）も、曲線の下の面積（積分）も、\
どちらも「無限に細かくしていった先の値」として定義されます。\
極限はその土台となる考え方です。

---

## 関連ページ

- [数列](../sequences/introduction.md)
- [微分](../derivatives/introduction.md)
- [積分](../integrals/introduction.md)
