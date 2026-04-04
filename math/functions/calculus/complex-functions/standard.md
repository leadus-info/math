---
title: 複素関数
description: "複素数を変数にとる関数"
tags: [math,complex-numbers,complex-functions]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数の操作
    href: /math/functions/calculus/index.html
  - text: 複素関数
    href: /math/functions/calculus/complex-functions/standard.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
  - level: professional
    url: professional.html
level: standard
requires:
  - title: 複素数
    url: professional.md
  - title: 微分
    url: professional.md
  - title: 積分
    url: professional.md
---









# 複素関数
複素数を変数にとる関数が**複素関数**です。
「複素数で微分できる」という条件が、実数のときより強い制約を生みます。

## このページで扱うこと
- 複素関数の定義と基本例
- 正則性とコーシー・リーマン方程式
- コーシーの積分定理と留数定理

---

## 複素関数とは

$$f: \mathbb{C} \to \mathbb{C}, \quad f(z) = z^2,\quad f(z) = e^z$$

$z = x + iy$ とすると $f(z) = u(x,y) + iv(x,y)$ の形になります。

---

## 基本的な複素関数

$$e^z = e^x(\cos y + i\sin y)$$

$$\sin z = \frac{e^{iz} - e^{-iz}}{2i}$$

---

## 正則性

$f(z)$ が $z_0$ で**正則**とは、複素数の方向からどう近づいても微分が同じ値になることです。

$$f'(z_0) = \lim_{h \to 0} \frac{f(z_0 + h) - f(z_0)}{h} \quad (h \in \mathbb{C})$$

---

## コーシー・リーマン方程式

$f = u + iv$ が正則であるための条件：

$$\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}, \qquad \frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x}$$

---

## コーシーの積分定理

$f$ が正則なら閉曲線 $C$ に沿った積分は 0：

$$\oint_C f(z)\,dz = 0$$

---

## 留数定理

$$\oint_C f(z)\,dz = 2\pi i \sum_k \text{Res}(f, z_k)$$

これを使って実数の難しい積分も計算できます。

---

## 関連ページ

- [複素数](professional.md)
- [複素関数（専門）](professional.md) — リーマン面・モジュラー形式
