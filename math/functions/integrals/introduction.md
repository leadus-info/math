---
title: 積分
description: "細かく分けて足し合わせる操作"
tags: [math,functions,calculus]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数の操作
    path: /math/functions/index.md
  - title: 積分
    path: /math/functions/integrals/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 微分
    path: /math/functions/derivatives/introduction.md
  - title: 極限
    path: /math/functions/limits/introduction.md
---

## 曲線で囲まれた面積

三角形や長方形の面積なら公式で求められます。\
では、こんな形は？

```
    ___
   /   \
  /     \
 /       \
/         \
```

曲線で囲まれた面積を求めるのが**積分**のもとになったアイデアです。

---

## 細かく分けて足し合わせる

曲線の下を細い長方形で埋めることを考えます。

```
│▓│▓│▓│▓│▓│▓│▓│
│▓│▓│▓│▓│▓│▓│▓│
│▓│▓│▓│▓│▓│▓│▓│
└─┴─┴─┴─┴─┴─┴─┘
```

長方形が粗いうちは近似が荒いですが、\
細くすればするほど正確な面積に近づきます。\
「無限に細かくした先の値」が積分です。

---

## 速さと距離の関係

時速60kmで2時間走れば120km進みます。\
でも速さが一定でない場合は？

速さのグラフを描いて、その「下の面積」を求めると距離になります。\
積分は「累積した量を求める」操作です。

---

## 微分と積分は逆操作

「速さを積分すると距離」「距離を微分すると速さ」——\
分解する（微分）と積み上げる（積分）は逆の操作です。\
これが微積分学の最も重要な発見です。

---

## 関連ページ

- [微分](../derivatives/introduction.md)
- [極限](../limits/introduction.md)
