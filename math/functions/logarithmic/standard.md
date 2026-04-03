---
title: 対数関数
description: "「何乗すれば？」という問いへの答え"
difficulty: 2
tags: [math,functions,logarithmic]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 対数関数
    href: /math/functions/logarithmic/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---




# 対数関数
「$2$ を何乗すれば $8$ になる？」——答えは $3$ です（$2^3 = 8$）。
この「何乗？」を求める操作が**対数**です。

## このページで扱うこと
- 対数の定義（指数と逆の操作）
- 計算ルール
- グラフの特徴

## 前提知識
- [指数関数](../exponential/standard.md) — 対数は指数の逆操作

---

## 対数とは？

$$\log_2 8 = 3 \quad \text{（$2$ を $3$ 乗すると $8$）}$$

$$y = \log_a x \iff a^y = x$$

「$a$ を何乗すれば $x$ になるか」が $\log_a x$ の答えです。

$$\log_{10} 1000 = 3, \quad \log_2 1 = 0, \quad \log_2 2 = 1$$

---

## 計算ルール

**掛け算 → 足し算に変換**：

$$\log_a (M \times N) = \log_a M + \log_a N$$

**割り算 → 引き算に変換**：

$$\log_a \frac{M}{N} = \log_a M - \log_a N$$

**べき乗 → 掛け算に変換**：

$$\log_a M^r = r \log_a M$$

このルールのおかげで、昔の人は対数を使って大きな数の掛け算を足し算に変換して計算しました。

---

## 底の変換

$$\log_a x = \frac{\ln x}{\ln a}$$

電卓では通常 $\ln$（自然対数）か $\log_{10}$（常用対数）だけが計算できます。
この式でどんな底の対数も計算できます。

---

## グラフの特徴

- 定義域：$x > 0$（$0$ 以下の対数は定義されない）
- $x = 1$ で必ず $y = 0$（$a^0 = 1$ なので $\log_a 1 = 0$）
- $y$ 軸（$x = 0$）に限りなく近づくが、到達しない

---

## 対数方程式

真数（$\log$ の中身）が $0$ より大きいか確認してから解きます。

$$\log_2(x + 1) = 3 \implies x + 1 = 2^3 = 8 \implies x = 7$$

---

## 関連ページ

- [指数関数](../exponential/standard.md)
- [対数関数（発展）](../logarithmic/advanced.md) — より詳しく学ぶ
