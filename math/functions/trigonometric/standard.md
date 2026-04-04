---
title: 三角関数
description: "角度と円から生まれる周期関数"
tags: [math,functions,trigonometric]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/functions/index.md
  - title: 三角関数
    path: /math/functions/trigonometric/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 円
    path: /math/geometry/circle/introduction.md
  - title: 分数
    path: /math/numbers/fractions/introduction.md
---



## このページで扱うこと

波・振動・回転——周期的な変化を表す関数です。
単位円（半径 1 の円）の上を動く点の座標として定義されます。

- $\sin$・$\cos$・$\tan$ の定義と主要な値
- グラフの周期と振幅
- 加法定理

---

## 定義（単位円）

半径 1 の円の上の点 $(\cos\theta,\ \sin\theta)$ で定義します。

- $\cos\theta$：$x$ 座標
- $\sin\theta$：$y$ 座標
- $\tan\theta = \dfrac{\sin\theta}{\cos\theta}$

---

## 主要な値

| 角度 | $0°$ | $30°$ | $45°$ | $60°$ | $90°$ |
|------|------|-------|-------|-------|-------|
| $\sin$ | $0$ | $\frac{1}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{3}}{2}$ | $1$ |
| $\cos$ | $1$ | $\frac{\sqrt{3}}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{1}{2}$ | $0$ |

---

## グラフの性質

| 関数 | 周期 | 値の範囲 |
|------|------|---------|
| $\sin x$ | $360°$ | $-1$ から $1$ |
| $\cos x$ | $360°$ | $-1$ から $1$ |
| $\tan x$ | $180°$ | すべての実数 |

---

## 基本公式

$$\sin^2\theta + \cos^2\theta = 1$$

**加法定理**：

$$\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$$
$$\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$$

---

## 微分

$$(\sin x)' = \cos x, \quad (\cos x)' = -\sin x$$

---

## 関連ページ

- [円](professional.md)
- [複素数](professional.md) — オイラーの公式
- [三角関数（専門）](professional.md) — フーリエ解析
