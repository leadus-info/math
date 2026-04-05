---
title: 極限
description: "限りなく近づくとはどういうことか"
tags: [math,operations,limits]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数の操作
    path: /math/functions/index.md
  - title: 極限
    path: /math/functions/limits/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 乗法・べき乗
    path: /math/numbers/arithmetic/introduction.md
  - title: 分数
    path: /math/numbers/fractions/introduction.md
---

## 数列の極限

数列 $\{a_n\}$ が値 $L$ に**収束**するとは、\
$n$ を大きくするにつれて $a_n$ が $L$ に限りなく近づくことです。

$$\lim_{n \to \infty} a_n = L$$

**例**：

$$\lim_{n \to \infty} \frac{1}{n} = 0, \quad \lim_{n \to \infty} \frac{n}{n+1} = 1, \quad \lim_{n \to \infty} \frac{n^2+1}{2n^2-3} = \frac{1}{2}$$

最後の例：分子・分母を $n^2$ で割ると $\frac{1 + 1/n^2}{2 - 3/n^2} \to \frac{1}{2}$。

収束しない場合を**発散**といいます。$\lim_{n\to\infty} n^2 = \infty$（正の無限大に発散）。

---

## 関数の極限

$x$ を $a$ に近づけたとき $f(x)$ が $L$ に近づくことを

$$\lim_{x \to a} f(x) = L$$

と書きます。「$x = a$ を代入する」のではなく「$a$ に近づける」という点が重要です。\
$x = a$ で $f$ が定義されていなくても極限は存在しうります。

**例**：$\displaystyle\lim_{x \to 2}(3x+1) = 7$（$x=2$ を代入した値と一致）

**例**（定義域外での極限）：$f(x) = \frac{x^2-1}{x-1}$ は $x=1$ で定義されませんが、\
$\frac{x^2-1}{x-1} = \frac{(x-1)(x+1)}{x-1} = x+1$（$x \neq 1$）\
なので $\displaystyle\lim_{x \to 1} \frac{x^2-1}{x-1} = 2$。

---

## 極限の計算規則

$\lim f = L$、$\lim g = M$ のとき（$x \to a$ または $n \to \infty$）：

$$\lim (f + g) = L + M$$
$$\lim (f \times g) = L \times M$$
$$\lim \frac{f}{g} = \frac{L}{M} \quad (M \neq 0)$$

これらを使って複雑な極限を分解して計算できます。

---

## 片側極限と連続

右から近づく**右側極限** $\lim_{x\to a^+} f(x)$ と\
左から近づく**左側極限** $\lim_{x\to a^-} f(x)$ が両方存在して等しいとき、\
（両側）極限 $\lim_{x\to a} f(x)$ が存在します。

**定義**：$\lim_{x\to a} f(x) = f(a)$ が成り立つとき $f$ は $x=a$ で**連続**であるといいます。

**例**（不連続な点）：$f(x) = \frac{1}{x}$ は $x=0$ で連続でありません（極限が存在しない）。

---

## よく使う極限

$$\lim_{n \to \infty} r^n = 0 \quad (|r| < 1)$$

**例**：$0.9^n \to 0$、$(-0.5)^n \to 0$、しかし $1.1^n \to \infty$。

$$\lim_{x \to 0} \frac{\sin x}{x} = 1 \quad \text{（ラジアン単位）}$$

この極限は三角関数の微分の計算で重要です。

---

## 例題

**例題**：$\displaystyle\lim_{n\to\infty} \frac{3n^2 + 2n - 1}{n^2 - 5}$ を求めてください。

分子・分母を $n^2$ で割ると：

$$\frac{3 + 2/n - 1/n^2}{1 - 5/n^2} \to \frac{3}{1} = 3$$

---

## 関連ページ

- [数列](../sequences/introduction.md)
- [微分](../derivatives/introduction.md)
- [積分](../integrals/introduction.md)
