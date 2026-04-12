---
title: 負数
description: "整数の演算と符号の規則"
goal: "整数の四則演算・符号規則・絶対値の性質・不等式における符号の扱いを理解し、後続のトピックに進める基礎を身につける"
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
  - title: 自然数（標準）
    path: /math/numbers/natural-numbers/standard.md
  - title: 負数（入門）
    path: /math/numbers/negative-numbers/introduction.md
---

## 整数の定義

自然数 $\mathbb{N} = \{1, 2, 3, \ldots\}$ に、各自然数 $n$ の負数 $-n$ と $0$ を加えた集合を**整数**といいます。

$$\mathbb{Z} = \{\ldots, -3, -2, -1, 0, 1, 2, 3, \ldots\}$$

$\mathbb{N} \subset \mathbb{Z}$（自然数は整数に含まれます）。

---

## 減法を加法で書く

負数（入門）では、負の数を足すことが引き算と同じ効果を持つことを見ました。これを一般的に書くと、

$$a - b = a + (-b)$$

です。引き算は「$-b$（$b$ の符号を反転した数）を足す操作」として定義できます。

この定義により、整数の世界では引き算がいつでも可能です。$a - b$ は $a, b$ がどんな整数でも必ず整数になります。

**例**：
- $3 - 5 = 3 + (-5) = -2$
- $-4 - (-7) = -4 + 7 = 3$
- $5 - (-3) = 5 + 3 = 8$

---

## 掛け算の符号規則

正の数と負の数を掛けるとき、答えの符号はどうなるでしょうか。

「$(-3)$ を4回足す」と考えると、$(-3) + (-3) + (-3) + (-3) = -12$ です。

$$(-3) \times 4 = -12$$

正の数と負の数を掛けると、答えは負になります。では、負の数同士の掛け算はどうでしょうか。

自然数（標準）で見た分配法則 $a \times (b + c) = a \times b + a \times c$ が整数でも成り立つとすると、

$$(-1) \times (1 + (-1)) = (-1) \times 0 = 0$$

左辺を展開すると $(-1) \times 1 + (-1) \times (-1) = -1 + (-1) \times (-1) = 0$。

よって $(-1) \times (-1) = 1$ です。負の数同士を掛けると正になります。

まとめると、

- 正 $\times$ 正 $=$ 正
- 正 $\times$ 負 $=$ 負
- 負 $\times$ 正 $=$ 負
- 負 $\times$ 負 $=$ 正

**例**：$(-3) \times (-4) = 12$、$(-2) \times 5 = -10$

割り算の符号も同じ規則に従います。$(-12) \div 3 = -4$、$(-12) \div (-3) = 4$。

---

## 絶対値の性質

負数（入門）で、絶対値は「0からの距離」であると見ました。正確に書くと、

$$|a| = \begin{cases} a & (a \geq 0) \\ -a & (a < 0) \end{cases}$$

絶対値は以下の性質を持ちます。

- $|a| \geq 0$（等号は $a = 0$ のとき）
- $|a \times b| = |a| \times |b|$（積の絶対値は絶対値の積）
- $|a + b| \leq |a| + |b|$（**三角不等式**）

三角不等式は「2点間を直線で結ぶ距離は、別の点を経由する距離以下」という直感に対応します。

---

## 不等式と負の数

整数の大小関係は、$a < b \iff b - a$ が正の数、で定められます。

負の数を掛けると不等号の向きが逆転します。

$$3 < 5$$

両辺に $-2$ を掛けると、

$$(-2) \times 3 > (-2) \times 5 \quad \text{すなわち} \quad -6 > -10$$

これは数直線上で考えると分かります。負の数を掛けることは、0を中心に数直線を反転させる操作です。反転すれば左右が入れ替わるので、不等号の向きが逆になります。

**例題**：不等式 $-2x + 1 > 5$ を解きます。

$-2x > 4$。両辺を $-2$ で割ると（不等号が逆転）、$x < -2$。

---

## 関連ページ

- [自然数（標準）](../natural-numbers/standard.md)
- [分数（入門）](../fractions/introduction.md) — 割り算を整数の外へ拡張する
- [不等号・不等式（入門）](../../math-language/inequalities/introduction.md)