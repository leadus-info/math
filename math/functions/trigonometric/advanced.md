---
title: 三角関数（発展）
description: "角度と円から生まれる周期関数（発展）"
difficulty: 3
tags: [math,functions,trigonometric,advanced]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 三角関数（発展）
    href: /math/functions/trigonometric/advanced.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
  - text: 専門
    href: professional.html
---







# 三角関数
波・振動・回転——周期的な変化を表す関数です。
単位円（半径 1 の円）の上を動く点の座標として定義されます。

## このページで扱うこと
- $\sin$・$\cos$・$\tan$ の定義と主要な値
- グラフの周期と振幅
- 加法定理

## 前提知識
- [円](professional.md) — 単位円の概念
- [分数](professional.md) — 角度の計算

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
