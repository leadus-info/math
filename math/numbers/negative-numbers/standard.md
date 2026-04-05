---
title: 負数
description: "0 より小さい数と引き算"
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
    path: /math/numbers/natural-numbers/introduction.md
---

## 整数の定義

自然数 $\mathbb{N}$ に対して、各 $n \in \mathbb{N}$ の**負数** $-n$ と $0$ を加えた集合を**整数**といいます。

$$\mathbb{Z} = \{\ldots, -3, -2, -1, 0, 1, 2, 3, \ldots\}$$

$\mathbb{N} \subset \mathbb{Z}$（自然数は整数に含まれます）。

---

## 絶対値

**定義**：$a \in \mathbb{Z}$ の**絶対値**を次で定めます。

$$|a| = \begin{cases} a & (a \geq 0) \\ -a & (a < 0) \end{cases}$$

**性質**：
- $|a| \geq 0$（等号は $a = 0$ のとき）
- $|ab| = |a||b|$（積の絶対値は絶対値の積）
- $|a + b| \leq |a| + |b|$（**三角不等式**）

三角不等式は「2点間の距離は迂回路より短い」という直感に対応します。

---

## 加法と減法

**定義**：減法を加法で定義します。

$$a - b := a + (-b)$$

これにより $\mathbb{Z}$ は加法について閉じており（$a - b \in \mathbb{Z}$）、\
$\mathbb{N}$ では成立しなかった「任意の減法が可能」という性質を持ちます。

**例**：
$$3 - 5 = 3 + (-5) = -2$$
$$-4 - (-7) = -4 + 7 = 3$$
$$5 - (-3) = 5 + 3 = 8$$

---

## 乗法の符号規則

乗法の符号は次の規則に従います。

| 左 | 右 | 積 |
|----|----|----|
| 正 | 正 | 正 |
| 正 | 負 | 負 |
| 負 | 正 | 負 |
| 負 | 負 | **正** |

**なぜ負×負=正か？**\
分配法則から導けます。$(-1) \times (1 + (-1)) = (-1) \times 0 = 0$。\
左辺を展開すると $(-1) \times 1 + (-1) \times (-1) = -1 + (-1)(-1) = 0$。\
よって $(-1)(-1) = 1$。

**例**：
$$(-3) \times 4 = -12, \quad (-3) \times (-4) = 12$$
$$(-12) \div 3 = -4, \quad (-12) \div (-3) = 4$$

---

## 大小関係

$\mathbb{Z}$ にも全順序が入ります。$a < b \iff b - a \in \mathbb{N}$。

**重要**：負の数を掛けると不等号の向きが逆転します。

$$3 < 5 \implies (-2) \times 3 > (-2) \times 5 \quad (-6 > -10)$$

これは「$\times (-2)$ という操作が数直線上の向きを逆にする」ためです。

**例題**：不等式 $-2x + 1 > 5$ を解きます。\
$-2x > 4$ \
$x < -2$（$-2$ で割るので不等号が逆転）

---

## 整数の構造

$\mathbb{Z}$ は加法と乗法について次の性質を持ちます（**整域**）：
- 加法の単位元：$0$（$a + 0 = a$）
- 乗法の単位元：$1$（$a \times 1 = a$）
- 加法の逆元が常に存在：$a + (-a) = 0$
- 零因子なし：$ab = 0 \Rightarrow a = 0$ または $b = 0$

$\mathbb{N}$ では加法の逆元が存在しませんでしたが、$\mathbb{Z}$ では常に存在します。

---

## 関連ページ

- [自然数](../natural-numbers/introduction.md)
- [分数](../fractions/introduction.md) — 除法を閉じさせる拡張
- [不等号・不等式](../../math-language/inequalities/introduction.md)
