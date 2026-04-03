---
title: 数列（専門）
description: "級数の収束判定・べき級数・漸近展開"
difficulty: 5
tags: [math,functions,sequences,professional]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 数列（専門）
    href: /math/functions/sequences/professional.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
    href: advanced.html
  - text: 専門
---








# 数列（発展）
級数の収束判定・べき級数・漸近展開を扱います。

## このページで扱うこと
- 収束判定法（比率・根・積分・交代）
- べき級数と収束半径
- 漸近展開と発散級数

## 前提知識
- [数列](../sequences/standard.md)
- [極限（専門）](../calculus/limits/professional.md)
- [微分](../calculus/derivatives/standard.md)

---

## 収束判定法

| 判定法 | 条件 |
|--------|------|
| 比率判定 | $\lim|a_{n+1}/a_n| < 1$ → 収束 |
| 根判定 | $\limsup|a_n|^{1/n} < 1$ → 収束 |
| 積分判定 | $\int_1^\infty f(x)dx$ の収束と同値 |
| ライプニッツ | 交代級数で $|a_n| \searrow 0$ → 収束 |

---

## べき級数と収束半径

$$\sum_{n=0}^{\infty} a_n(x-a)^n$$

収束半径: $R = 1/\limsup|a_n|^{1/n}$

$|x-a| < R$ で絶対収束、$|x-a| > R$ で発散。

---

## 漸近展開

$n \to \infty$ でのスターリング近似:

$$n! \sim \sqrt{2\pi n}\left(\frac{n}{e}\right)^n$$

（発散するが有限項で打ち切ると良い近似を与える「漸近級数」）

---

## 関連ページ

- [数列](../sequences/standard.md)
- [複素関数](../calculus/complex-functions/standard.md)
- [三角関数（専門）](../trigonometric/professional.md)
