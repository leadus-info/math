---
title: 三角関数
description: "角度と波を表す周期関数"
goal: "三角関数が単位円から定義されることを理解し、基本性質・加法定理を使って値を計算できるようになる"
tags: [math, specific-functions, trigonometric]
stage: 応用編
subject: 具体的な関数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 応用編
    path: /math/advanced/index.md
  - title: 三角関数
    path: /math/advanced/specific-functions/trigonometric.md
requires:
  - title: 円
    path: /math/advanced/geometry/circles.md
---

## 円の上を動く点

半径1の円（単位円）の上を動く点を考えます。原点から反時計回りに角度 $\theta$ 進んだとき、その点の座標が $(\cos\theta, \sin\theta)$ です。

- $\cos\theta$：$x$ 座標——横方向の成分
- $\sin\theta$：$y$ 座標——縦方向の成分

$$\tan\theta = \frac{\sin\theta}{\cos\theta} \quad (\cos\theta \neq 0)$$

**ラジアンと度の変換**：$\pi \text{ rad} = 180°$（$1 \text{ rad} \approx 57.3°$）

| 角度 | $0°$ | $30°$ | $45°$ | $60°$ | $90°$ |
|------|------|-------|-------|-------|-------|
| $\sin$ | $0$ | $\frac{1}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{3}}{2}$ | $1$ |
| $\cos$ | $1$ | $\frac{\sqrt{3}}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{1}{2}$ | $0$ |

---

## 基本性質

$$\sin^2\theta + \cos^2\theta = 1$$

単位円の方程式 $x^2 + y^2 = 1$ がそのままこの形になります。

$$\sin(-\theta) = -\sin\theta \quad \text{（奇関数）}, \qquad \cos(-\theta) = \cos\theta \quad \text{（偶関数）}$$

**周期**：$\sin(\theta + 2\pi) = \sin\theta$、$\cos(\theta + 2\pi) = \cos\theta$（周期 $2\pi$）。$y = \sin\theta$ のグラフは山と谷が繰り返す波の形になります。音の振動・光の波・電流の変化——自然界の周期的な現象はすべて三角関数で表せます。

---

## 加法定理

$$\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$$
$$\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$$

**2倍角の公式**（$\beta = \alpha$ を代入）：

$$\sin 2\alpha = 2\sin\alpha\cos\alpha, \qquad \cos 2\alpha = \cos^2\alpha - \sin^2\alpha$$

**半角の公式**：

$$\sin^2\frac{\alpha}{2} = \frac{1 - \cos\alpha}{2}, \quad \cos^2\frac{\alpha}{2} = \frac{1 + \cos\alpha}{2}$$

---

## 微分

$$(\sin x)' = \cos x, \quad (\cos x)' = -\sin x, \quad (\tan x)' = \frac{1}{\cos^2 x}$$

$\sin$ の場合、$\lim_{h\to 0}\dfrac{\sin(x+h)-\sin x}{h} = \lim_{h\to 0}\dfrac{\sin h}{h}\cos x = \cos x$（$\lim_{h\to 0}\frac{\sin h}{h} = 1$ を使用）と導けます。

---

## まとめ

三角関数は単位円上の点の座標として定義される周期関数です。$\sin^2\theta+\cos^2\theta=1$ という基本性質と加法定理を使うと、様々な角度の値を計算したり式を変形したりできます。

---

## 関連ページ

- [円（応用編）](/math/advanced/geometry/circles.md)
- [微分（応用編）](/math/advanced/analysis/derivatives.md)
