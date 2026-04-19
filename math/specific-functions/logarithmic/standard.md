---
title: 対数関数
description: "指数関数の逆の操作"
goal: "対数関数の定義・主要な定理・代表的な計算を理解し、後続のトピックに進める基礎を身につける"
tags: [math,specific-functions,logarithmic]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 具体的な関数
    path: /math/specific-functions/index.md
  - title: 対数関数
    path: /math/specific-functions/logarithmic/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 指数関数
    path: /math/specific-functions/exponential/introduction.md
---

## 対数の定義

**定義**：$a > 0$、$a \neq 1$、$x > 0$ のとき、$a^y = x$ を満たす $y$ を**$a$ を底とする $x$ の対数**といい、$y = \log_a x$ と書きます。

$$\log_a x = y \iff a^y = x$$

$$\log_2 8 = 3 \quad (\text{なぜなら } 2^3 = 8)$$

---

## 対数の計算規則

$$\log_a(MN) = \log_a M + \log_a N$$
$$\log_a\frac{M}{N} = \log_a M - \log_a N$$
$$\log_a M^r = r\log_a M$$
$$\log_a 1 = 0, \quad \log_a a = 1$$

「掛け算→足し算、割り算→引き算、べき乗→掛け算」に変換します。

**底の変換公式**：$\log_a x = \dfrac{\log_b x}{\log_b a}$

---

## グラフの特徴

- 定義域：$x > 0$
- $x$ 切片：$(1, 0)$（$\log_a 1 = 0$ のため）
- 漸近線：$y$ 軸（$x \to 0^+$ で $\pm\infty$）
- $a > 1$ なら増加、$0 < a < 1$ なら減少

指数関数 $y = a^x$ と $y = x$ に関して対称なグラフです。

---

## 自然対数 $\ln$

底が $e$ の対数を**自然対数**といい $\ln x$ と書きます。

$$(\ln x)' = \frac{1}{x}, \quad \int \frac{1}{x}\,dx = \ln|x| + C$$

---

## 対数方程式

**真数が正であることを必ず確認**してから解きます。

**例題**：$\log_2(x+1) = 3$。$x+1 = 2^3 = 8$、$x = 7$（$x+1 = 8 > 0$ を確認）。

---

## 関連ページ

- [対数関数（入門）](introduction.md)
- [指数関数（標準）](../exponential/standard.md)
