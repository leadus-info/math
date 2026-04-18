---
title: 極限
description: "限りなく近づくとはどういうことか"
goal: "極限の定義・主要な定理・代表的な計算を理解し、後続のトピックに進める基礎を身につける"
tags: [math,operations,limits]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数の操作
    path: /math/analysis/index.md
  - title: 極限
    path: /math/analysis/limits/standard.md
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

数列 $\{a_n\}$ が値 $L$ に**収束する**とは、$n$ を大きくするにつれて $a_n$ が $L$ に限りなく近づくことです。

$$\lim_{n \to \infty} a_n = L$$

と書きます。収束しない（発散する）場合もあります。$a_n = n^2$ のように限りなく大きくなる場合は $\lim_{n\to\infty} a_n = \infty$ と書きます。

**例**：

$$\lim_{n \to \infty} \frac{1}{n} = 0, \quad \lim_{n \to \infty} \frac{n}{n+1} = 1, \quad \lim_{n \to \infty} \frac{n^2+1}{2n^2-3} = \frac{1}{2}$$

最後の例：分子・分母を $n^2$ で割ると $\dfrac{1 + 1/n^2}{2 - 3/n^2} \to \dfrac{1}{2}$。

---

## 関数の極限

$x$ を $a$ に近づけたとき $f(x)$ が $L$ に近づくことを

$$\lim_{x \to a} f(x) = L$$

と書きます。「$x = a$ を代入する」のではなく「$a$ に近づける」という点が重要で、$x = a$ で $f$ が定義されていなくても極限は存在しえます。

**例**：$f(x) = \dfrac{x^2 - 1}{x - 1}$ は $x = 1$ で定義されませんが、

$$\frac{x^2-1}{x-1} = \frac{(x-1)(x+1)}{x-1} = x+1 \quad (x \neq 1)$$

なので $\lim_{x \to 1} \dfrac{x^2-1}{x-1} = 2$。

---

## 極限の計算規則

$\lim f = L$、$\lim g = M$ のとき：

$$\lim (f + g) = L + M, \quad \lim (fg) = LM, \quad \lim \frac{f}{g} = \frac{L}{M} \; (M \neq 0)$$

---

## 片側極限と連続

右から近づく**右側極限** $\displaystyle\lim_{x\to a^+} f(x)$ と、左から近づく**左側極限** $\displaystyle\lim_{x\to a^-} f(x)$ が一致するとき、両側極限 $\displaystyle\lim_{x\to a} f(x)$ が存在します。

**定義（連続性）**：$\displaystyle\lim_{x\to a} f(x) = f(a)$ が成り立つとき、$f$ は $x = a$ で**連続**です。

---

## 重要な極限

$$\lim_{n \to \infty} r^n = 0 \quad (|r| < 1)$$

$$\lim_{x \to 0} \frac{\sin x}{x} = 1 \quad \text{（ラジアン単位）}$$

---

## 例題

$\displaystyle\lim_{n\to\infty} \frac{3n^2 + 2n - 1}{n^2 - 5}$ を求めます。

分子・分母を $n^2$ で割ると $\dfrac{3 + 2/n - 1/n^2}{1 - 5/n^2} \to \dfrac{3}{1} = 3$。

---

## 関連ページ

- [極限（入門）](introduction.md)
- [微分（標準）](../derivatives/standard.md)
- [数列（標準）](../sequences/standard.md)
