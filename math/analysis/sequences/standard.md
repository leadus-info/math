---
title: 数列
description: "規則正しく並んだ数の列"
goal: "数列の定義・主要な定理・代表的な計算を理解し、後続のトピックに進める基礎を身につける"
tags: [math,functions,sequences]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/analysis/index.md
  - title: 数列
    path: /math/analysis/sequences/standard.md
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
    path: /math/analysis/limits/introduction.md
---

## 数列と一般項

自然数 $n$ に対して $a_n$ が決まる規則を**数列**といい、$\{a_n\}$ と書きます。$a_n$ の式（**一般項**）がわかれば任意の項が計算できます。

---

## 等差数列

隣り合う項の差が一定（公差 $d$）：

$$a_n = a_1 + (n-1)d$$

**和の公式**（ガウスの方法で導出）：

$$S_n = \frac{n(a_1 + a_n)}{2}$$

**例**：$1, 4, 7, 10, \ldots$（公差3）の第10項は $1 + 9 \times 3 = 28$。最初の10項の和は $\dfrac{10(1+28)}{2} = 145$。

---

## 等比数列

隣り合う項の比が一定（公比 $r$）：

$$a_n = a_1 r^{n-1}$$

**和の公式**（$r \neq 1$のとき、$S_n - rS_n$ を計算して導出）：

$$S_n = \frac{a_1(1 - r^n)}{1 - r}$$

**例**：初項2、公比3の等比数列の最初4項の和：$\dfrac{2(1-81)}{1-3} = 80$。

---

## 漸化式

前の項から次の項を決める式が**漸化式**です。

$a_1 = 1$、$a_{n+1} = a_n + 2$ → $a_n = 2n - 1$（奇数列）

$a_1 = 2$、$a_{n+1} = 3a_n$ → $a_n = 2 \cdot 3^{n-1}$

---

## 無限級数

数列 $\{a_n\}$ の和 $\displaystyle\sum_{n=1}^{\infty} a_n$ を**無限級数**といいます。

**無限等比級数**（$|r| < 1$ のとき）：

$$\sum_{n=0}^{\infty} ar^n = \frac{a}{1-r}$$

**例**：$1 + \dfrac{1}{2} + \dfrac{1}{4} + \ldots = \dfrac{1}{1-1/2} = 2$

$|r| \geq 1$ のときは発散します。

---

## 関連ページ

- [数列（入門）](introduction.md)
- [極限（標準）](../limits/standard.md)
