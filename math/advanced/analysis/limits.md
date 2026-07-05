---
title: 極限
description: "限りなく近づくとはどういうことか"
goal: "数列と関数の極限の意味を理解し、極限の計算規則を使って値を求め、連続性を説明できるようになる"
tags: [math, analysis, limits]
stage: advanced
subject: 解析
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 応用編
    path: ../index.md
  - title: 極限
    path: limits.md
requires:
  - title: 数列
    path: sequences.md
  - title: 三角関数
    path: ../specific-functions/trigonometric.md
---

## 「近づく」とはどういうことか

$\frac{1}{10}$、$\frac{1}{100}$、$\frac{1}{1000}$……分母を大きくしていくと、この分数は0に近づいていきます。でも、どんなに分母を大きくしても、$\frac{1}{n}$ はちょうど0にはなりません。このように「限りなく近づいていく先の値」を**極限**といいます。

アキレスと亀のパラドックスを考えてみましょう。アキレスは亀の10倍の速さで走り、亀は100m先からスタートします。アキレスが100m進む間に亀は10m、その10mを進む間に亀は1m……と、亀は常にわずかに先にいるように見えます。しかしアキレスが走る距離の合計 $100 + 10 + 1 + 0.1 + \ldots$ は限りなく $111.1\ldots$ mに近づき、有限の距離に収まります。**無限個足しても有限の値になる**——これが極限の力です。

---

## 数列の極限

数列 $\{a_n\}$ が値 $L$ に**収束する**とは、$n$ を大きくするにつれて $a_n$ が $L$ に限りなく近づくことです。

$$\lim_{n \to \infty} a_n = L$$

収束しない場合は「**発散する**」といいます。$a_n = n^2$ のように限りなく大きくなる場合は $\lim_{n\to\infty} a_n = \infty$ と書きます。

**例**：

$$\lim_{n \to \infty} \frac{1}{n} = 0, \quad \lim_{n \to \infty} \frac{n^2+1}{2n^2-3} = \frac{1}{2}$$

最後の例は、分子・分母を $n^2$ で割ると $\dfrac{1 + 1/n^2}{2 - 3/n^2} \to \dfrac{1}{2}$ とわかります。

---

## 関数の極限

$x$ を $a$ に近づけたとき $f(x)$ が $L$ に近づくことを

$$\lim_{x \to a} f(x) = L$$

と書きます。「$x = a$ を代入する」のではなく「$a$ に近づける」という点が重要で、$x=a$ で $f$ が定義されていなくても極限は存在しえます。

**例**：$f(x) = \dfrac{x^2 - 1}{x - 1}$ は $x = 1$ で定義されませんが、

$$\frac{x^2-1}{x-1} = \frac{(x-1)(x+1)}{x-1} = x+1 \quad (x \neq 1)$$

なので $\lim_{x \to 1} \dfrac{x^2-1}{x-1} = 2$。

---

## 極限の計算規則

$\lim f = L$、$\lim g = M$ のとき：

$$\lim (f + g) = L + M, \quad \lim (fg) = LM, \quad \lim \frac{f}{g} = \frac{L}{M} \; (M \neq 0)$$

---

## 連続性

**定義**：$\displaystyle\lim_{x\to a} f(x) = f(a)$ が成り立つとき、$f$ は $x = a$ で**連続**であるといいます。グラフでいうと、その点で線がつながっている（切れ目がない）ということです。

---

## 重要な極限

$$\lim_{n \to \infty} r^n = 0 \quad (|r| < 1)$$

$$\lim_{x \to 0} \frac{\sin x}{x} = 1 \quad \text{（ラジアン単位）}$$

**例題**：$\displaystyle\lim_{n\to\infty} \frac{3n^2 + 2n - 1}{n^2 - 5}$ を求める。分子・分母を $n^2$ で割ると $\dfrac{3 + 2/n - 1/n^2}{1 - 5/n^2} \to 3$。

---

## はさみうちの原理

極限が直接計算しづらいとき、その数列（関数）を上下から挟む2つの数列（関数）の極限が一致すれば、間の極限も同じ値に定まります。

**はさみうちの原理**：$a_n \leq b_n \leq c_n$ が成り立ち、$\displaystyle\lim_{n\to\infty} a_n = \lim_{n\to\infty} c_n = L$ ならば、$\displaystyle\lim_{n\to\infty} b_n = L$。

**例**：$\displaystyle\lim_{n\to\infty} \frac{\sin n}{n}$ を求める。$-1 \leq \sin n \leq 1$ より $-\dfrac1n \leq \dfrac{\sin n}{n} \leq \dfrac1n$。両端が0に収束するので、はさみうちの原理より極限も0。

---

## まとめ

極限とは「ある値に限りなく近づいていく先」のことです。数列でも関数でも定義でき、和・積・商について計算規則が成り立ちます。連続性は「極限と実際の値が一致する」性質として定義され、微分・積分の土台になります。

---

## 関連ページ

- [微分（応用編）](derivatives.md)
- [極限の厳密な定義（発展編）](../../bachelor/analysis/epsilon-delta.md)
