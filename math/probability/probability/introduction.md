---
title: 確率
description: "起こりやすさを数値で表す"
goal: "確率の意味を理解し、基本的な確率の計算と余事象の考え方を説明できるようになる"
tags: [math,statistics,probability]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 統計・確率
    path: /math/probability/index.md
  - title: 確率
    path: /math/probability/probability/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 場合の数（入門）
    path: /math/probability/counting/introduction.md
---

## 「どれくらい起きやすいか」を数で表す

コインを投げると表か裏が出ます。どちらが出るかは投げてみるまでわかりません。

でも「たくさん投げると、だいたい半分ずつ出る」ことは予想できます。この「起きやすさ」を 0 から 1 の数で表したものが**確率**です。

- 確率 $0$：絶対に起きない
- 確率 $0.5$：2回に1回くらい起きる
- 確率 $1$：必ず起きる

---

## 確率の計算の基本

サイコロを1回振ります。出る目は $1, 2, 3, 4, 5, 6$ の6通りで、それぞれ同じくらい起きやすいとします。

「偶数の目（2, 4, 6）が出る」確率は？

$$P(\text{偶数}) = \frac{\text{偶数の目の数}}{\text{全部の目の数}} = \frac{3}{6} = \frac{1}{2}$$

「全部の起き方のうち、求めたい起き方が何割か」——これが確率の基本です。

---

## 起きない確率

「起きる確率」と「起きない確率」を足すと必ず1になります。

$$P(\text{起きない}) = 1 - P(\text{起きる})$$

「少なくとも1回は起きる確率」を求めるとき、「1回も起きない確率」を引く方が計算しやすい場合があります。

> コインを3回投げて「少なくとも1回は表が出る」確率：\
> $1 - P(\text{3回全部裏}) = 1 - \left(\dfrac{1}{2}\right)^3 = 1 - \dfrac{1}{8} = \dfrac{7}{8}$

---

## まとめ

確率は「起きやすさ」を 0 から 1 の数で表します。「全体の中で求めたい場合が何割か」で計算でき、「起きない確率 = 1 − 起きる確率」という関係が使えます。

---

## 関連ページ

- [場合の数（入門）](../counting/introduction.md)
