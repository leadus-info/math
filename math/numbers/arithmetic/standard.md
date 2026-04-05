---
title: 乗法・べき乗
description: "掛け算の性質とべき乗・平方根"
tags: [math,operations,arithmetic]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 乗法・べき乗
    path: /math/numbers/arithmetic/standard.md
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
  - title: 負数
    path: /math/numbers/negative-numbers/introduction.md
  - title: 分数
    path: /math/numbers/fractions/introduction.md
---

## 乗法の性質まとめ

掛け算には次の三つの重要な性質があります。

**交換法則**：順番を入れ替えてよい

$$a \times b = b \times a$$

**結合法則**：まとめ方を変えてよい

$$(a \times b) \times c = a \times (b \times c)$$

**分配法則**：足し算と掛け算をつなぐ

$$a \times (b + c) = a \times b + a \times c$$

---

## べき乗

同じ数を何度も掛けることを**べき乗**（累乗）といいます。

$$2^3 = 2 \times 2 \times 2 = 8$$\
$$a^n = \underbrace{a \times a \times \cdots \times a}_{n \text{ 個}}$$

特別な場合：

$$a^1 = a, \quad a^0 = 1 \quad (a \neq 0)$$

---

## 指数法則

| 法則 | 式 | 例 |
|------|----|----|
| 掛け算 | $a^m \times a^n = a^{m+n}$ | $2^3 \times 2^4 = 2^7$ |
| 割り算 | $a^m \div a^n = a^{m-n}$ | $2^5 \div 2^3 = 2^2$ |
| 累乗の累乗 | $(a^m)^n = a^{mn}$ | $(2^3)^2 = 2^6$ |
| 積のべき乗 | $(ab)^n = a^n b^n$ | $(2 \times 3)^2 = 4 \times 9$ |

---

## 負の指数

$a^{-n}$ は $a^n$ の逆数として定義します。

$$a^{-n} = \frac{1}{a^n}, \quad a^{-1} = \frac{1}{a}$$

これにより指数法則がすべての整数に対して成り立ちます。

---

## 平方根・累乗根

$x^2 = a$ になる $x$（$x \geq 0$）を $\sqrt{a}$（ルート $a$）と書きます。

$$\sqrt{9} = 3 \quad (3^2 = 9), \quad \sqrt{4} = 2 \quad (2^2 = 4)$$\
$$\sqrt{2} = 1.414\ldots \quad \text{（割り切れない）}$$

より一般に、$x^n = a$ になる $x$（$x \geq 0$）を $\sqrt[n]{a} = a^{1/n}$ と書きます。

$$\sqrt[3]{8} = 2 \quad (2^3 = 8)$$

---

## 関連ページ

- [等号・等式](professional.md) — 計算結果を式で表す
- [指数関数](professional.md) — べき乗を関数として見る
- [乗法・べき乗（専門）](professional.md) — 群・環・体の代数的構造
