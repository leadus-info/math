---
title: 不等号・不等式
description: "不等式の解法と重要不等式"
goal: "一次・二次不等式・絶対値不等式を解き、AM-GM不等式などの重要不等式を使えるようになる"
tags: [math,math-language,inequalities]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数学の言語
    path: /math/math-language/index.md
  - title: 不等号・不等式
    path: /math/math-language/inequalities/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 不等号・不等式（入門）
    path: /math/math-language/inequalities/introduction.md
  - title: 負数（標準）
    path: /math/numbers/negative-numbers/standard.md
  - title: 二次関数（標準）
    path: /math/functions/quadratic/standard.md
---

## 一次不等式

一次不等式は等式と同じ手順で解けます。ただし負の数で割るとき不等号が逆転します。

**例題**：$-2x + 1 > 5$ を解いてください。

$-2x > 4$。両辺を $-2$ で割ると（逆転）$x < -2$。

**連立一次不等式**：複数の不等式を同時に満たす範囲を求めます。

**例題**：$\begin{cases} 2x - 1 > 3 \\ x + 4 < 10 \end{cases}$ を解いてください。

上：$x > 2$。下：$x < 6$。共通範囲：$2 < x < 6$。

---

## 二次不等式

$ax^2 + bx + c > 0$ の形の不等式です。二次関数のグラフを使って解きます。

$a > 0$ のとき、$f(x) = ax^2 + bx + c$ のグラフは下に開く放物線です。

- $D > 0$（解 $\alpha < \beta$）：$f(x) > 0$ の解は $x < \alpha$ または $x > \beta$
- $D = 0$（解 $\alpha$）：$f(x) > 0$ の解は $\alpha$ 以外のすべての実数
- $D < 0$：$f(x) > 0$ の解はすべての実数

**例題**：$x^2 - 3x + 2 > 0$ を解いてください。

$x^2 - 3x + 2 = (x-1)(x-2)$。解は $x = 1, 2$。よって不等式の解は $x < 1$ または $x > 2$。

---

## 絶対値不等式

$|x - a| < r$ は「$x$ と $a$ の距離が $r$ 未満」を意味します。

$$|x - a| < r \iff a - r < x < a + r$$

**例**：$|x - 3| < 2 \iff 1 < x < 5$

$|x - a| > r$ の場合は：

$$|x - a| > r \iff x < a - r \text{ または } x > a + r$$

---

## AM-GM 不等式

$a, b > 0$ のとき、

$$\frac{a + b}{2} \geq \sqrt{ab}$$

（等号は $a = b$ のとき）。「算術平均 $\geq$ 幾何平均」です。

**証明**：$(\sqrt{a} - \sqrt{b})^2 \geq 0$ を展開すると $a - 2\sqrt{ab} + b \geq 0$、整理して $\frac{a+b}{2} \geq \sqrt{ab}$。$\square$

**応用例**：$x > 0$ のとき $x + \frac{1}{x} \geq 2$（$a = x$、$b = \frac{1}{x}$ とすると $\frac{x + 1/x}{2} \geq \sqrt{x \cdot 1/x} = 1$）。

---

## 関連ページ

- [二次関数（標準）](../../functions/quadratic/standard.md)
- [不等号・不等式（専門）](professional.md)
