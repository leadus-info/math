---
title: 積分
description: "ルベーグ積分・広義積分・多重積分"
tags: [math,operations,integrals]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 関数の操作
    path: /math/functions/index.html
  - title: 積分
    path: /math/functions/integrals/professional.html
levels:
  - level: introduction
    path: introduction.html
  - level: standard
    path: standard.html
  - level: professional
level: professional
requires:
  - title: 積分
    path: /math/functions/integrals/introduction
  - title: 微分（専門）
    path: ../derivatives/professional.md
  - title: 集合（専門）
    path: ../../../math-language/sets/professional.md
---



> この記事は [標準](standard.md) の続きです。先に標準を読むことを推奨します。

ルベーグ積分・多重積分・線積分・曲面積分を扱います。

## このページで扱うこと
- ルベーグ積分の動機と構成
- 多重積分とフビニの定理
- 線積分・曲面積分とストークスの定理

---

## ルベーグ積分の動機

リーマン積分は「縦に切る」——ルベーグ積分は「横に切る」発想です。

$$\int f\,d\mu = \int_0^{\infty} \mu(\{x : f(x) > t\})\,dt$$

点ごとの収束に対して積分と極限の交換が保証されます（**優収束定理**）。

---

## フビニの定理

$$\int_{A \times B} f(x,y)\,d(x,y) = \int_A\left(\int_B f(x,y)\,dy\right)dx$$

（適切な可測性・可積分性のもとで）

---

## 変数変換公式

$$\int_{\phi(U)} f\,dy = \int_U (f \circ \phi)|\det J\phi|\,dx$$

**例（極座標）**: $\iint f(x,y)\,dxdy = \iint f(r\cos\theta, r\sin\theta)\,r\,dr\,d\theta$

---

## ストークスの定理

$$\int_{\partial M}\omega = \int_M d\omega$$

グリーンの定理・発散定理・古典的ストークスの定理を統一する。

---

## 関連ページ

- [積分](introduction.md)
- [微分（専門）](../derivatives/professional.md)
- [複素関数](introduction.md)
