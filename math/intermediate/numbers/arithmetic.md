---
title: 乗法・べき乗
description: "掛け算の繰り返しと、その逆操作である平方根"
goal: "べき乗の指数法則を理解し、平方根の性質を使って根号を含む式を計算できるようになる"
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

## 平方根——べき乗の逆

「2乗すると9になる数は何か？」——答えは3です。$3^2 = 9$ だからです。

この「2乗すると $a$ になる数（$a \geq 0$）」を**平方根**といい、$\sqrt{a}$ と書きます。

$$\sqrt{9} = 3, \quad \sqrt{4} = 2, \quad \sqrt{25} = 5$$

$\sqrt{2}$ はどうでしょう。$1^2 = 1$、$2^2 = 4$ なので1と2の間のどこかにあります。電卓で計算すると $\sqrt{2} \approx 1.41421\ldots$ で、割り切れない小数が延々と続きます。これは整数でも分数でもない数（無理数）です。

---

## 根号を含む式の計算

平方根には次の性質があります。

$$\sqrt{ab} = \sqrt{a} \times \sqrt{b}, \qquad \sqrt{\frac{a}{b}} = \frac{\sqrt{a}}{\sqrt{b}}$$

これを使うと、根号の中を簡単にできます。

**例**：$\sqrt{12} = \sqrt{4 \times 3} = \sqrt{4} \times \sqrt{3} = 2\sqrt{3}$

分母に根号が残っていると計算しづらいので、分母と分子に同じ数を掛けて根号を分子に移します（**有理化**）。

$$\frac{1}{\sqrt{2}} = \frac{1 \times \sqrt{2}}{\sqrt{2} \times \sqrt{2}} = \frac{\sqrt{2}}{2}$$

**例題**：$\frac{\sqrt{18}}{\sqrt{2}}$ を計算する。

$$\frac{\sqrt{18}}{\sqrt{2}} = \sqrt{\frac{18}{2}} = \sqrt{9} = 3$$

---

## まとめ

べき乗は「同じ数を繰り返し掛ける操作」で、同じ底のべき乗の掛け算・割り算は指数の足し算・引き算に対応します。平方根は2乗の逆操作で、根号の中を簡単にしたり分母を有理化したりして計算します。

---

## 関連ページ

- [負数（中級編）](integers.md)
- [指数関数（応用編）](/math/advanced/specific-functions/exponential.md) — べき乗を関数として見る
