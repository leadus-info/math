---
title: 微分
description: "瞬間の変化率を求める操作"
tags: [math,functions,calculus]
level: introduction
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数の操作
    href: /math/functions/calculus/index.html
  - text: 微分
    href: /math/functions/calculus/derivatives/introduction.html
levels:
  - level: introduction
  - level: standard
    url: standard.html
  - level: professional
    url: professional.html

requires:
  - title: 極限
    url: /math/functions/calculus/limits/introduction
---

# 微分
車のスピードメーターは「今この瞬間の速さ」を表しています。
2時間で100km走ったとしても、ずっと同じ速さだったわけではありません。

**微分**は、この「瞬間の変化の速さ」を求める操作です。

---

## 平均の速さから瞬間の速さへ

2時間で100km走ったときの平均の速さは50km/時。

でも「今この瞬間の速さ」を求めるには？

「1時間の平均」→「1分間の平均」→「1秒間の平均」→「0.001秒間の平均」…
と時間を限りなく短くしていったときの「行き着く先」が瞬間の速さです。

これが**微分の考え方**です。

---

## グラフで見ると

グラフ上の2点を結んだ直線の傾きが「平均の変化率」。
2点を限りなく近づけたときの「行き着く傾き」が**接線**で、
その傾きが「瞬間の変化率」（微分係数）です。

---

## 微分の使われ方

- 物理：速度・加速度・力の計算
- 経済：費用・利益の最大化（最適化）
- 機械学習：誤差を最小にするパラメータ探索
- 工学：設計の最適化

「変化率を知る」必要があるあらゆる場面で使われます。

---

## 関連ページ

- [積分](../integrals/introduction.md) — 微分の逆操作
- [極限](../limits/introduction.md)
