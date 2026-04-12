---
title: 不等号・不等式
description: "大小関係を表す記号"
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
  - title: 等号・等式
    path: /math/math-language/equations/introduction.md
  - title: 負数
    path: /math/numbers/negative-numbers/introduction.md
---

## 不等号の定義

**定義**：実数 $a, b$ に対して：

- $a < b$：数直線上で $a$ が $b$ より左にある（$b - a > 0$）
- $a \leq b$：$a < b$ または $a = b$

---

## 不等式の変形ルール

**定理**：次の変形をしても不等号の向きは変わりません。
1. 両辺に同じ数を加える（引く）：$a < b \Rightarrow a + c < b + c$
2. 両辺に**正の数**を掛ける（割る）：$a < b$、$c > 0 \Rightarrow ac < bc$

**定理**：次の変形では不等号の向きが**逆になります**。
3. 両辺に**負の数**を掛ける（割る）：$a < b$、$c < 0 \Rightarrow ac > bc$

**なぜ負の数を掛けると逆転するか**：\
数直線上で $-1$ 倍すると左右が入れ替わるためです。\
$3 < 5$ の両辺を $-1$ 倍すると $-3 > -5$（$-5$ の方が左にある）。

---

## 一次不等式の解き方

$$-2x + 1 > 5$$
$$-2x > 4$$
$$x < -2 \quad \text{（$-2$ で割るので向き逆転）}$$

解は「$x$ が満たすべき範囲」です。$x < -2$ は数直線上の半直線で表せます。

---

## 絶対値不等式

**定理**：$k > 0$ のとき

$$|x - a| < k \iff a - k < x < a + k$$

「$x$ と $a$ の距離が $k$ 未満」という意味です。

**例**：$|x - 2| < 3 \iff -1 < x < 5$

**例題**：$|2x - 1| \leq 5$ を解きます。\
$-5 \leq 2x - 1 \leq 5$\
$-4 \leq 2x \leq 6$\
$-2 \leq x \leq 3$

---

## 連立不等式

複数の不等式を同時に満たす範囲を求めます。

**例題**：$\begin{cases} x + 1 > 3 \\ 2x - 4 < 6 \end{cases}$ を解きます。

上：$x > 2$\
下：$x < 5$\
共通部分：$2 < x < 5$

---

## 関連ページ

- [等号・等式](../equations/introduction.md)
- [必要・十分条件](../conditions/introduction.md)
