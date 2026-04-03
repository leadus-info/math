---
title: 三角関数
description: "角度から波を作る関数"
difficulty: 2
tags: [math,functions,trigonometric]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 三角関数
    href: /math/functions/trigonometric/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 三角関数
波・振動・回転——周期的に繰り返す変化を表す関数が**三角関数**です。
単位円（半径 $1$ の円）の上の点の座標として定義します。

## このページで扱うこと
- $\sin$・$\cos$・$\tan$ の定義
- 主要な角度の値
- グラフの形・周期

## 前提知識
- [円](../../geometry/circle/standard.md) — 単位円
- [分数](../../numbers/fractions/standard.md)

---

## 単位円で定義する

半径 $1$ の円の上を動く点を考えます。
$x$ 軸の正方向から角度 $\theta$ の点の座標が $(\cos\theta,\ \sin\theta)$ です。

$$\cos\theta = x \text{ 座標}, \quad \sin\theta = y \text{ 座標}$$

$$\tan\theta = \frac{\sin\theta}{\cos\theta} = \frac{y \text{ 座標}}{x \text{ 座標}}$$

---

## 主要な値

| 角度 | $0°$ | $30°$ | $45°$ | $60°$ | $90°$ |
|------|------|-------|-------|-------|-------|
| $\sin$ | $0$ | $\frac{1}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{3}}{2}$ | $1$ |
| $\cos$ | $1$ | $\frac{\sqrt{3}}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{1}{2}$ | $0$ |
| $\tan$ | $0$ | $\frac{1}{\sqrt{3}}$ | $1$ | $\sqrt{3}$ | 定義なし |

---

## グラフと周期

| 関数 | 周期 | 値の範囲 |
|------|------|---------|
| $\sin x$ | $360°$（$= 2\pi$ ラジアン） | $-1$ から $1$ |
| $\cos x$ | $360°$ | $-1$ から $1$ |
| $\tan x$ | $180°$（$= \pi$ ラジアン） | すべての実数 |

$\sin$ と $\cos$ は波のような形、$\tan$ は周期ごとに $-\infty$ から $+\infty$ に飛びます。

---

## 基本公式

$$\sin^2\theta + \cos^2\theta = 1 \quad \text{（ピタゴラスの定理から）}$$

**加法定理**：

$$\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$$
$$\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$$

---

## 微分

$$(\sin x)' = \cos x, \quad (\cos x)' = -\sin x$$

---

## 関連ページ

- [円](../../geometry/circle/standard.md)
- [三角関数（発展）](../trigonometric/advanced.md) — より詳しく学ぶ
