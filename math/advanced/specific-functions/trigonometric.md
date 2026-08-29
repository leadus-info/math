---
title: 三角関数
description: "単位円上の点の座標として定義される三角関数sin・cos・tanと、正弦と余弦の2乗の和が1になるなどの基本性質・周期性、加法定理から導かれる2倍角・半角の公式、正弦と余弦の1次結合を1つの正弦にまとめる合成を扱う"
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
  - title: 点
    path: ../geometry/point.md
---

## 円の上を動く点

半径1の円（単位円）の上を動く点を考えます。$x$ 軸の正の向きから反時計回りに角度 $\theta$ 進んだとき、その点の座標が $(\cos\theta, \sin\theta)$ です。

- $\cos\theta$：$x$ 座標——横方向の成分
- $\sin\theta$：$y$ 座標——縦方向の成分

$$\tan\theta = \frac{\sin\theta}{\cos\theta} \quad (\cos\theta \neq 0)$$

以降ではラジアンで角度を表すため、度との対応を確認しておきます。**ラジアンと度の変換**：$\pi \text{ rad} = 180°$（$1 \text{ rad} \approx 57.3°$）

| 角度 | $0°$ | $30°$ | $45°$ | $60°$ | $90°$ |
|------|------|-------|-------|-------|-------|
| $\sin$ | $0$ | $\frac{1}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{3}}{2}$ | $1$ |
| $\cos$ | $1$ | $\frac{\sqrt{3}}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{1}{2}$ | $0$ |

---

## 基本性質

$$\sin^2\theta + \cos^2\theta = 1$$

単位円の方程式 $x^2 + y^2 = 1$ がそのままこの形になります。

単位円上で角度を $-\theta$ にすると、点は $x$ 軸に関して対称な位置に移ります（反射）。そのため $x$ 座標（$\cos$）は変わらず、$y$ 座標（$\sin$）の符号だけが反転します。

$$\sin(-\theta) = -\sin\theta \quad \text{（奇関数）}, \qquad \cos(-\theta) = \cos\theta \quad \text{（偶関数）}$$

> [!NOTE]
> 奇関数とは $f(-\theta)=-f(\theta)$ を満たす関数、偶関数とは $f(-\theta)=f(\theta)$ を満たす関数のことです。

**周期**：$\sin(\theta + 2\pi) = \sin\theta$、$\cos(\theta + 2\pi) = \cos\theta$（周期 $2\pi$）。$y = \sin\theta$ のグラフは山と谷が繰り返す波の形になります。音の振動・光の波・電流の変化——自然界の周期的な現象の多くは、三角関数の組み合わせで表せます。

---

## 加法定理

単位円上の2点間の距離を2通りの方法で表すことで、加法定理を導けます。角度 $\alpha$ の点を $\mathrm{P}=(\cos\alpha, \sin\alpha)$、角度 $\beta$ の点を $\mathrm{Q}=(\cos\beta, \sin\beta)$ とします。

まず、通常の2点間の距離の公式から

$$\mathrm{PQ}^2 = (\cos\alpha-\cos\beta)^2+(\sin\alpha-\sin\beta)^2$$

を展開し、基本性質 $\sin^2\theta+\cos^2\theta=1$ で整理すると

$$\mathrm{PQ}^2 = 2-2(\cos\alpha\cos\beta+\sin\alpha\sin\beta)$$

となります。一方、$\mathrm{P}$、$\mathrm{Q}$ をどちらも角度 $-\beta$ だけ回転させても2点間の距離は変わりません（回転不変性）。回転後は角度 $\alpha-\beta$ の点と角度 $0$ の点 $(1,0)$ になるので、同じ整理から

$$\mathrm{PQ}^2 = 2-2\cos(\alpha-\beta)$$

も成り立ちます。2つは同じ $\mathrm{PQ}^2$ を表すので、両者は等しく

$$\cos(\alpha-\beta) = \cos\alpha\cos\beta+\sin\alpha\sin\beta$$

が得られます。$\cos(\alpha+\beta)=\cos(\alpha-(-\beta))$ とみなし、この式で $\beta$ を $-\beta$ に置き換えると、基本性質の偶関数・奇関数の性質（$\cos(-\beta)=\cos\beta$、$\sin(-\beta)=-\sin\beta$）から

$$\cos(\alpha+\beta) = \cos\alpha\cos\beta-\sin\alpha\sin\beta$$

が得られます。$\sin(\alpha+\beta)$ も同様の考え方（$\sin\theta=\cos\left(\theta-\dfrac{\pi}{2}\right)$ という関係を使う方法）で導けますが、ここでは結果のみ示します。

$$\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$$

**2倍角の公式**（$\beta = \alpha$ を代入）：

$$\sin 2\alpha = 2\sin\alpha\cos\alpha, \qquad \cos 2\alpha = \cos^2\alpha - \sin^2\alpha$$

