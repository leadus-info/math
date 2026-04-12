---
title: 確率
description: "起こりやすさを数値で表す"
tags: [math,statistics]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 統計・確率
    path: /math/statistics/index.md
  - title: 確率
    path: /math/statistics/probability/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 場合の数
    path: /math/statistics/counting/introduction.md
  - title: 分数
    path: /math/numbers/fractions/introduction.md
---

## 「どれくらい起こりやすいか」

コインを投げると、表か裏が出ます。\
どちらが出るかは投げてみるまでわかりません。

でも「たくさん投げたら、だいたい半分ずつ出る」ことは予想できます。\
この「起こりやすさ」を 0 から 1 の数で表したものが**確率**です。

$$\text{確率 0.5} \quad \longleftrightarrow \quad \text{2 回に 1 回くらい起きる}$$

---

## 確率の読み方

| 確率 | 意味 |
|------|------|
| $0$ | 絶対に起きない |
| $0.5$ | 2 回に 1 回くらい |
| $0.9$ | 10 回中 9 回くらい |
| $1$ | 必ず起きる |

天気予報の「降水確率 70%」は「同じような天気の日 100 回のうち 70 回くらい雨が降る」という意味です。

---

## 確率の計算

サイコロを 1 回振るとき、$1$ から $6$ の目が同じくらいの確率で出ます。

$$P(\text{1 が出る}) = \frac{1}{6}$$

$$P(\text{偶数が出る}) = \frac{\text{偶数の目の数}}{\text{全部の目の数}} = \frac{3}{6} = \frac{1}{2}$$

「全部の出方のうち、求めたい出方が何割か」が確率の基本的な考え方です。

---

## 起きない確率

確率が $0.3$ の出来事が「起きない確率」は $1 - 0.3 = 0.7$ です。\
「起きる確率」と「起きない確率」を足すと必ず 1 になります。

「少なくとも 1 回は起きる確率」を求めるとき、\
「1 回も起きない確率」を引く方が計算しやすい場合があります。

---

## 関連ページ

- [場合の数](../counting/introduction.md)
