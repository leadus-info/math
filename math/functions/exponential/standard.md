---
title: 指数関数
description: "倍々で増える変化を表す関数"
difficulty: 2
tags: [math,functions,exponential]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 指数関数
    href: /math/functions/exponential/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 指数関数
$1$ 円を毎年 $2$ 倍にすると、$10$ 年後は $1024$ 円、$20$ 年後は約 $100$ 万円——
**指数関数**は「倍々で増える（または減る）変化」を表す関数です。

## このページで扱うこと
- 指数関数の定義とグラフ
- $e$（ネイピア数）とは何か
- 指数方程式の解き方

## 前提知識
- [乗法・べき乗](../../numbers/arithmetic/standard.md)
- [一次関数](../linear/standard.md)

---

## 指数関数とは？

$$f(x) = 2^x$$

| $x$ | $-2$ | $-1$ | $0$ | $1$ | $2$ | $3$ |
|-----|------|------|-----|-----|-----|-----|
| $2^x$ | $\frac{1}{4}$ | $\frac{1}{2}$ | $1$ | $2$ | $4$ | $8$ |

$x$ が $1$ 増えるたびに $2$ 倍になります。

一般に $f(x) = a^x$（$a > 0$、$a \neq 1$）。

---

## グラフの特徴

| | $a > 1$（例：$2^x$） | $0 < a < 1$（例：$(0.5)^x$） |
|-|---------------------|------------------------------|
| 形 | 右上がりで急増 | 右下がりで急減 |
| $y$ 切片 | $(0,\ 1)$（$a^0 = 1$） | $(0,\ 1)$ |
| 漸近線 | $y = 0$（$x$ 軸）に近づくが触れない | $y = 0$ に近づくが触れない |

---

## ネイピア数 $e$

$$e = 2.71828\ldots$$

特別な底で、**微分してもそのまま**という性質を持ちます。

$$\frac{d}{dx}e^x = e^x$$

自然界の成長・減衰（人口増加・放射性崩壊など）を表すのによく使われます。

---

## 指数方程式

**底を揃える**ことで解けます。

$$2^x = 8 = 2^3 \implies x = 3$$
$$3^{x+1} = 81 = 3^4 \implies x + 1 = 4 \implies x = 3$$

底が揃わないときは[対数関数](../logarithmic/standard.md)を使います。

---

## 関連ページ

- [対数関数](../logarithmic/standard.md) — 指数関数の逆
- [指数関数（発展）](../exponential/advanced.md) — より詳しく学ぶ
