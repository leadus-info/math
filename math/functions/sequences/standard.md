---
title: 数列
description: "規則正しく並んだ数の列"
tags: [math,functions,sequences]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/functions/index.md
  - title: 数列
    path: /math/functions/sequences/standard.md
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
  - title: 極限
    path: /math/functions/limits/introduction.md
---

## 数列の定義

自然数 $n$ に対して数 $a_n$ が定まる規則が**数列**です。$\{a_n\}$ と書きます。

$a_1, a_2, a_3, \ldots$ と各項が並びます。

---

## 等差数列

隣り合う項の差が一定（公差 $d$）な数列。

**一般項**：

$$a_n = a_1 + (n-1)d$$

**和の公式**（初項から第 $n$ 項まで）：

$$S_n = \frac{n(a_1 + a_n)}{2} = na_1 + \frac{n(n-1)}{2}d$$

**導出**：$S_n = a_1 + a_2 + \cdots + a_n$ と逆順の和を足し合わせると各項の和が $a_1 + a_n$ になり、$n$ 組あるので $2S_n = n(a_1+a_n)$。

**例**：$1, 4, 7, 10, \ldots$（公差 3）の最初の 10 項の和\
$a_{10} = 1 + 9 \times 3 = 28$、$S_{10} = \frac{10(1+28)}{2} = 145$

---

## 等比数列

隣り合う項の比が一定（公比 $r$）な数列。

**一般項**：

$$a_n = a_1 \cdot r^{n-1}$$

**和の公式**（$r \neq 1$）：

$$S_n = \frac{a_1(1 - r^n)}{1 - r}$$

**導出**：$S_n - rS_n = a_1 - a_1 r^n$ から $(1-r)S_n = a_1(1-r^n)$。

**例**：初項 2、公比 3 の等比数列の最初の 4 項の和\
$S_4 = \frac{2(1-81)}{1-3} = \frac{2 \times (-80)}{-2} = 80$

---

## 漸化式

前の項から次の項を求める規則（漸化式）で定まる数列もあります。

**例（等差型）**：$a_1 = 1$、$a_{n+1} = a_n + 3$ → $a_n = 3n - 2$

**例（等比型）**：$a_1 = 2$、$a_{n+1} = 2a_n$ → $a_n = 2^n$

---

## 数列の極限

**収束**：$n \to \infty$ のとき $a_n$ が一定値 $L$ に近づくとき、$\lim_{n\to\infty} a_n = L$ と書きます。

$$\lim_{n\to\infty} r^n = 0 \quad (|r| < 1)$$

**無限等比級数**（$|r| < 1$ のとき収束）：

$$\sum_{n=0}^{\infty} ar^n = \frac{a}{1-r}$$

**例**：$1 + \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \cdots = \frac{1}{1 - 1/2} = 2$

---

## 関連ページ

- [極限](../limits/introduction.md)
- [積分](../integrals/introduction.md)
