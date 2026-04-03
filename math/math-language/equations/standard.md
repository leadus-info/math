---
title: 等号・等式
description: "「等しい」を記号で表す"
difficulty: 1
tags: [math,math-language,equations]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数学の言語
    href: /math/math-language/index.html
  - text: 等号・等式
    href: /math/math-language/equations/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 等号・等式
「左の量と右の量は同じ」——これを数学の記号で表したのが**等号** $=$ です。

## このページで扱うこと
- 等号の意味と使い方
- 方程式とは（答えを求める等式）
- 一次方程式・二次方程式の解き方

## 前提知識
- [乗法・べき乗](../../numbers/arithmetic/standard.md)

---

## 等号とは？

$$3 + 4 = 7$$

「左辺（$3+4$）と右辺（$7$）は同じ値」という意味です。

等号には大切な性質があります。

**両辺に同じことをしても等号は保たれる**

$$3 + 4 = 7 \implies (3 + 4) \times 2 = 7 \times 2 \quad (14 = 14)$$

これが方程式を解くときの基本です。

---

## 方程式とは？

$$x + 3 = 8$$

$x$ に特定の値を入れたときだけ成り立つ等式を**方程式**といいます。
「どんな値でも成り立つ等式（恒等式）」とは違います。

$$x + 3 = 8 \implies x = 5$$

---

## 一次方程式の解き方

「$x$ だけを左辺に残す」のが基本です。

$$2x + 3 = 7$$

両辺から $3$ を引く：

$$2x = 4$$

両辺を $2$ で割る：

$$x = 2$$

---

## 二次方程式の解き方

$$ax^2 + bx + c = 0$$

解の公式：

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

$b^2 - 4ac$（**判別式**）の値によって解の個数が変わります。

| 判別式 | 解の数 |
|--------|--------|
| 正 | $2$ 個 |
| $0$ | $1$ 個（ちょうど $x$ 軸に接する） |
| 負 | 実数の解なし |

---

## 関連ページ

- [不等号・不等式](../inequalities/standard.md)
- [代数](../algebra/standard.md)
- [等号・等式（発展）](../equations/advanced.md) — より詳しく学ぶ
