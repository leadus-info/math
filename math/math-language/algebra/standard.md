---
title: 代数
description: "文字を使って数の関係を一般的に表す"
difficulty: 1
tags: [math,math-language,algebra]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数学の言語
    href: /math/math-language/index.html
  - text: 代数
    href: /math/math-language/algebra/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 代数
「どんな数でも……」という一般的な関係を表すとき、数の代わりに**文字**を使います。
この文字を使った数学を**代数**といいます。

## このページで扱うこと
- 文字式の意味
- 展開（括弧を外す）
- 因数分解（掛け算の形に戻す）

## 前提知識
- [乗法・べき乗](../../numbers/arithmetic/standard.md)
- [等号・等式](../equations/standard.md)

---

## 文字式とはなに？

$$2x = 6$$

$x$ は「何かわからない数」を表す文字（**変数**）です。
$x = 3$ のとき $2 \times 3 = 6$ が成り立ちます。

文字を使うと「どんな数でも成り立つルール」を一行で書けます。

$$a + b = b + a \quad \text{（どんな数でも足す順番を変えてよい）}$$

---

## 展開（括弧を外す）

括弧を外して計算することを**展開**といいます。

$$3(x + 4) = 3x + 12 \quad \text{（分配法則）}$$

### よく使う展開の公式

$$(a + b)^2 = a^2 + 2ab + b^2$$

確認：$(a+b)^2 = (a+b)(a+b) = a^2 + ab + ba + b^2 = a^2 + 2ab + b^2$

$$(a - b)^2 = a^2 - 2ab + b^2$$

$$(a + b)(a - b) = a^2 - b^2$$

---

## 因数分解（掛け算の形に戻す）

展開の逆——式を掛け算の形に変形することを**因数分解**といいます。

$$x^2 + 5x + 6 = (x + 2)(x + 3)$$

確認：右辺を展開すると $x^2 + 3x + 2x + 6 = x^2 + 5x + 6$ ○

**コツ**：「足すと $5$、掛けると $6$ になる二つの数」を探す → $2$ と $3$

---

## 剰余定理・因数定理

多項式 $f(x)$ を $(x - a)$ で割った余りは $f(a)$ です。

特に $f(a) = 0$ のとき、$(x - a)$ は $f(x)$ を割り切れます（因数定理）。

**例**：$f(x) = x^2 - 5x + 6$ で $f(2) = 4 - 10 + 6 = 0$
→ $(x - 2)$ は因数 → $f(x) = (x-2)(x-3)$

---

## 関連ページ

- [多項式](../../functions/polynomials/standard.md)
- [代数（発展）](../algebra/advanced.md) — より詳しく学ぶ
