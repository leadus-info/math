---
title: 数列
description: "規則正しく並んだ数の列"
difficulty: 2
tags: [math,functions,sequences]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 数列
    href: /math/functions/sequences/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 数列
$1, 3, 5, 7, 9, \ldots$ のように、規則に従って並んだ数の列が**数列**です。

## このページで扱うこと
- 等差数列（一定の差で増える）
- 等比数列（一定の比で増える）
- 無限に続く数列の和

## 前提知識
- [自然数](../../numbers/natural-numbers/standard.md)
- [極限](../calculus/limits/standard.md)

---

## 等差数列

隣り合う項の差が一定（**公差** $d$）な数列です。

$$1, 4, 7, 10, 13, \ldots \quad (d = 3)$$

**一般項**（第 $n$ 項の式）：

$$a_n = a_1 + (n-1)d$$

**最初の $n$ 項の和**：

$$S_n = \frac{n(a_1 + a_n)}{2} = \frac{n(2a_1 + (n-1)d)}{2}$$

**例**：$1 + 4 + 7 + 10 + 13 = \dfrac{5 \times (1+13)}{2} = 35$

---

## 等比数列

隣り合う項の比が一定（**公比** $r$）な数列です。

$$1, 2, 4, 8, 16, \ldots \quad (r = 2)$$

**一般項**：

$$a_n = a_1 \times r^{n-1}$$

**最初の $n$ 項の和**（$r \neq 1$）：

$$S_n = \frac{a_1(1 - r^n)}{1 - r}$$

---

## 無限等比級数

$|r| < 1$ のとき、等比数列を無限に足し続けると収束します。

$$\sum_{n=0}^{\infty} a_1 r^n = \frac{a_1}{1-r}$$

**例**：$1 + \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \cdots = \frac{1}{1 - \frac{1}{2}} = 2$

---

## 関連ページ

- [極限](../calculus/limits/standard.md)
- [積分](../calculus/integrals/standard.md)
- [数列（発展）](../sequences/advanced.md) — より詳しく学ぶ
