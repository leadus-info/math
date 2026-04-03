---
title: 積分
description: "面積を細かく足し合わせる操作"
difficulty: 2
tags: [math,operations,integrals]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数の操作
    href: /math/functions/calculus/index.html
  - text: 積分
    href: /math/functions/calculus/integrals/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---





# 積分
曲線で囲まれた図形の面積は、定規だけでは測れません。
**積分**は「細かく分割して足し合わせる」ことで、この面積を求める操作です。

## このページで扱うこと
- 積分のアイデア（細かく分けて足し合わせる）
- 微分との関係（逆操作）
- よく使う積分の公式

## 前提知識
- [微分](../derivatives/standard.md)
- [極限](../limits/standard.md)

---

## 積分のアイデア

$y = f(x)$ のグラフと $x$ 軸で囲まれた面積を求めたいとします。

1. 区間を細い短冊に分割する
2. 各短冊を「高さ $f(x)$、幅 $\Delta x$ の長方形」で近似する
3. すべての長方形の面積を足し合わせる
4. 分割を**無限に細かく**した極限が「積分」

$$\int_a^b f(x)\,dx = \lim_{\Delta x \to 0} \sum f(x_k) \Delta x$$

$\int$（インテグラル）は「$S$（Summation = 和）」を細長くした記号です。

---

## 微分と積分の関係

微分の「逆操作」が積分です。

「微分すると $f(x)$ になる関数」を $F(x)$ とすると：

$$\int_a^b f(x)\,dx = F(b) - F(a)$$

この関係を**微積分学の基本定理**といいます。
面積の計算が「$F(b) - F(a)$」という引き算に変わります。

---

## よく使う積分の公式

| 元の式 $f(x)$ | 積分 $\int f(x)\,dx$ |
|---------------|----------------------|
| 定数 $c$ | $cx + C$ |
| $x$ | $\dfrac{x^2}{2} + C$ |
| $x^2$ | $\dfrac{x^3}{3} + C$ |
| $x^n$（$n \neq -1$） | $\dfrac{x^{n+1}}{n+1} + C$ |
| $e^x$ | $e^x + C$ |
| $\sin x$ | $-\cos x + C$ |

$C$ は「積分定数」——微分したとき消えてしまう定数の分を補います。

---

## 計算例

$$\int_0^2 x^2\,dx = \left[\frac{x^3}{3}\right]_0^2 = \frac{8}{3} - 0 = \frac{8}{3}$$

---

## 関連ページ

- [微分](../derivatives/standard.md)
- [確率](../../../statistics/probability/standard.md) — 確率の「面積」を積分で計算
- [積分（発展）](../integrals/advanced.md) — より詳しく学ぶ
