---
title: 三角関数
description: "角度と円から生まれる周期関数"
goal: "三角関数の定義・主要な定理・代表的な計算を理解し、後続のトピックに進める基礎を身につける"
tags: [math,functions,trigonometric]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/analysis/index.md
  - title: 三角関数
    path: /math/geometry/trigonometry/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 円
    path: /math/geometry/euclidean/circles/introduction.md
  - title: 分数
    path: /math/numbers/fractions/introduction.md
---

## 定義（単位円）

半径1の単位円上で、原点から角度 $\theta$（反時計回りを正とするラジアン）の点の座標を $(\cos\theta, \sin\theta)$ と定義します。

$$\tan\theta = \frac{\sin\theta}{\cos\theta} \quad (\cos\theta \neq 0)$$

---

## 主要な値

| $\theta$ | $0$ | $\pi/6$ | $\pi/4$ | $\pi/3$ | $\pi/2$ |
|---------|-----|--------|--------|--------|--------|
| $\sin$ | $0$ | $\dfrac{1}{2}$ | $\dfrac{\sqrt{2}}{2}$ | $\dfrac{\sqrt{3}}{2}$ | $1$ |
| $\cos$ | $1$ | $\dfrac{\sqrt{3}}{2}$ | $\dfrac{\sqrt{2}}{2}$ | $\dfrac{1}{2}$ | $0$ |

ラジアン：$\pi = 180°$、$2\pi = 360°$。

---

## 基本公式

$$\sin^2\theta + \cos^2\theta = 1$$

**加法定理**：

$$\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$$
$$\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$$

加法定理から、2倍角・半角の公式が導かれます。

---

## 微分

$$(\sin x)' = \cos x, \quad (\cos x)' = -\sin x$$

証明は $\displaystyle\lim_{h\to 0}\frac{\sin h}{h} = 1$ を用います。

---

## 例題

$\sin 75° = \sin(45° + 30°)$ を加法定理で計算します。

$$= \sin 45°\cos 30° + \cos 45°\sin 30° = \frac{\sqrt{2}}{2} \cdot \frac{\sqrt{3}}{2} + \frac{\sqrt{2}}{2} \cdot \frac{1}{2} = \frac{\sqrt{6}+\sqrt{2}}{4}$$

---

## 関連ページ

- [三角関数（入門）](introduction.md)
- [複素数（標準）](../../numbers/complex-numbers/standard.md) — オイラーの公式
