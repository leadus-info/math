---
title: 二次関数
description: "放物線を描く関数"
goal: "二次関数の定義・主要な定理・代表的な計算を理解し、後続のトピックに進める基礎を身につける"
tags: [math,specific-functions,quadratic]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 具体的な関数
    path: /math/specific-functions/index.md
  - title: 二次関数
    path: /math/specific-functions/quadratic/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 一次関数
    path: /math/specific-functions/linear/introduction.md
  - title: 代数
    path: /math/algebra/expressions/introduction.md
---

## 二次関数の定義

**定義**：$f(x) = ax^2 + bx + c$（$a \neq 0$）を**二次関数**といいます。

- $a > 0$：下に開く（$\cup$ 形）
- $a < 0$：上に開く（$\cap$ 形）

---

## 平方完成と頂点

$$f(x) = a\left(x + \frac{b}{2a}\right)^2 - \frac{b^2 - 4ac}{4a}$$

頂点は $\left(-\dfrac{b}{2a},\ -\dfrac{b^2-4ac}{4a}\right)$ です。

**例題**：$f(x) = x^2 + 4x + 1$ を平方完成します。

$$f(x) = (x+2)^2 - 4 + 1 = (x+2)^2 - 3$$

頂点は $(-2, -3)$。

---

## 判別式

二次方程式 $ax^2 + bx + c = 0$ の解の公式：

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

判別式 $D = b^2 - 4ac$ の符号でグラフの $x$ 軸との交点が決まります。

| $D > 0$ | 2点で交わる |
| $D = 0$ | 1点で接する（重解） |
| $D < 0$ | 交わらない |

**例題**：$x^2 - 5x + 6 = 0$。$D = 25 - 24 = 1 > 0$。$x = \dfrac{5 \pm 1}{2}$ より $x = 3, 2$。

---

## 二次不等式

$a > 0$、解 $\alpha < \beta$ のとき：

$$ax^2 + bx + c < 0 \iff \alpha < x < \beta$$
$$ax^2 + bx + c > 0 \iff x < \alpha \text{ または } x > \beta$$

---

## 関連ページ

- [二次関数（入門）](introduction.md)
- [多項式（標準）](../../algebra/polynomials/standard.md)
