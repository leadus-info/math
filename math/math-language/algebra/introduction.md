---
title: 代数
description: "文字式の計算と変形"
goal: "文字式の整理・展開・因数分解の基本を理解し、式を目的に応じた形に変形できるようになる"
tags: [math,math-language,algebra]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数学の言語
    path: /math/math-language/index.md
  - title: 代数
    path: /math/math-language/algebra/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 自然数（標準）
    path: /math/numbers/natural-numbers/standard.md
  - title: 等号・等式（入門）
    path: /math/math-language/equations/introduction.md
---

## 文字式を計算する

自然数（標準）で、文字を使って「どんな数でも成り立つこと」を表す方法を見ました。$a + b = b + a$ のように、$a$ や $b$ はどんな数でも入る箱でした。

ここでは、文字を含む式そのものを計算したり、形を変えたりする方法を学びます。

---

## 同類項をまとめる

$3x + 2x$ は、$x$ が3つと $x$ が2つで、合わせて $x$ が5つです。

$$3x + 2x = 5x$$

$x$ と $y$ のように違う文字同士はまとめられません。

$$3x + 2y + x = 4x + 2y$$

このように、同じ文字を含む項（**同類項**）をまとめることが、文字式の計算の基本です。

---

## 掛け算の書き方

文字式では、数と文字の掛け算から $\times$ を省略して書きます。

$$2 \times x = 2x, \quad a \times b = ab$$

また、同じ文字の掛け算はべき乗で書きます。

$$x \times x = x^2, \quad a \times a \times a = a^3$$

---

## 展開——括弧を外す

自然数（標準）で見た分配法則 $a \times (b + c) = a \times b + a \times c$ を使うと、括弧を外すことができます。

$$3(x + 2) = 3x + 6$$

括弧同士の掛け算も、分配法則を繰り返し使います。

$$(x + 2)(x + 3) = x \times x + x \times 3 + 2 \times x + 2 \times 3 = x^2 + 3x + 2x + 6 = x^2 + 5x + 6$$

このように括弧を外して計算することを**展開**といいます。

---

## 因数分解——掛け算の形に戻す

展開の逆を**因数分解**といいます。

$$x^2 + 5x + 6 = (x + 2)(x + 3)$$

展開すると左辺に戻ることを確認してみてください。展開と因数分解は、同じ式の「別の見た目」です。場面に応じて使いやすい形に変えます。

---

## まとめ

文字式の計算では、同類項をまとめる、分配法則で括弧を外す（展開）、掛け算の形に戻す（因数分解）が基本操作です。これらは方程式を解くときや、関数の性質を調べるときに繰り返し使います。

---

## 関連ページ

- [自然数（標準）](../../numbers/natural-numbers/standard.md) — 文字を使った法則の表し方
- [等号・等式（入門）](../equations/introduction.md) — 方程式と恒等式
- [多項式（入門）](../../functions/polynomials/introduction.md)