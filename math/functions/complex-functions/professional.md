---
title: 複素関数
description: "リーマン面・解析接続・モジュラー形式"
tags: [math,complex-numbers,complex-functions]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 関数の操作
    path: /math/functions/index.html
  - title: 複素関数
    path: /math/functions/complex-functions/professional.html
levels:
  - level: 入門
    path: introduction.html
  - level: 標準
    path: standard.html
  - level: 専門
level: 専門
requires:
  - title: 複素関数
    path: /math/functions/complex-functions/introduction.html
  - title: 対数関数（専門）
    path: ../../logarithmic/professional.md
  - title: 点（専門）
    path: ../../../geometry/point/professional.md
---


## このページで扱うこと

リーマン面・解析接続・モジュラー形式を扱います。

- リーマン面（多価関数の定義域）
- 解析接続とモノドロミー
- モジュラー形式の概要

---

## リーマン面

多価関数（$\log z$, $\sqrt{z}$）を一価にするための被覆空間。

$\log z$ のリーマン面は無限に重なった螺旋状のシート。

---

## 解析接続

正則関数を定義域の外に一意に拡張する操作。

**例**: $\zeta(s) = \sum n^{-s}$（$\text{Re}(s)>1$ で定義）を全複素平面に解析接続 → リーマンゼータ関数

---

## モノドロミー

解析接続して一周したとき関数値がどう変化するかを追跡する群論的構造。

---

## モジュラー形式

上半平面 $\mathbb{H}$ 上の正則関数で、$SL(2,\mathbb{Z})$ の変換に対してほぼ不変:

$$f\left(\frac{az+b}{cz+d}\right) = (cz+d)^k f(z)$$

整数論・弦理論との深い関係（谷山・志村予想とフェルマーの最終定理）。

---

## 関連ページ

- [複素関数](introduction.md)
- [複素数（専門）](../../numbers/complex-numbers/professional.md)
- [等号・等式（専門）](../../math-language/equations/professional.md)
