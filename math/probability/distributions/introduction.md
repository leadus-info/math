---
title: 確率分布
description: "確率変数の値の広がり方"
goal: "確率変数と確率分布の意味を理解し、正規分布・二項分布の形と使いどころを説明できるようになる"
tags: [math,probability,distributions]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 確率
    path: /math/probability/index.md
  - title: 確率分布
    path: /math/probability/distributions/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 確率（標準）
    path: /math/probability/probability/standard.md
---

## 「何が出るか」を関数で表す

サイコロを1回振ったとき、出る目 $X$ は $1$ から $6$ のどれかです。\
各値の出やすさをまとめると：

| $X$ | 1 | 2 | 3 | 4 | 5 | 6 |
|-----|---|---|---|---|---|---|
| 確率 | $\frac{1}{6}$ | $\frac{1}{6}$ | $\frac{1}{6}$ | $\frac{1}{6}$ | $\frac{1}{6}$ | $\frac{1}{6}$ |

このように「確率変数の値とその確率の対応」を**確率分布**といいます。

---

## 期待値——平均的な値

サイコロの目の「長い目で見た平均」はいくつでしょうか。

$$E[X] = 1 \times \frac{1}{6} + 2 \times \frac{1}{6} + \cdots + 6 \times \frac{1}{6} = \frac{21}{6} = 3.5$$

「値 × その確率」を全部足したものが**期待値**（平均）です。

---

## 二項分布——成功・失敗の繰り返し

コインを10回投げて表が出る回数 $X$ の分布が**二項分布**です。

- 各回の結果は独立
- 毎回「表（成功）か裏（失敗）」の2択
- 表の出る確率は毎回同じ

「10回中ちょうど3回表が出る確率」のような問いに答えられます。

---

## 正規分布——釣り鐘型の分布

身長・テストの点数・測定誤差——自然界や社会の多くの量が従う分布が**正規分布**です。

左右対称の釣り鐘型で、平均のあたりに最も多く集まり、離れるほど少なくなります。

「偏差値」は正規分布を使って計算されています。

---

## 関連ページ

- [確率（標準）](../probability/standard.md)
- [場合の数（標準）](../counting/standard.md)
