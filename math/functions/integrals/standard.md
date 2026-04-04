---
title: 積分
description: "面積・累積を求める操作"
tags: [math,operations,integrals]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 関数の操作
    path: /math/functions/index.html
  - title: 積分
    path: /math/functions/integrals/standard.html
levels:
  - level: introduction
    path: introduction.html
  - level: standard
  - level: professional
    path: professional.html
level: standard
requires:
  - title: 微分
    path: /math/functions/derivatives/introduction
  - title: 極限
    path: /math/functions/limits/introduction
---



グラフの下の面積を求める操作が積分です。微分の逆操作でもあります。

## 積分のアイデア

$y = f(x)$ のグラフと $x$ 軸で囲まれた $a \leq x \leq b$ の面積を求めたいとします。

1. 区間 $[a, b]$ を $n$ 等分する
2. 各小区間で高さ $f(x_k)$、幅 $\Delta x = \frac{b-a}{n}$ の長方形で近似する
3. すべての長方形の面積を足す：$\sum_{k=1}^n f(x_k) \Delta x$
4. $n \to \infty$（幅を限りなく細く）した極限が積分の値

$$\int_a^b f(x)\,dx = \lim_{n \to \infty} \sum_{k=1}^n f(x_k)\,\Delta x$$

---

## 不定積分

微分の逆操作を**不定積分**といいます。
$F'(x) = f(x)$ を満たす $F(x)$ を $f(x)$ の**原始関数**といい、

$$\int f(x)\,dx = F(x) + C$$

と書きます（$C$ は任意定数）。微分すると $f(x)$ になる関数を探す操作です。

---

## 微積分学の基本定理

定積分は原始関数で計算できます。

$$\int_a^b f(x)\,dx = F(b) - F(a) \quad \text{ただし } F'(x) = f(x)$$

例：$\int_0^2 x^2\,dx = \left[\frac{x^3}{3}\right]_0^2 = \frac{8}{3} - 0 = \frac{8}{3}$

これにより「面積を求める」問題が「原始関数に端点を代入して引く」操作に変わります。

---

## 基本的な不定積分

| $f(x)$ | $\int f(x)\,dx$ |
|--------|----------------|
| $x^n$ ($n \neq -1$) | $\dfrac{x^{n+1}}{n+1} + C$ |
| $\dfrac{1}{x}$ | $\ln|x| + C$ |
| $e^x$ | $e^x + C$ |
| $\sin x$ | $-\cos x + C$ |
| $\cos x$ | $\sin x + C$ |

---

## 計算技法

**置換積分**：$u = g(x)$ と置くことで積分を簡単にします。

$$\int 2x \cos(x^2)\,dx \xrightarrow{u = x^2} \int \cos u\,du = \sin u + C = \sin(x^2) + C$$

**部分積分**：積の形のときに使います。

$$\int f \cdot g'\,dx = f \cdot g - \int f' \cdot g\,dx$$

例：$\int x e^x\,dx = x e^x - \int e^x\,dx = x e^x - e^x + C = (x-1)e^x + C$

---

## 関連ページ

- [微分](../derivatives/introduction.md) — 積分の逆操作
- [極限](../limits/introduction.md) — 積分の定義の基礎
