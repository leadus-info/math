---
title: 数列
description: "級数の収束判定・べき級数・漸近展開"
goal: "数列を厳密に定義し、主要な定理を証明できるようになる"
tags: [math,analysis,sequences]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/analysis/index.md
  - title: 数列
    path: /math/analysis/sequences/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 数列
    path: /math/analysis/sequences/introduction.md
  - title: 極限（専門）
    path: /math/analysis/limits/professional.md
  - title: 微分
    path: /math/analysis/derivatives/introduction.md
---

## 級数の収束判定

無限級数 $\displaystyle\sum_{n=1}^\infty a_n$ の収束判定法：

| 判定法 | 条件 |
|--------|------|
| 比率判定 | $\lim\left|\dfrac{a_{n+1}}{a_n}\right| < 1$ → 絶対収束 |
| 根判定 | $\limsup|a_n|^{1/n} < 1$ → 絶対収束 |
| 積分判定 | $\int_1^\infty f(x)\,dx$ の収束と同値（$f$ 単調減少） |
| ライプニッツ | 交代級数で $|a_n| \searrow 0$ → 収束 |

---

## べき級数と収束半径

$$\sum_{n=0}^\infty a_n(x-a)^n$$

**収束半径**：$R = \dfrac{1}{\limsup_{n\to\infty} |a_n|^{1/n}}$（アダマールの公式）

$|x-a| < R$ で絶対収束、$|x-a| > R$ で発散。端点は個別に判定が必要です。

べき級数は収束域内で無限回微分可能で、項別微分・積分が可能です。

---

## テイラー展開

$f$ が $a$ の周りで無限回微分可能なら：

$$f(x) = \sum_{n=0}^\infty \frac{f^{(n)}(a)}{n!}(x-a)^n$$

（ただし収束は別途確認が必要）

$$e^x = \sum_{n=0}^\infty \frac{x^n}{n!}, \quad \sin x = \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!}$$

---

## スターリング近似

$$n! \sim \sqrt{2\pi n}\left(\frac{n}{e}\right)^n \quad (n \to \infty)$$

発散するが有限項で打ち切ると良い近似を与える「漸近級数」の例です。

**参考文献**：Knopp, K. (1956). *Infinite Sequences and Series*. Dover.

---

## 関連ページ

- [数列（標準）](standard.md)
- [複素関数（専門）](../complex-analysis/professional.md)
