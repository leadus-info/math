---
title: 微分
description: "瞬間の変化率を求める操作"
tags: [math,functions,calculus]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数の操作
    path: /math/functions/index.md
  - title: 微分
    path: /math/functions/derivatives/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 極限
    path: /math/functions/limits/introduction.md
---



## 平均の速さから瞬間の速さへ

2時間で100km走ったときの平均の速さは50km/時。

では「今この瞬間の速さ」はどう求めるか？

「1時間の平均」→「1分間の平均」→「1秒間の平均」→「0.001秒間の平均」……
と時間を限りなく短くしていったときの行き着く先が瞬間の速さです。

これが微分の考え方です。

---

## グラフで見ると

グラフ上の2点を結んだ直線の傾きが「平均の変化率」です。
2点を限りなく近づけたとき、その傾きが接線の傾きになります。
この接線の傾きが「瞬間の変化率」です。

---

## 使われ方

物理学では速度・加速度の計算に、
経済学では費用・利益の最大化に、
機械学習では誤差を小さくするパラメータ探索に使われます。

「変化率を知る」必要があるあらゆる場面で使われます。

---

## 関連ページ

- [積分](../integrals/introduction.md)
- [極限](../limits/introduction.md)
