---
title: 指数関数
description: "倍々で増える変化を表す関数"
goal: "指数関数の定義とグラフの特徴を理解し、指数法則を使って指数方程式を解けるようになる"
tags: [math, specific-functions, exponential]
stage: 応用編
subject: 具体的な関数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 応用編
    path: /math/advanced/index.md
  - title: 指数関数
    path: /math/advanced/specific-functions/exponential.md
requires:
  - title: 乗法・べき乗
    path: /math/intermediate/numbers/arithmetic.md
  - title: 一次関数
    path: /math/advanced/specific-functions/linear.md
---

## 倍々で増える

「毎日2倍になる細菌がいる。今日1匹なら、10日後は？」

| 日 | 1日目 | 2日目 | 3日目 | 4日目 | 5日目 |
|----|-------|-------|-------|-------|-------|
| 匹数 | 2 | 4 | 8 | 16 | 32 |

10日後は $2^{10} = 1024$ 匹になります。「毎日2匹ずつ増える」場合（10日後は21匹）と比べると、その差は圧倒的です。このように「一定の割合で増え続ける」変化を表す関数が**指数関数**です。

---

## 指数関数の定義

**定義**：底 $a > 0$、$a \neq 1$ の**指数関数**を $f(x) = a^x$ とします。

| | $a > 1$ | $0 < a < 1$ |
|--|---------|-------------|
| 形状 | 右上がり（増加） | 右下がり（減少） |
| $y$ 切片 | $(0, 1)$ | $(0, 1)$ |
| 漸近線 | $y = 0$（$x \to -\infty$） | $y = 0$（$x \to +\infty$） |

$a^0 = 1$ なので $y$ 切片は常に1。$a^x > 0$ なので $x$ 軸とは交わりません。

---

## 指数法則

$$a^m \cdot a^n = a^{m+n}, \quad (a^m)^n = a^{mn}, \quad a^{-n} = \frac{1}{a^n}, \quad a^{1/n} = \sqrt[n]{a}$$

---

## ネイピア数 $e$

$$e = \lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n \approx 2.71828\ldots$$

$e$ は「微分しても変わらない」という特別な性質を持ちます：$(e^x)' = e^x$。この性質から、自然界の成長・減衰の記述に自然に登場します。

---

## 指数方程式

底を揃えて指数を比較します。

$$4^x = 8 \Rightarrow (2^2)^x = 2^3 \Rightarrow 2x = 3 \Rightarrow x = \frac{3}{2}$$

底が1より大きいとき、$a^x > a^y \iff x > y$。底が0と1の間なら不等号が逆転します。

---

## 身の回りの例

- **複利**：元金が毎年一定の割合で増える
- **放射性物質の半減期**：一定時間ごとに量が半分になる
- **感染症の初期拡大**：感染者が一定の割合で増える

---

## まとめ

指数関数 $f(x) = a^x$ は「一定の割合で増減する」変化を表します。変化のスピード自体が変わっていくのが特徴で、指数法則を使って指数方程式を解いたり式を整理したりできます。

---

## 関連ページ

- [対数関数（応用編）](logarithmic.md)
- [微分（応用編）](/math/advanced/analysis/derivatives.md)
