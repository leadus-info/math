---
title: 三角形
description: "三点で定まる基本図形"
tags: [math,geometry,triangle]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 幾何
    url: /math/geometry/index.html
  - title: 三角形
    url: /math/geometry/triangle/standard.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
  - level: professional
    url: professional.html
level: standard
requires:
  - title: 点
    url: /math/geometry/point/introduction
  - title: 直線
    url: /math/geometry/line/introduction
  - title: 三角関数
    url: /math/functions/trigonometric/introduction
---


> この記事は [入門](introduction.md) の続きです。先に入門を読むことを推奨します。

3 本の直線で囲まれた最もシンプルな多角形が**三角形**です。

## このページで扱うこと
- 内角の和・辺の大小関係
- 面積の求め方
- 正弦定理・余弦定理

---

## 内角の和

$$\alpha + \beta + \gamma = 180°$$

---

## 面積

$$S = \frac{1}{2} \times \text{底辺} \times \text{高さ} = \frac{1}{2}ab\sin C$$

**ヘロンの公式**（3 辺から）：

$$s = \frac{a+b+c}{2}, \quad S = \sqrt{s(s-a)(s-b)(s-c)}$$

---

## 正弦定理

$$\frac{a}{\sin A} = \frac{b}{\sin B} = \frac{c}{\sin C} = 2R$$

---

## 余弦定理

$$a^2 = b^2 + c^2 - 2bc\cos A$$

$A = 90°$ のとき、ピタゴラスの定理になります。

---

## 重心・外心・内心

| 点 | 定義 |
|----|------|
| 重心 | 中線の交点。座標は頂点の平均 |
| 外心 | 外接円の中心 |
| 内心 | 内接円の中心 |

---

## 関連ページ

- [円](professional.md)
- [三角関数](professional.md)
- [三角形（専門）](professional.md)
