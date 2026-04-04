---
title: 数列
description: "級数の収束判定・べき級数・漸近展開"
tags: [math,functions,sequences]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 関数
    url: /math/functions/index.html
  - title: 数列
    url: /math/functions/sequences/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: 数列
    url: /math/functions/sequences/introduction
  - title: 極限（専門）
    url: ../../limits/professional.md
  - title: 微分
    url: /math/functions/derivatives/introduction
---


> この記事は [標準](standard.md) の続きです。先に標準を読むことを推奨します。

級数の収束判定・べき級数・漸近展開を扱います。

## このページで扱うこと
- 収束判定法（比率・根・積分・交代）
- べき級数と収束半径
- 漸近展開と発散級数

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

- [数列](introduction.md)
- [複素関数](introduction.md)
- [三角関数（専門）](../trigonometric/professional.md)
