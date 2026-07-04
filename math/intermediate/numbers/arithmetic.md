---
title: 乗法・べき乗
description: "掛け算の繰り返し"
goal: "べき乗の意味と指数法則を理解し、計算できるようになる"
tags: [math, numbers, arithmetic]
stage: 中級編
subject: 数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 中級編
    path: /math/intermediate/index.md
  - title: 乗法・べき乗
    path: /math/intermediate/numbers/arithmetic.md
requires:
  - title: 掛け算
    path: /math/beginner/numbers/multiplication.md
---

## 同じ数を何度も掛ける

クッキーが1皿に3個。同じ皿が3枚なら $3 \times 3 = 9$ 個。さらに同じ棚が3段なら $3 \times 3 \times 3 = 27$ 個です。

「同じ数を繰り返し掛ける」操作を**べき乗**（累乗）といいます。

$$3 \times 3 \times 3 = 3^3 = 27$$

右上の小さな数（**指数**）が「何回掛けるか」を表します。$3^3$ は「3の3乗」と読みます。

$$2^1 = 2, \quad 2^2 = 4, \quad 2^3 = 8, \quad 2^4 = 16, \quad 2^{10} = 1024$$

---

## 指数法則

同じ底のべき乗を掛けるときは、指数を足すだけで計算できます。

$$a^m \times a^n = a^{m+n}$$

**例**：$2^3 \times 2^4 = 2^7$

割り算では指数を引きます。

$$a^m \div a^n = a^{m-n} \quad (m \geq n)$$

べき乗のべき乗では、指数を掛けます。

$$(a^m)^n = a^{mn}$$

**例**：$(3^2)^4 = 3^8 = 6561$

---

## まとめ

べき乗は「同じ数を繰り返し掛ける操作」です。同じ底のべき乗の掛け算・割り算は指数の足し算・引き算に対応し、べき乗のべき乗は指数の掛け算に対応します。

---

## 関連ページ

- [負数（中級編）](integers.md)
- [平方根（中級編）](arithmetic-square-root.md)
- [指数関数（応用編）](/math/advanced/specific-functions/exponential.md) — べき乗を関数として見る
