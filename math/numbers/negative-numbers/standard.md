---
title: 負数
description: "整数の演算と符号の規則"
goal: "整数の四則演算の規則を正確に述べ、符号を含む計算ができるようになる"
tags: [math,numbers,negative-numbers]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 負数
    path: /math/numbers/negative-numbers/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 自然数
    path: /math/numbers/natural-numbers/standard.md
  - title: 負数
    path: /math/numbers/negative-numbers/introduction.md
---

## 整数の定義

自然数 $\mathbb{N}$ に対して、各 $n \in \mathbb{N}$ の**負数** $-n$ と $0$ を加えた集合を**整数**といいます。

$$\mathbb{Z} = \{\ldots, -3, -2, -1, 0, 1, 2, 3, \ldots\}$$

$\mathbb{N} \subset \mathbb{Z}$ です。自然数では引き算が常にはできませんでしたが、整数では任意の二数の差が整数になります。

---

## 加法の逆元

任意の整数 $a$ に対して、$a + (-a) = 0$ を満たす整数 $-a$ が存在します。この $-a$ を $a$ の**加法の逆元**といいます。

逆元の存在により、減法は加法で定義できます。

$$a - b := a + (-b)$$

**例**：

$$3 - 5 = 3 + (-5) = -2$$
$$-4 - (-7) = -4 + 7 = 3$$
$$5 - (-3) = 5 + 3 = 8$$

---

## 絶対値

**定義**：$a \in \mathbb{Z}$ の**絶対値**を次で定めます。

$$|a| = \begin{cases} a & (a \geq 0) \\ -a & (a < 0) \end{cases}$$

絶対値は数直線上での $0$ からの距離を表します。$|-5| = 5$、$|3| = 3$ です。

**性質**：

- $|a| \geq 0$（等号は $a = 0$ のとき）
- $|ab| = |a||b|$
- $|a + b| \leq |a| + |b|$（**三角不等式**）

三角不等式は「2点間の距離は迂回路より短い」という直感に対応します。

---

## 乗法の符号規則

乗法の符号は次の規則に従います。

| 左 | 右 | 積 |
|----|----|----|
| 正 | 正 | 正 |
| 正 | 負 | 負 |
| 負 | 正 | 負 |
| 負 | 負 | **正** |

**なぜ負×負＝正か？** 分配法則から導けます。$(-1) \times (1 + (-1)) = (-1) \times 0 = 0$。左辺を展開すると $(-1) \times 1 + (-1) \times (-1) = -1 + (-1)(-1) = 0$。よって $(-1)(-1) = 1$ です。

**例**：$(-3) \times 4 = -12$、$(-3) \times (-4) = 12$

除法の符号も同じ規則です。$(-12) \div 3 = -4$、$(-12) \div (-3) = 4$。

---

## 大小関係と不等号の逆転

$\mathbb{Z}$ にも全順序が入ります。$a < b \iff b - a \in \mathbb{N}$ です。

**重要**：負の数を掛けると不等号の向きが逆転します。

$$3 < 5 \implies (-2) \times 3 > (-2) \times 5 \quad (-6 > -10)$$

これは数直線上で「負の数を掛ける操作」が左右を反転させることに対応します。

**例題**：不等式 $-2x + 1 > 5$ を解きます。$-2x > 4$、$-2$ で割ると不等号が逆転して $x < -2$。

---

## 関連ページ

- [自然数（標準）](../natural-numbers/standard.md)
- [分数](../fractions/introduction.md) — 除法を閉じさせる拡張
- [不等号・不等式](../../math-language/inequalities/introduction.md)