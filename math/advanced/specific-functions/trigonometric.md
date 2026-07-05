---
title: 三角関数
description: "角度と波を表す周期関数"
goal: "三角関数が単位円から定義されることを理解し、基本性質・加法定理・合成を使って値や式を扱えるようになる"
tags: [math, specific-functions, trigonometric]
stage: advanced
subject: 具体的な関数
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 応用編
    path: ../index.md
  - title: 三角関数
    path: trigonometric.md
requires:
  - title: 三角比
    path: ../geometry/trigonometry.md
  - title: 円
    path: ../geometry/circles.md
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

## 三角関数の合成

$a\sin\theta + b\cos\theta$ のように $\sin$ と $\cos$ が混ざった式も、加法定理を逆向きに使うと、1つの $\sin$ にまとめられます。

$$a\sin\theta + b\cos\theta = \sqrt{a^2+b^2}\,\sin(\theta+\varphi)$$

ここで $\varphi$ は、$\cos\varphi = \dfrac{a}{\sqrt{a^2+b^2}}$、$\sin\varphi = \dfrac{b}{\sqrt{a^2+b^2}}$ を満たす角です。

**例**：$\sin\theta+\cos\theta$ を合成する。$\sqrt{1^2+1^2}=\sqrt2$ で、$\cos\varphi=\sin\varphi=\dfrac{1}{\sqrt2}$ より $\varphi=\dfrac{\pi}{4}$。よって $\sin\theta+\cos\theta=\sqrt2\sin\left(\theta+\dfrac{\pi}{4}\right)$。

この形にすると、最大値・最小値や周期といった $a\sin\theta+b\cos\theta$ の性質が、単一の $\sin$ の性質としてそのまま読み取れます。

---

## 微分

$$(\sin x)' = \cos x, \quad (\cos x)' = -\sin x, \quad (\tan x)' = \frac{1}{\cos^2 x}$$

$\sin$ の場合、$\lim_{h\to 0}\dfrac{\sin(x+h)-\sin x}{h} = \lim_{h\to 0}\dfrac{\sin h}{h}\cos x = \cos x$（$\lim_{h\to 0}\frac{\sin h}{h} = 1$ を使用）と導けます。

---

## まとめ

三角関数は単位円上の点の座標として定義される周期関数です。$\sin^2\theta+\cos^2\theta=1$ という基本性質と加法定理を使うと、様々な角度の値を計算したり式を変形したりできます。

---

## 関連ページ

- [微分（応用編）](../analysis/derivatives.md)
