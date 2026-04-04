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
    url: professional.md
  - title: 乗法・べき乗
    url: professional.md
---



車のスピードメーターは「今この瞬間の速さ」を示します。
**微分**は、関数の「その瞬間の変化の速さ」を求める操作です。

## このページで扱うこと
- 微分の直感（平均の変化率 → 瞬間の変化率）
- 導関数の定義
- よく使う微分の公式と計算規則

---

## 平均の変化率

$x$ が $a$ から $b$ まで変化するとき：

$$\frac{f(b) - f(a)}{b - a}$$

これはグラフ上の 2 点を結ぶ直線の傾きです。

---

## 瞬間の変化率（微分）

2 点を限りなく近づけると、傾きは接線の傾きに近づきます。

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

---

## よく使う微分の公式

| 元の関数 $f(x)$ | 微分 $f'(x)$ |
|-----------------|-------------|
| 定数 $c$ | $0$ |
| $x^n$ | $nx^{n-1}$ |
| $e^x$ | $e^x$ |
| $\ln x$ | $\dfrac{1}{x}$ |
| $\sin x$ | $\cos x$ |
| $\cos x$ | $-\sin x$ |

---

## 計算規則

$$(f + g)' = f' + g'$$
$$(f \cdot g)' = f'g + fg'$$
$$\left(\frac{f}{g}\right)' = \frac{f'g - fg'}{g^2}$$
$$(f \circ g)'(x) = f'(g(x)) \cdot g'(x) \quad \text{（連鎖律）}$$

---

## グラフでの意味

- $f'(a) > 0$ → $x = a$ 付近で右上がり
- $f'(a) < 0$ → $x = a$ 付近で右下がり
- $f'(a) = 0$ → 頂点・谷底の候補

---

## 関連ページ

- [積分](professional.md)
- [極限](professional.md)
- [一次関数](professional.md) — 傾きが一定の関数
- [微分（専門）](professional.md) — 多変数微分・フレシェ微分
