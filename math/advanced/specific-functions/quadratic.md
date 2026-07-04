---
title: 二次関数
description: "グラフが放物線になる関数"
goal: "二次関数の定義と平方完成による頂点の求め方を理解し、判別式を使ってグラフとx軸の関係を説明できるようになる"
tags: [math, specific-functions, quadratic]
stage: 応用編
subject: 具体的な関数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 応用編
    path: /math/advanced/index.md
  - title: 二次関数
    path: /math/advanced/specific-functions/quadratic.md
requires:
  - title: 一次関数
    path: /math/advanced/specific-functions/linear.md
  - title: 代数
    path: /math/intermediate/algebra/expressions.md
---

## 放物線という形

ボールを斜めに投げると、弧を描いて飛びます。この弧の形が**放物線**です。噴水の水の軌跡や、橋のアーチにも同じ形があります。

一次関数では「$x$ が1増えるたびに $y$ が一定量増える」でした。二次関数では、変化量そのものが変わっていきます。$y = x^2$ を見ると、$x$ が $0,1,2,3,4$ と増えるとき $y$ の増え方は $1,3,5,7$ と大きくなり、一定ではなく加速しています。

---

## 二次関数の定義

**定義**：$f(x) = ax^2 + bx + c$（$a \neq 0$）を**二次関数**といいます。

- $a > 0$：下に開く（$\cup$ 形）
- $a < 0$：上に開く（$\cap$ 形）

---

## 平方完成と頂点

放物線には必ず「一番高い点」または「一番低い点」があり、これを**頂点**といいます。頂点は式を変形すると求められます。

$$f(x) = a\left(x + \frac{b}{2a}\right)^2 - \frac{b^2 - 4ac}{4a}$$

頂点は $\left(-\dfrac{b}{2a},\ -\dfrac{b^2-4ac}{4a}\right)$ です。

**例題**：$f(x) = x^2 + 4x + 1$ を平方完成する。$f(x) = (x+2)^2 - 4 + 1 = (x+2)^2 - 3$。頂点は $(-2, -3)$。

---

## 判別式

二次方程式 $ax^2 + bx + c = 0$ の解の公式 $x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a}$ において、判別式 $D = b^2 - 4ac$ の符号でグラフと $x$ 軸との関係が決まります。

| $D$ の符号 | グラフと $x$ 軸の関係 |
|---|---|
| $D > 0$ | 2点で交わる |
| $D = 0$ | 1点で接する（重解） |
| $D < 0$ | 交わらない |

**例題**：$x^2 - 5x + 6 = 0$。$D = 25 - 24 = 1 > 0$。$x = \dfrac{5 \pm 1}{2}$ より $x = 3, 2$。

---

## 二次不等式

$a > 0$、解 $\alpha < \beta$（$D>0$ のとき）のグラフを使うと、次のように解けます。

$$ax^2 + bx + c < 0 \iff \alpha < x < \beta$$
$$ax^2 + bx + c > 0 \iff x < \alpha \text{ または } x > \beta$$

---

## まとめ

二次関数のグラフは放物線で、頂点が最大値・最小値を与えます。平方完成で頂点の座標がわかり、判別式でグラフと $x$ 軸との交点の個数がわかります。

---

## 関連ページ

- [一次関数（応用編）](linear.md)
- [多項式（応用編）](/math/advanced/algebra/polynomials.md)
