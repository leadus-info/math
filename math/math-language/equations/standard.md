---
title: 等号・等式
description: "「等しい」を記号で表す"
tags: [math,math-language,equations]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数学の言語
    path: /math/math-language/index.md
  - title: 等号・等式
    path: /math/math-language/equations/standard.md
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
---

## 等号の性質

等号 $=$ は次の三つの性質を持ちます。

- **反射律**：$a = a$
- **対称律**：$a = b \Rightarrow b = a$
- **推移律**：$a = b$ かつ $b = c$ ならば $a = c$

これらは等号が**同値関係**であることを示します。

また、等式は両辺に同じ操作をしても保たれます。

$$a = b \Rightarrow a + c = b + c$$
$$a = b \Rightarrow a \times c = b \times c$$

ただし乗法では $c = 0$ のとき情報が失われるので注意が必要です\
（$0 \times a = 0 \times b$ は $a \neq b$ でも成り立つ）。

---

## 恒等式と方程式

**定義（恒等式）**：変数のすべての値で成り立つ等式。\
$(x+y)^2 = x^2 + 2xy + y^2$ は任意の実数 $x, y$ で成立します。

**定義（方程式）**：特定の値でのみ成り立つ等式。\
その値を**解（根）**といいます。

**一次方程式**（解が一つ）：

$$2x + 3 = 7 \implies 2x = 4 \implies x = 2$$

---

## 二次方程式

$$ax^2 + bx + c = 0 \quad (a \neq 0)$$

**解の公式**：

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

**導出**（平方完成）：\
$a\left(x + \frac{b}{2a}\right)^2 = \frac{b^2 - 4ac}{4a}$ と変形し、両辺を $a$ で割って平方根を取ります。

**判別式** $D = b^2 - 4ac$ で実数解の個数が決まります。

| $D > 0$ | 異なる2実数解 |
| $D = 0$ | 重解（1実数解） |
| $D < 0$ | 実数解なし |

**例題**：$x^2 - 5x + 6 = 0$ を解いてください。\
$D = 25 - 24 = 1 > 0$ なので解は2つ。\
$x = \frac{5 \pm 1}{2}$ より $x = 3$ または $x = 2$。\
確認：$(x-2)(x-3) = 0$ と因数分解しても同じ結果。

---

## 連立方程式

複数の等式を同時に満たす未知数を求めます。

**例**：$\begin{cases} 2x + y = 5 \\ x - y = 1 \end{cases}$

2式を加算：$3x = 6 \Rightarrow x = 2$\
代入：$y = 5 - 4 = 1$\
解：$(x, y) = (2, 1)$

---

## 関連ページ

- [不等号・不等式](../inequalities/introduction.md)
- [代数](../algebra/introduction.md)
