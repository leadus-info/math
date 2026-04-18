---
title: ベクトル
description: "大きさと向きを持つ量"
goal: "ベクトルが「大きさと向きを持つ量」であることを理解し、足し算とスカラー倍の意味を説明できるようになる"
tags: [math,linear-algebra,vectors]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 線形代数
    path: /math/linear-algebra/index.md
  - title: ベクトル
    path: /math/linear-algebra/vectors/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 点（入門）
    path: /math/geometry/point/introduction.md
---

## 大きさだけでは足りない

「時速60kmで進む」という情報だけでは、どこに向かっているかわかりません。「北向きに時速60kmで進む」——**方向**があって初めて移動が定まります。

このように「大きさ」と「向き」の両方を持つ量を**ベクトル**といいます。力・速度・変位などがベクトルです。

---

## 矢印で表す

ベクトルは矢印で表します。矢印の長さが大きさ、矢印の向きが方向です。

「東へ3km、北へ4km」という移動を表すベクトルは、右に3・上に4の矢印です。

---

## 足し算——矢印をつなぐ

「東へ3km進み、次に北へ4km進む」——2つの移動を合わせた結果は？

最初の矢印の先から2番目の矢印を続けて引き、始点から終点へ引いた矢印が答えです。「右3・上4」という1つの移動で同じ場所に着きます。

---

## どれだけ同じ向きを向いているか——内積

2つのベクトルが同じ方向を向いているとき、「一致度」は高い。垂直なとき「一致度」はゼロ。この「どれだけ同じ向きか」を数値で表すのが**内積**です。

内積がゼロ → 2つのベクトルは**直交（垂直）**

---

## まとめ

ベクトルは大きさと向きを持つ量です。矢印で表し、「矢印をつなぐ」ことで足し算が定義されます。内積は2つのベクトルの「方向の一致度」を数値化し、直交判定などに使われます。

---

## 関連ページ

- [行列（入門）](../matrices/introduction.md)
- [点（入門）](../../geometry/point/introduction.md)
