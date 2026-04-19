---
title: 三角関数
description: "角度と波を表す関数"
goal: "三角関数が単位円から生まれることを理解し、sin・cos・tan の基本的な値と波形を説明できるようになる"
tags: [math,specific-functions,trigonometric]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 具体的な関数
    path: /math/specific-functions/index.md
  - title: 三角関数
    path: /math/specific-functions/trigonometric/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 円（入門）
    path: /math/geometry/euclidean/circles/introduction.md
---

## 円の上を動く点

半径 1 の円（単位円）の上を動く点を考えます。原点から反時計回りに角度 $\theta$ 進んだとき、その点の座標が $(\cos\theta, \sin\theta)$ です。

- $\cos\theta$：$x$ 座標——横方向の成分
- $\sin\theta$：$y$ 座標——縦方向の成分

---

## よく使う値

| 角度 | $0°$ | $30°$ | $45°$ | $60°$ | $90°$ |
|------|------|-------|-------|-------|-------|
| $\sin$ | $0$ | $\frac{1}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{3}}{2}$ | $1$ |
| $\cos$ | $1$ | $\frac{\sqrt{3}}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{1}{2}$ | $0$ |

---

## グラフは「波」

$y = \sin\theta$ のグラフを描くと、山と谷が繰り返す波の形になります。$360°$ ごとに同じ形が繰り返します（**周期** $360°$）。

音の振動・光の波・電流の変化——自然界の周期的な現象はすべて三角関数で表せます。

---

## $\tan$ とは

$$\tan\theta = \frac{\sin\theta}{\cos\theta}$$

$\cos\theta = 0$ のとき（$90°$、$270°$）は定義されません。

---

## 最重要の公式

$$\sin^2\theta + \cos^2\theta = 1$$

単位円の方程式 $x^2 + y^2 = 1$ がそのままこの形になります。

---

## 関連ページ

- [円（入門）](../../geometry/euclidean/circles/introduction.md)
- [三角関数（入門）](../../geometry/trigonometry/introduction.md)
