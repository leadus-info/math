---
title: 微分
description: "関数の瞬間の変化率"
tags: [math,operations,derivatives]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 関数の操作
    url: /math/functions/index.html
  - title: 微分
    url: /math/functions/derivatives/standard.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
  - level: professional
    url: professional.html
level: standard
requires:
  - title: 極限
    url: /math/functions/limits/introduction
  - title: 乗法・べき乗
    url: /math/numbers/arithmetic/introduction
---


関数の「瞬間の変化の速さ」を求める操作が微分です。

## 平均の変化率

関数 $f(x)$ において、$x$ が $a$ から $b$ まで変化するとき

$$\frac{f(b) - f(a)}{b - a}$$

を**平均の変化率**といいます。グラフ上では、2点 $(a, f(a))$ と $(b, f(b))$ を結ぶ直線の傾きです。

---

## 微分の定義（導関数）

2点を限りなく近づけた極限が**微分係数**（瞬間の変化率）です。

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

この $f'(x)$ を $f$ の**導関数**といいます。「$f$ を微分する」とはこの操作のことです。

$f'(a) > 0$ のとき $x = a$ 付近でグラフは右上がり、
$f'(a) < 0$ のとき右下がり、
$f'(a) = 0$ のとき水平（山の頂上か谷の底の候補）。

---

## 基本的な導関数

| $f(x)$ | $f'(x)$ | 読み方・備考 |
|--------|---------|-------------|
| 定数 $c$ | $0$ | 定数は変化しない |
| $x^n$ | $nx^{n-1}$ | べき乗の微分（$n$ は実数で成立） |
| $e^x$ | $e^x$ | 自分自身が導関数になる唯一の基本関数 |
| $\ln x$ | $\dfrac{1}{x}$ | $x > 0$ で定義 |
| $\sin x$ | $\cos x$ | |
| $\cos x$ | $-\sin x$ | |

例：$f(x) = x^3$ のとき $f'(x) = 3x^2$。$x = 2$ での傾きは $3 \times 4 = 12$。

---

## 計算規則

**定数倍・和**：

$$(\alpha f)' = \alpha f', \quad (f + g)' = f' + g'$$

**積の微分法則**：

$$(f \cdot g)' = f'g + fg'$$

例：$(x^2 \cdot \sin x)' = 2x \cdot \sin x + x^2 \cdot \cos x$

**商の微分法則**：

$$\left(\frac{f}{g}\right)' = \frac{f'g - fg'}{g^2}$$

**連鎖律**（合成関数）：

$$(f \circ g)'(x) = f'(g(x)) \cdot g'(x)$$

例：$(\sin(x^2))' = \cos(x^2) \cdot 2x$

---

## 関連ページ

- [極限](../limits/introduction.md) — 微分の定義の基礎
- [積分](../integrals/introduction.md) — 微分の逆操作
- [一次関数](../linear/introduction.md) — 傾きが一定の関数
