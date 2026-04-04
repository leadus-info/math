---
title: 代数
description: "文字を使って関係を表す"
tags: [math,math-language,algebra]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数学の言語
    path: /math/math-language/index.md
  - title: 代数
    path: /math/math-language/algebra/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 乗法・べき乗
    path: /math/numbers/arithmetic/introduction.md
  - title: 等号・等式
    path: /math/math-language/equations/introduction.md
---




## このページで扱うこと

「どんな数でも……」という一般的な関係を表すとき、文字を使います。\
文字を使った式の操作を扱う分野が**代数**です。

- 文字式の意味
- 展開と因数分解
- 剰余定理・因数定理

---

## 文字式

$2x$ は「2 に何かを掛けた結果」を一般的に表します。\
$x$ は「どんな数でも入れられる箱」です。

---

## 展開

括弧を外して計算することを**展開**といいます。

$$(a + b)^2 = a^2 + 2ab + b^2$$\
$$(a + b)(a - b) = a^2 - b^2$$\
$$(a + b)^3 = a^3 + 3a^2 b + 3ab^2 + b^3$$

---

## 因数分解

展開の逆——掛け算の形に変形することです。

$$x^2 + 5x + 6 = (x + 2)(x + 3)$$\
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
