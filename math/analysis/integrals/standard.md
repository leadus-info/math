---
title: 積分
description: "面積・累積を求める操作"
goal: "積分の定義・主要な定理・代表的な計算を理解し、後続のトピックに進める基礎を身につける"
tags: [math,operations,integrals]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数の操作
    path: /math/analysis/index.md
  - title: 積分
    path: /math/analysis/integrals/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 微分
    path: /math/analysis/derivatives/introduction.md
  - title: 極限
    path: /math/analysis/limits/introduction.md
---

## 定積分の定義

区間 $[a, b]$ を $n$ 等分し、各小区間で高さ $f(x_k)$、幅 $\Delta x = \frac{b-a}{n}$ の長方形で近似します。

$$\int_a^b f(x)\,dx = \lim_{n \to \infty} \sum_{k=1}^n f(x_k)\,\Delta x$$

これが $f$ の $a$ から $b$ までの**定積分**であり、グラフと $x$ 軸で囲まれた面積を表します（$f \geq 0$ の場合）。

---

## 不定積分と原始関数

$F'(x) = f(x)$ を満たす $F(x)$ を $f(x)$ の**原始関数**といい、

$$\int f(x)\,dx = F(x) + C$$

と書きます（$C$ は任意定数）。

---

## 微積分学の基本定理

$$\int_a^b f(x)\,dx = F(b) - F(a) \quad \text{（$F'(x) = f(x)$ とする）}$$

面積の計算が、原始関数に端点を代入する操作に変わります。

**例**：$\displaystyle\int_0^2 x^2\,dx = \left[\frac{x^3}{3}\right]_0^2 = \frac{8}{3}$

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

**置換積分**：$u = g(x)$ と置き、積分を変数変換します。

$$\int 2x\cos(x^2)\,dx \xrightarrow{u=x^2} \int \cos u\,du = \sin u + C = \sin(x^2) + C$$

**部分積分**：積の形に使います。

$$\int f g'\,dx = fg - \int f'g\,dx$$

**例**：$\displaystyle\int x e^x\,dx = xe^x - \int e^x\,dx = (x-1)e^x + C$

---

## 関連ページ

- [積分（入門）](introduction.md)
- [微分（標準）](../derivatives/standard.md)
