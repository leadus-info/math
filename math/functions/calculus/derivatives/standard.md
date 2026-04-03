---
title: 微分
description: "「今この瞬間の速さ」を求める操作"
difficulty: 2
tags: [math,operations,derivatives]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数の操作
    href: /math/functions/calculus/index.html
  - text: 微分
    href: /math/functions/calculus/derivatives/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---





# 微分
車のスピードメーターは「今この瞬間の速さ」を表しています。
$100$ km 走るのに $2$ 時間かかったとしても、ずっと同じ速さだったわけではありません。
**微分**は、こういった「瞬間の変化の速さ」を求める操作です。

## このページで扱うこと
- 「変化の速さ」のイメージ（平均 → 瞬間）
- 微分の計算（よく使う公式）
- グラフでの意味

## 前提知識
- [極限](../limits/standard.md) — 「限りなく近づける」操作
- [乗法・べき乗](../../../numbers/arithmetic/standard.md)

---

## 平均の変化の速さ

$2$ 時間で $100$ km 走ったときの「平均の速さ」は

$$\frac{100 \text{ km}}{2 \text{ 時間}} = 50 \text{ km/時}$$

これを式で書くと：変化の速さ $= \dfrac{f(b) - f(a)}{b - a}$

グラフ上で見ると、**$2$ 点を結んだ直線の傾き**です。

---

## 瞬間の変化の速さ（微分）

$2$ 点をどんどん近づけていくと、直線は最終的に**接線**（グラフに接する直線）になります。
この**接線の傾き**が「瞬間の変化の速さ」です。

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

この操作を「$f$ を微分する」といい、$f'(x)$（エフダッシュエックス）と書きます。

---

## よく使う微分の公式

| 元の式 $f(x)$ | 微分した式 $f'(x)$ |
|---------------|-------------------|
| 定数（例：$5$） | $0$ |
| $x$ | $1$ |
| $x^2$ | $2x$ |
| $x^3$ | $3x^2$ |
| $x^n$ | $nx^{n-1}$ |
| $e^x$ | $e^x$ |
| $\sin x$ | $\cos x$ |
| $\cos x$ | $-\sin x$ |

$x^n$ の微分は「指数を前に出して、指数を $1$ 減らす」と覚えましょう。

---

## 微分の計算ルール

**定数倍・足し算**：

$$(3x^2)' = 3 \times 2x = 6x$$
$$(x^2 + x)' = 2x + 1$$

**掛け算（積の微分法則）**：

$$(fg)' = f'g + fg'$$

**割り算（商の微分法則）**：

$$\left(\frac{f}{g}\right)' = \frac{f'g - fg'}{g^2}$$

---

## グラフで見た意味

- $f'(a) > 0$：$x = a$ の付近でグラフが**右上がり**
- $f'(a) < 0$：$x = a$ の付近でグラフが**右下がり**
- $f'(a) = 0$：グラフが**平ら**（山の頂上か谷の底の候補）

---

## 関連ページ

- [積分](../integrals/standard.md) — 微分の逆操作
- [極限](../limits/standard.md)
- [微分（発展）](../derivatives/advanced.md) — より詳しく学ぶ
