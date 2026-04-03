---
title: 複素数（発展）
description: "実数を超えた数の体系（発展）"
difficulty: 3
tags: [math,complex-numbers,complex-numbers,advanced]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数
    href: /math/numbers/index.html
  - text: 複素数（発展）
    href: /math/numbers/complex-numbers/advanced.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
  - text: 専門
    href: professional.html
---







# 複素数
$x^2 = -1$ を満たす数は実数の中に存在しません。
「存在することにしよう」と決めたのが虚数単位 $i$ であり、これを使って表す数が**複素数**です。

## このページで扱うこと
- 虚数単位 $i$ と複素数の定義
- 複素数の四則演算
- 複素平面と極形式・オイラーの公式

## 前提知識
- [負数](professional.md)
- [三角関数](professional.md)
- [指数関数](professional.md)

---

## 虚数単位 $i$

$$i^2 = -1$$

---

## 複素数の定義

$$z = a + bi \quad (a, b \in \mathbb{R})$$

- $a$：実部、$b$：虚部

---

## 四則演算

**足し算**：

$$(3 + 2i) + (1 + 4i) = 4 + 6i$$

**掛け算**（$i^2 = -1$ を使う）：

$$(1 + 2i)(3 + i) = 3 + i + 6i + 2i^2 = 1 + 7i$$

**複素共役**：$\overline{a + bi} = a - bi$

---

## 複素平面

複素数 $a + bi$ を平面上の点 $(a, b)$ として表します。

**絶対値**：原点からの距離

$$|z| = \sqrt{a^2 + b^2}$$

---

## 極形式とオイラーの公式

$$z = r(\cos\theta + i\sin\theta) = re^{i\theta}$$

$$e^{i\theta} = \cos\theta + i\sin\theta$$

$$e^{i\pi} + 1 = 0$$

---

## 関連ページ

- [複素関数](professional.md)
- [三角関数](professional.md)
- [複素数（専門）](professional.md)
