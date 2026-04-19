---
title: 指数関数
description: "倍々で増える関数"
goal: "指数関数の定義・主要な定理・代表的な計算を理解し、後続のトピックに進める基礎を身につける"
tags: [math,specific-functions,exponential]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 具体的な関数
    path: /math/specific-functions/index.md
  - title: 指数関数
    path: /math/specific-functions/exponential/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 四則演算
    path: professional.md
  - title: 一次関数
    path: /math/specific-functions/linear/introduction.md
---

## 指数関数の定義

**定義**：底 $a > 0$、$a \neq 1$ の**指数関数**を $f(x) = a^x$ とします。

---

## グラフの特徴

| | $a > 1$ | $0 < a < 1$ |
|--|---------|-------------|
| 形状 | 右上がり（増加） | 右下がり（減少） |
| $y$ 切片 | $(0, 1)$（どちらも） | $(0, 1)$（どちらも） |
| 漸近線 | $y = 0$（$x \to -\infty$） | $y = 0$（$x \to +\infty$） |

$a^0 = 1$ なので $y$ 切片は常に1。$a^x > 0$ なので $x$ 軸と交わりません。

---

## 指数法則

$$a^m \cdot a^n = a^{m+n}, \quad (a^m)^n = a^{mn}, \quad a^{-n} = \frac{1}{a^n}, \quad a^{1/n} = \sqrt[n]{a}$$

---

## ネイピア数 $e$

$$e = \lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n \approx 2.71828\ldots$$

$e$ は「微分しても変わらない」という特別な性質を持ちます：$(e^x)' = e^x$。この性質から自然界の成長・減衰の記述に自然に登場します。

---

## 指数方程式

底を揃えて指数を比較します。

$$4^x = 8 \Rightarrow (2^2)^x = 2^3 \Rightarrow 2x = 3 \Rightarrow x = \frac{3}{2}$$

底が1より大きいとき、$a^x > a^y \iff x > y$。底が0と1の間なら不等号が逆転します。

---

## 関連ページ

- [指数関数（入門）](introduction.md)
- [対数関数（標準）](../logarithmic/standard.md)
- [微分（標準）](../../analysis/derivatives/standard.md)
