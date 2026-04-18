---
title: 乗法・べき乗
description: "掛け算を繰り返す操作"
goal: "べき乗が「掛け算の繰り返し」であることを理解し、指数法則と平方根の意味を説明できるようになる"
tags: [math,numbers,arithmetic]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 乗法・べき乗
    path: /math/numbers/arithmetic/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 自然数（入門）
    path: /math/numbers/natural-numbers/introduction.md
---

## 同じ数を何度も掛ける

クッキーが1皿に3個。同じ皿が3枚なら $3 \times 3 = 9$ 個。さらに同じ棚が3段なら $3 \times 3 \times 3 = 27$ 個です。

「同じ数を繰り返し掛ける」操作を**べき乗**（累乗）といいます。

$$3 \times 3 \times 3 = 3^3 = 27$$

右上の小さな数（**指数**）が「何回掛けるか」を表します。$3^3$ は「3の3乗」と読みます。

---

## べき乗の例

$$2^1 = 2$$
$$2^2 = 2 \times 2 = 4$$
$$2^3 = 2 \times 2 \times 2 = 8$$
$$2^4 = 2 \times 2 \times 2 \times 2 = 16$$
$$2^{10} = 1024$$

指数が1増えるたびに、値が2倍になっていきます。この急激な増え方が「指数的増加」と呼ばれる現象の正体です。

---

## べき乗の計算を楽にする

$2^3 \times 2^4$ を計算してみましょう。

$$2^3 \times 2^4 = (2 \times 2 \times 2) \times (2 \times 2 \times 2 \times 2) = 2^7$$

掛け算の回数を足すだけです。同じ底のべき乗を掛けるときは、指数を足します。

$$a^m \times a^n = a^{m+n}$$

---

## 平方根——べき乗の逆

「2乗すると9になる数は何か？」——答えは3です。$3^2 = 9$ だからです。

この「2乗すると $a$ になる数（$a \geq 0$）」を**平方根**といい、$\sqrt{a}$ と書きます。

$$\sqrt{9} = 3, \quad \sqrt{4} = 2, \quad \sqrt{25} = 5$$

$\sqrt{2}$ はどうでしょう。$1^2 = 1$、$2^2 = 4$ なので1と2の間のどこかにあります。電卓で計算すると $\sqrt{2} \approx 1.41421\ldots$ で、割り切れない小数が延々と続きます。これは整数でも分数でもない数（無理数）です。

---

## まとめ

べき乗は「同じ数を繰り返し掛ける操作」で、指数が指数の個数を表します。同じ底のべき乗の掛け算は指数を足すだけで計算できます。平方根は2乗の逆操作です。

---

## 関連ページ

- [自然数（標準）](../natural-numbers/standard.md) — べき乗の法則の詳細
- [指数関数（入門）](../../specific-functions/exponential/introduction.md) — べき乗を関数として見る
