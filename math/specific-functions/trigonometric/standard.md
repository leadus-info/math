---
title: 三角関数
description: "三角関数の性質・加法定理・逆三角関数"
goal: "加法定理を使って三角関数の値を計算し、逆三角関数の定義と微分を理解できるようになる"
tags: [math,specific-functions,trigonometric]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 具体的な関数
    path: /math/specific-functions/index.md
  - title: 三角関数
    path: /math/specific-functions/trigonometric/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 三角関数（入門）
    path: /math/specific-functions/trigonometric/introduction.md
  - title: 微分（標準）
    path: /math/analysis/derivatives/standard.md
---

## 定義（単位円）

半径 1、原点中心の単位円上で角度 $\theta$（ラジアン）の点の座標を $(\cos\theta, \sin\theta)$ と定義します。

$$\tan\theta = \frac{\sin\theta}{\cos\theta} \quad \left(\cos\theta \neq 0\right)$$

**ラジアンと度の変換**：$\pi \text{ rad} = 180°$（$1 \text{ rad} \approx 57.3°$）

---

## 基本性質

$$\sin^2\theta + \cos^2\theta = 1$$
$$\sin(-\theta) = -\sin\theta \quad \text{（奇関数）}$$
$$\cos(-\theta) = \cos\theta \quad \text{（偶関数）}$$

**周期**：$\sin(\theta + 2\pi) = \sin\theta$、$\cos(\theta + 2\pi) = \cos\theta$（周期 $2\pi$）

---

## 加法定理

$$\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$$
$$\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$$

**2倍角の公式**（$\beta = \alpha$ を代入）：

$$\sin 2\alpha = 2\sin\alpha\cos\alpha$$
$$\cos 2\alpha = \cos^2\alpha - \sin^2\alpha = 1 - 2\sin^2\alpha = 2\cos^2\alpha - 1$$

**半角の公式**：

$$\sin^2\frac{\alpha}{2} = \frac{1 - \cos\alpha}{2}, \quad \cos^2\frac{\alpha}{2} = \frac{1 + \cos\alpha}{2}$$

---

## 微分

$$(\sin x)' = \cos x, \quad (\cos x)' = -\sin x, \quad (\tan x)' = \frac{1}{\cos^2 x}$$

**導出**（$\sin$ の場合）：$\lim_{h\to 0}\frac{\sin(x+h)-\sin x}{h} = \lim_{h\to 0}\frac{\sin h}{h}\cos x = \cos x$

（$\lim_{h\to 0}\frac{\sin h}{h} = 1$ を使用）

---

## 逆三角関数

$\sin$ は単調でないため逆関数が存在しません。定義域を制限して逆関数を定めます。

$$\arcsin: [-1, 1] \to \left[-\frac{\pi}{2}, \frac{\pi}{2}\right], \quad \arccos: [-1, 1] \to [0, \pi]$$
$$\arctan: \mathbb{R} \to \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$$

**微分**：

$$(\arcsin x)' = \frac{1}{\sqrt{1-x^2}}, \quad (\arctan x)' = \frac{1}{1+x^2}$$

---

## 関連ページ

- [三角関数（標準）](../../geometry/trigonometry/standard.md)
- [円（標準）](../../geometry/euclidean/circles/standard.md)
- [微分（標準）](../../analysis/derivatives/standard.md)