**半角の公式**：

$$\sin^2\frac{\alpha}{2} = \frac{1 - \cos\alpha}{2}, \quad \cos^2\frac{\alpha}{2} = \frac{1 + \cos\alpha}{2}$$

半角の公式は、2倍角の公式と基本性質 $\sin^2\theta+\cos^2\theta=1$ から導けます。

まず $\sin^2\dfrac{\alpha}{2}$ について、$\cos2\alpha=\cos^2\alpha-\sin^2\alpha$ に $\cos^2\alpha=1-\sin^2\alpha$ を代入すると

$$\cos2\alpha = (1-\sin^2\alpha)-\sin^2\alpha = 1-2\sin^2\alpha$$

これを $\sin^2\alpha$ について整理すると $\sin^2\alpha=\dfrac{1-\cos2\alpha}{2}$。ここで $\alpha$ を $\dfrac{\alpha}{2}$ に置き換えると、次が得られます。

$$\sin^2\frac{\alpha}{2}=\frac{1-\cos\alpha}{2}$$

このとき $\cos\left(2\times\dfrac{\alpha}{2}\right)=\cos\alpha$ となっています。

$\cos^2\dfrac{\alpha}{2}$ も同じ手順で導けますが、代入する式は先ほど（$\sin^2\dfrac{\alpha}{2}$の導出）とは異なります。$\cos2\alpha=\cos^2\alpha-\sin^2\alpha$ に、今度は $\sin^2\alpha=1-\cos^2\alpha$ を代入すると

$$\cos2\alpha = \cos^2\alpha-(1-\cos^2\alpha) = 2\cos^2\alpha-1$$

これを $\cos^2\alpha$ について整理すると $\cos^2\alpha=\dfrac{1+\cos2\alpha}{2}$。ここでも $\alpha$ を $\dfrac{\alpha}{2}$ に置き換えると、次が得られます。

$$\cos^2\frac{\alpha}{2}=\frac{1+\cos\alpha}{2}$$

このとき $\cos\left(2\times\dfrac{\alpha}{2}\right)=\cos\alpha$ となっています。

---

## 三角関数の合成

$a\sin\theta + b\cos\theta$ のように $\sin$ と $\cos$ が混ざった式も、加法定理を逆向きに使うと、1つの $\sin$ にまとめられます。$\sqrt{a^2+b^2}\sin(\theta+\varphi)$ を加法定理で展開すると

$$\sqrt{a^2+b^2}\sin(\theta+\varphi) = \sqrt{a^2+b^2}\cos\varphi\,\sin\theta + \sqrt{a^2+b^2}\sin\varphi\,\cos\theta$$

となります。これが $a\sin\theta+b\cos\theta$ と一致するように $\sin\theta$、$\cos\theta$ の係数を比較すると、$\sqrt{a^2+b^2}\cos\varphi=a$、$\sqrt{a^2+b^2}\sin\varphi=b$、すなわち

$$\cos\varphi = \frac{a}{\sqrt{a^2+b^2}}, \qquad \sin\varphi = \frac{b}{\sqrt{a^2+b^2}}$$

この2式の2乗の和は $\cos^2\varphi+\sin^2\varphi=\dfrac{a^2+b^2}{a^2+b^2}=1$ となり、これは「円の上を動く点」で確認した単位円上の点の座標が満たす関係と一致するため、この2式を満たす角 $\varphi$ が存在します。この $\varphi$ をとれば、次の式が成り立ちます。

$$a\sin\theta + b\cos\theta = \sqrt{a^2+b^2}\,\sin(\theta+\varphi)$$

**例**：$\sin\theta+\cos\theta$ を合成する。$\sqrt{1^2+1^2}=\sqrt2$ で、$\cos\varphi=\sin\varphi=\dfrac{1}{\sqrt2}$ より $\varphi=\dfrac{\pi}{4}$（$=45°$）。よって $\sin\theta+\cos\theta=\sqrt2\sin\left(\theta+\dfrac{\pi}{4}\right)$。

この形にすると、最大値・最小値や周期といった $a\sin\theta+b\cos\theta$ の性質が、単一の $\sin$ の性質としてそのまま読み取れます。具体的には、最大値は $\sqrt{a^2+b^2}$、最小値は $-\sqrt{a^2+b^2}$、周期は $2\pi$ です。

---

## まとめ

三角関数は単位円上の点の座標として定義される周期関数です。$\sin^2\theta+\cos^2\theta=1$ という基本性質と加法定理を使うと、様々な角度の値を計算したり式を変形したりできます。また、加法定理を逆向きに使う三角関数の合成によって、$a\sin\theta+b\cos\theta$ の形の式を1つの $\sin$ にまとめ、その最大値・最小値や周期を調べられます。

---

## 関連ページ

- [微分](../analysis/derivatives.md)
