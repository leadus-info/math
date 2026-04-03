---
title: 対数関数（発展）
description: "指数関数の逆の操作（発展）"
difficulty: 3
tags: [math,functions,logarithmic,advanced]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 対数関数（発展）
    href: /math/functions/logarithmic/advanced.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
  - text: 専門
    href: professional.html
---







# 対数関数
「2 を何乗すれば 8 になるか？」——この問いの答えが**対数**です。
指数関数の逆の操作です。

## このページで扱うこと
- 対数の定義と読み方
- 計算規則（掛け算 → 足し算）
- グラフの特徴と対数方程式

## 前提知識
- [指数関数](professional.md)

---

## 定義

$$y = \log_a x \iff a^y = x$$

$$\log_2 8 = 3 \quad (\text{なぜなら } 2^3 = 8)$$

---

## 計算規則

$$\log_a (M \times N) = \log_a M + \log_a N$$
$$\log_a \frac{M}{N} = \log_a M - \log_a N$$
$$\log_a M^r = r \log_a M$$
$$\log_a 1 = 0, \quad \log_a a = 1$$

掛け算が足し算になるのがポイントです。

---

## 底の変換

$$\log_a x = \frac{\ln x}{\ln a}$$

---

## グラフの特徴

- 定義域：$x > 0$（負の数の対数は定義されない）
- $x$ 切片：$(1,\ 0)$
- 漸近線：$y$ 軸

---

## 対数方程式

真数（$\log$ の中身）が正であることを確認してから解きます。

$$\log_2(x + 1) = 3 \implies x + 1 = 8 \implies x = 7$$

---

## 自然対数 $\ln$

$$\frac{d}{dx}\ln x = \frac{1}{x}$$

---

## 関連ページ

- [指数関数](professional.md)
- [微分](professional.md)
- [対数関数（専門）](professional.md)
