---
title: 統計
description: "データから母集団の性質を推測する"
goal: "統計が「標本から母集団を推測する学問」であることを理解し、平均・分散・ヒストグラムの意味を説明できるようになる"
tags: [math,probability,statistics]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 確率
    path: /math/probability/index.md
  - title: 統計
    path: /math/probability/statistics/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 確率（入門）
    path: /math/probability/probability/introduction.md
---

## データから「全体」を知りたい

日本全国の有権者の支持率を調べるとき、1億人全員に聞くのは現実的でありません。\
1000人に聞いた結果から、全体を推測する——これが**統計**のやっていることです。

- **母集団**：知りたい対象全体（全有権者）
- **標本**：実際に調べた一部（1000人）

標本から母集団の性質を推測することを**統計的推測**といいます。

---

## データを要約する

まずデータの特徴を数値でまとめます。

**平均**：データの合計 ÷ 個数——「真ん中あたり」を表します。

**中央値**：データを並べたときの真ん中の値——極端な値の影響を受けにくい。

**分散・標準偏差**：データのばらつき具合——小さいほど平均の近くに集まっている。

---

## ヒストグラム

データの分布の形を視覚的に確認できます。\
山が1つか2つか、左右対称か偏っているか——形によって適切な分析方法が変わります。

---

## 相関

2つの量の間に「一方が増えると他方も増える」傾向があるとき、**正の相関**があるといいます。

身長と体重、勉強時間と試験の点数——相関は「関係の強さ」を数値で表します。

ただし「相関があること」は「原因と結果の関係がある」ことを意味しません。

---

## 関連ページ

- [確率（入門）](../probability/introduction.md)
- [確率分布（入門）](../distributions/introduction.md)
