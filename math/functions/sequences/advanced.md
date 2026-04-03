---
title: 数列（発展）
description: "規則正しく並んだ数の列（発展）"
difficulty: 3
tags: [math,functions,sequences,advanced]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 数列（発展）
    href: /math/functions/sequences/advanced.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
  - text: 専門
    href: professional.html
---







# 数列
1、3、5、7、9……のように、規則に従って並んだ数の列が**数列**です。

## このページで扱うこと
- 等差数列・等比数列の一般項と和
- 漸化式
- 数列の極限（収束・発散）

## 前提知識
- [自然数](professional.md)
- [極限](professional.md)

---

## 等差数列

隣り合う項の差が一定（公差 $d$）な数列。

$$a_n = a_1 + (n-1)d$$

**和の公式**：

$$S_n = \frac{n(a_1 + a_n)}{2}$$

**例**：$1, 3, 5, \ldots$ の最初の 10 項の和 $= \dfrac{10 \times (1+19)}{2} = 100$

---

## 等比数列

隣り合う項の比が一定（公比 $r$）な数列。

$$a_n = a_1 \times r^{n-1}$$

**和の公式**（$r \neq 1$）：

$$S_n = \frac{a_1(1 - r^n)}{1 - r}$$

---

## 漸化式

前の項から次の項を求める規則です。

$$a_{n+1} = a_n + 3,\ a_1 = 1 \implies a_n = 3n - 2$$

---

## 数列の極限

$$\lim_{n \to \infty} r^n = 0 \quad (|r| < 1)$$

**無限等比級数**（$|r| < 1$）：

$$\sum_{n=0}^{\infty} a_1 r^n = \frac{a_1}{1-r}$$

---

## 関連ページ

- [極限](professional.md)
- [積分](professional.md)
- [数列（専門）](professional.md)
