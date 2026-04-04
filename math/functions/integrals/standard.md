---
title: 積分
description: "面積・累積を求める操作"
tags: [math,operations,integrals]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 関数の操作
    url: /math/functions/index.html
  - title: 積分
    url: /math/functions/integrals/standard.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
  - level: professional
    url: professional.html
level: standard
requires:
  - title: 微分
    url: professional.md
  - title: 極限
    url: professional.md
---



グラフと横軸で囲まれた面積を求める——それが**積分**の出発点です。
細かく刻んで足し合わせることで、曲線で囲まれた面積も計算できます。

## このページで扱うこと
- 積分の直感（細かく分割して足し合わせる）
- 微積分学の基本定理（微分と積分の関係）
- よく使う積分の公式と計算技法

---

## 面積を求めるアイデア

グラフの下の面積を細い長方形で近似し、分割を無限に細かくします。

$$\int_a^b f(x)\,dx = \lim_{n \to \infty} \sum_{k=1}^n f(x_k) \Delta x$$

---

## 不定積分

「微分したら $f(x)$ になる関数」を求める操作です。

$$\int f(x)\,dx = F(x) + C \quad (F'(x) = f(x),\ C \text{ は定数})$$

---

## 微積分学の基本定理

$$\int_a^b f(x)\,dx = F(b) - F(a)$$

面積の計算が「$F$ に端点を代入して引く」だけになります。

---

## よく使う積分の公式

| $f(x)$ | $\int f(x)\,dx$ |
|--------|----------------|
| $x^n$（$n \neq -1$） | $\dfrac{x^{n+1}}{n+1} + C$ |
| $\dfrac{1}{x}$ | $\ln|x| + C$ |
| $e^x$ | $e^x + C$ |
| $\sin x$ | $-\cos x + C$ |
| $\cos x$ | $\sin x + C$ |

---

## 計算技法

**置換積分**：$u = g(x)$ と置き換えます。

$$\int 2x\cos(x^2)\,dx \xrightarrow{u=x^2} \int \cos u\,du = \sin(x^2) + C$$

**部分積分**：

$$\int f \cdot g'\,dx = fg - \int f' \cdot g\,dx$$

---

## 関連ページ

- [微分](professional.md)
- [確率](professional.md)
- [積分（専門）](professional.md) — ルベーグ積分・多重積分
