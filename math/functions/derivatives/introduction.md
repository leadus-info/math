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

## 「今この瞬間の速さ」とは何か

車のスピードメーターは「今この瞬間の速さ」を示しています。\
2時間で100km走ったとして、平均は時速50kmですが、\
信号で止まったり高速道路で加速したりと、実際の速さは常に変化しています。

「1時間の平均」→「1分間の平均」→「1秒間の平均」→「0.001秒間の平均」……\
時間を限りなく短くした先の「瞬間の速さ」——これが**微分**の考え方です。

---

## グラフで見ると

2点を結んだ直線の傾きが「平均の変化率」です。

2点を限りなく近づけていくと、この直線は最終的にグラフに接する直線（**接線**）になります。\
接線の傾きが「瞬間の変化率（微分係数）」です。

---

## 増減の情報を得る

微分は「どこで増えてどこで減るか」を教えてくれます。

- 傾きが正（上り坂） → その点で関数は増加している
- 傾きが負（下り坂） → その点で関数は減少している
- 傾きがゼロ（水平） → 山の頂上か谷の底の候補

これで「最大値・最小値がどこか」を探せます。

---

## 使われ方

- **物理**：速度・加速度・電流の変化率
- **経済**：「あと1個作ると収益がどれだけ増えるか」（限界費用・限界収入）
- **機械学習**：誤差を最小にするパラメータの探索方向

「変化率を知りたい」すべての場面で使われます。

---

## 関連ページ

- [極限](../limits/introduction.md) — 微分の定義の基礎
- [積分](../integrals/introduction.md) — 微分の逆操作
