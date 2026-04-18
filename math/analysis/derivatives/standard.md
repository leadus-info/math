---
title: 微分
description: "関数の瞬間の変化率"
goal: "微分の定義・主要な定理・代表的な計算を理解し、後続のトピックに進める基礎を身につける"
tags: [math,operations,derivatives]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数の操作
    path: /math/analysis/index.md
  - title: 微分
    path: /math/analysis/derivatives/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 極限
    path: /math/analysis/limits/introduction.md
  - title: 乗法・べき乗
    path: /math/numbers/arithmetic/introduction.md
---

## 微分の定義

**定義**：関数 $f(x)$ の $x = a$ における**微分係数**を次で定めます。

$$f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}$$

この極限が存在するとき $f$ は $x = a$ で**微分可能**といいます。$a$ を変数と見た関数 $f'(x)$ を**導関数**といいます。

幾何学的意味：$f'(a)$ はグラフ $y = f(x)$ の $x = a$ における接線の傾きです。

---

## 基本的な導関数

| $f(x)$ | $f'(x)$ | 補足 |
|--------|---------|------|
| 定数 $c$ | $0$ | 変化しない |
| $x^n$ | $nx^{n-1}$ | $n$ は実数一般で成立 |
| $e^x$ | $e^x$ | 微分しても変わらない |
| $\ln x$ | $\dfrac{1}{x}$ | $x > 0$ で定義 |
| $\sin x$ | $\cos x$ | |
| $\cos x$ | $-\sin x$ | |

**例**：$f(x) = x^3$ のとき $f'(x) = 3x^2$。$f'(2) = 12$（$x=2$ での接線の傾き）。

---

## 計算規則

**和の微分**：$(f + g)' = f' + g'$、$(\alpha f)' = \alpha f'$

**積の微分法則**：$(fg)' = f'g + fg'$

導出：$\dfrac{f(x+h)g(x+h)-f(x)g(x)}{h} = \dfrac{f(x+h)-f(x)}{h} \cdot g(x+h) + f(x) \cdot \dfrac{g(x+h)-g(x)}{h}$、$h\to 0$ で成立。

**例**：$(x^2 \sin x)' = 2x\sin x + x^2\cos x$

**商の微分法則**：$\left(\dfrac{f}{g}\right)' = \dfrac{f'g - fg'}{g^2}$

**連鎖律**（合成関数）：$(f(g(x)))' = f'(g(x)) \cdot g'(x)$

**例**：$(\sin(x^2))' = \cos(x^2) \cdot 2x$

---

## 増減と極値

$f'(a) > 0$ なら $x = a$ 付近で増加、$f'(a) < 0$ なら減少、$f'(a) = 0$ なら**極値の候補**。

**定理**：$f'(a) = 0$ かつ前後で $f'$ の符号が変わるとき、$f(a)$ は極大値または極小値。

**例題**：$f(x) = x^3 - 3x$ の極値を求めます。

$f'(x) = 3x^2 - 3 = 3(x+1)(x-1) = 0 \Rightarrow x = \pm 1$

$x < -1$：$f' > 0$（増加）、$-1 < x < 1$：$f' < 0$（減少）、$x > 1$：$f' > 0$（増加）

よって $x = -1$ で極大値 $f(-1) = 2$、$x = 1$ で極小値 $f(1) = -2$。

---

## 関連ページ

- [微分（入門）](introduction.md)
- [極限（標準）](../limits/standard.md)
- [積分（標準）](../integrals/standard.md)
