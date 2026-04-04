---
title: 確率
description: "起こりやすさを数値で表す"
tags: [math,statistics]
level: introduction
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 統計・確率
    href: /math/statistics/index.html
  - text: 確率
    href: /math/statistics/probability/introduction.html
levels:
  - level: introduction
  - level: standard
    url: standard.html
  - level: professional
    url: professional.html

requires:
  - title: 場合の数
    url: /math/statistics/counting/introduction
  - title: 分数
    url: /math/numbers/fractions/introduction
---

# 確率
コインを投げると表か裏が出ます。
どちらが出るかは事前にわかりません。
でも「どれくらいの割合で表が出るか」は言えます——$\dfrac{1}{2}$（50%）。

**確率**は、起こりやすさを0から1の数値で表したものです。

---

## 確率とは

全部で同じくらい起こりやすい場合が $n$ 通りあって、
そのうち事象 $A$ が起きる場合が $m$ 通りなら、

$$P(A) = rac{m}{n}$$

サイコロで4が出る確率は $\dfrac{1}{6}$。
52枚のカードからハートを引く確率は $\dfrac{13}{52} = \dfrac{1}{4}$。

---

## 「起きない」確率

「雨が降る確率が30%」なら「雨が降らない確率」は70%。
$P(	ext{起きない}) = 1 - P(	ext{起きる})$

---

## 独立な事象

コインを2回投げるとき、1回目の結果は2回目に影響しません（独立）。
「両方表」の確率は $\dfrac{1}{2} 	imes \dfrac{1}{2} = \dfrac{1}{4}$。

---

## 条件付き確率

「Bが起きたとわかった上でのAの確率」——情報を更新して確率を見直す考え方です。
医療検査の精度評価などで重要です。

---

## 関連ページ

- [場合の数](../counting/introduction.md)
