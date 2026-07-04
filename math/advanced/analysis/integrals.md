---
title: 積分
description: "面積・累積を求める操作"
goal: "定積分の定義と微積分学の基本定理を理解し、基本的な不定積分と置換積分・部分積分を計算できるようになる"
tags: [math, analysis, integrals]
stage: 応用編
subject: 解析
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 応用編
    path: /math/advanced/index.md
  - title: 積分
    path: /math/advanced/analysis/integrals.md
requires:
  - title: 微分
    path: /math/advanced/analysis/derivatives.md
  - title: 極限
    path: /math/advanced/analysis/limits.md
---

## 曲線で囲まれた面積

長方形の面積は縦×横で求められますが、なめらかな曲線と $x$ 軸の間の面積は定規では測れません。曲線の下の領域を細い長方形で埋めていき、長方形を無限に細くした極限——それが**積分**です。

$$\text{積分} = \text{面積} = \text{無限に細かくした長方形の和の極限}$$

速さが変化しながら走るとき、細かい時間ごとに「速さ×短い時間」を足し合わせていくと走った距離に近づきます。積分は「変化し続ける量を積み重ねた総量」を求める操作でもあります。

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

| $f(x)$ | $\int f(x)\,dx$ |
|--------|----------------|
| $x^n$ ($n \neq -1$) | $\dfrac{x^{n+1}}{n+1} + C$ |
| $\dfrac{1}{x}$ | $\ln\lvert x\rvert + C$ |
| $e^x$ | $e^x + C$ |
| $\sin x$ | $-\cos x + C$ |
| $\cos x$ | $\sin x + C$ |

---

## 微積分学の基本定理

「速さを積み重ねると距離」「距離を微分すると速さに戻る」——微分と積分は逆の操作です。曲線の傾き（微分）と面積（積分）が逆関係にあるという事実は、数学史上最大の発見のひとつで、**微積分学の基本定理**といいます。

$$\int_a^b f(x)\,dx = F(b) - F(a) \quad \text{（$F'(x) = f(x)$ とする）}$$

面積の計算が、原始関数に端点を代入する操作に変わります。

**例**：$\displaystyle\int_0^2 x^2\,dx = \left[\frac{x^3}{3}\right]_0^2 = \frac{8}{3}$

---

## 計算技法

**置換積分**：$u = g(x)$ と置き、積分を変数変換します。

$$\int 2x\cos(x^2)\,dx \xrightarrow{u=x^2} \int \cos u\,du = \sin u + C = \sin(x^2) + C$$

**部分積分**：積の形に使います。

$$\int f g'\,dx = fg - \int f'g\,dx$$

**例**：$\displaystyle\int x e^x\,dx = xe^x - \int e^x\,dx = (x-1)e^x + C$

---

## 回転体の体積

区間 $[a,b]$ で $y=f(x)$ と $x$ 軸に囲まれた図形を、$x$ 軸のまわりに1回転させてできる立体（**回転体**）の体積は、次の式で求められます。

$$V = \pi\int_a^b \{f(x)\}^2\,dx$$

これは、$x$ を固定するたびにできる半径 $f(x)$ の円（断面積 $\pi\{f(x)\}^2$）を、$a$ から $b$ まで積み重ねたものと考えられます。

**例題**：$y=\sqrt{x}$（$0\leq x\leq 4$）と $x$ 軸で囲まれた図形を $x$ 軸のまわりに回転させた体積を求める。

$$V = \pi\int_0^4 (\sqrt{x})^2\,dx = \pi\int_0^4 x\,dx = \pi\left[\frac{x^2}{2}\right]_0^4 = 8\pi$$

---

## 曲線の長さ

媒介変数表示 $x=f(t)$、$y=g(t)$（$a\leq t\leq b$）で表された曲線の長さは、次の式で求められます。

$$L = \int_a^b \sqrt{\{f'(t)\}^2+\{g'(t)\}^2}\,dt$$

これは、曲線を微小な直線の断片に分け、三平方の定理（中級編）でそれぞれの長さを求めて足し合わせた極限と考えられます。

---

## まとめ

積分は「細い長方形を無限に足し合わせた極限」として面積や累積量を求める操作です。微積分学の基本定理により、原始関数を使って定積分を計算でき、置換積分・部分積分で計算の幅が広がります。

---

## 関連ページ

- [リーマン積分（発展編）](/math/bachelor/analysis/riemann-integral.md)
