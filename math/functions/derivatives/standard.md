---
title: 微分
description: "関数の瞬間の変化率"
tags: [math,operations,derivatives]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数の操作
    path: /math/functions/index.md
  - title: 微分
    path: /math/functions/derivatives/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 極限
    path: /math/functions/limits/introduction.md
  - title: 乗法・べき乗
    path: /math/numbers/arithmetic/introduction.md
---

## 微分の定義

**定義**：関数 $f(x)$ の $x = a$ における**微分係数**を次の極限で定めます。

$$f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}$$

この極限が存在するとき $f$ は $x=a$ で**微分可能**といいます。

$a$ を変数と見た関数 $f'(x)$ を $f$ の**導関数**といいます。\
$f'(x)$、$\frac{df}{dx}$、$\frac{d}{dx}f(x)$ はすべて同じ意味です。

**幾何学的意味**：$f'(a)$ はグラフ $y = f(x)$ の点 $(a, f(a))$ における接線の傾きです。

---

## 基本的な導関数

| $f(x)$ | $f'(x)$ | 補足 |
|--------|---------|------|
| 定数 $c$ | $0$ | 変化しないから変化率は0 |
| $x^n$ | $nx^{n-1}$ | $n$ は実数全般で成立 |
| $e^x$ | $e^x$ | 微分しても変わらない唯一の指数関数 |
| $\ln x$ | $\dfrac{1}{x}$ | $x > 0$ で定義 |
| $\sin x$ | $\cos x$ | |
| $\cos x$ | $-\sin x$ | |

**例**：$f(x) = x^3$ のとき $f'(x) = 3x^2$。\
$x = 2$ での接線の傾きは $f'(2) = 3 \times 4 = 12$。

**例**：$f(x) = \sqrt{x} = x^{1/2}$ のとき $f'(x) = \frac{1}{2}x^{-1/2} = \frac{1}{2\sqrt{x}}$。

---

## 計算規則

**定数倍・和**（線形性）：

$$(\alpha f + \beta g)' = \alpha f' + \beta g'$$

**積の微分法則**：

$$(fg)' = f'g + fg'$$

**導出**：$\frac{f(x+h)g(x+h) - f(x)g(x)}{h}$ を変形すると\
$\frac{f(x+h)-f(x)}{h} \cdot g(x+h) + f(x) \cdot \frac{g(x+h)-g(x)}{h}$ となり、$h\to 0$ で成立。

**例**：$(x^2 \sin x)' = 2x \sin x + x^2 \cos x$

**商の微分法則**：

$$\left(\frac{f}{g}\right)' = \frac{f'g - fg'}{g^2}$$

**例**：$\left(\frac{x}{x^2+1}\right)' = \frac{1 \cdot (x^2+1) - x \cdot 2x}{(x^2+1)^2} = \frac{1-x^2}{(x^2+1)^2}$

**連鎖律**（合成関数）：

$$(f(g(x)))' = f'(g(x)) \cdot g'(x)$$

**例**：$(\sin(x^2))' = \cos(x^2) \cdot 2x = 2x\cos(x^2)$

---

## 増減と極値

$f'(a) > 0$ なら $x=a$ 付近で増加、$f'(a) < 0$ なら減少、$f'(a) = 0$ なら**極値の候補**。

**定理**：$f'(a) = 0$ かつ $x=a$ の前後で $f'$ の符号が変わるとき、\
$f(a)$ は**極大値**または**極小値**です。

**例題**：$f(x) = x^3 - 3x$ の極値を求めます。\
$f'(x) = 3x^2 - 3 = 3(x+1)(x-1)$\
$f'(x) = 0 \Rightarrow x = \pm 1$\
$x < -1$：$f'>0$（増加）、$-1 < x < 1$：$f'<0$（減少）、$x > 1$：$f'>0$（増加）\
よって $x = -1$ で極大値 $f(-1) = 2$、$x = 1$ で極小値 $f(1) = -2$。

---

## 関連ページ

- [極限](../limits/introduction.md)
- [積分](../integrals/introduction.md)
- [一次関数](../linear/introduction.md) — 傾きが一定の特別な場合
