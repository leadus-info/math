---
title: 代数
description: "文字を使って関係を表す"
tags: [math,math-language,algebra]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 数学の言語
    path: /math/math-language/index.html
  - title: 代数
    path: /math/math-language/algebra/standard.html
levels:
  - level: introduction
    path: introduction.html
  - level: standard
  - level: professional
    path: professional.html
level: standard
requires:
  - title: 乗法・べき乗
    path: /math/numbers/arithmetic/introduction
  - title: 等号・等式
    path: /math/math-language/equations/introduction
---



> この記事は [入門](introduction.md) の続きです。先に入門を読むことを推奨します。

「どんな数でも……」という一般的な関係を表すとき、文字を使います。
文字を使った式の操作を扱う分野が**代数**です。

## このページで扱うこと
- 文字式の意味
- 展開と因数分解
- 剰余定理・因数定理

---

## 文字式

$2x$ は「2 に何かを掛けた結果」を一般的に表します。
$x$ は「どんな数でも入れられる箱」です。

---

## 展開

括弧を外して計算することを**展開**といいます。

$$(a + b)^2 = a^2 + 2ab + b^2$$
$$(a + b)(a - b) = a^2 - b^2$$
$$(a + b)^3 = a^3 + 3a^2 b + 3ab^2 + b^3$$

---

## 因数分解

展開の逆——掛け算の形に変形することです。

$$x^2 + 5x + 6 = (x + 2)(x + 3)$$
$$x^2 - 9 = (x + 3)(x - 3)$$

---

## 剰余定理・因数定理

多項式 $f(x)$ を $(x - a)$ で割ったときの余りは $f(a)$ です。

特に $f(a) = 0$ なら $(x - a)$ は $f(x)$ の因数です。

**例**：$f(x) = x^2 - 5x + 6$

$f(2) = 0$ なので $(x-2)$ は因数 → $f(x) = (x-2)(x-3)$

---

## 関連ページ

- [多項式](professional.md)
- [行列](professional.md)
- [代数（専門）](professional.md)
