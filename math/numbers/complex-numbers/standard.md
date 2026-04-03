---
title: 複素数
description: "$x^2=-1$ の解として生まれた数"
difficulty: 2
tags: [math,complex-numbers,complex-numbers]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数
    href: /math/numbers/index.html
  - text: 複素数
    href: /math/numbers/complex-numbers/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 複素数
$x^2 = -1$ を満たす数は実数の中にありません。
「存在することにしてしまおう」と決めた数が**虚数単位** $i$ で、これを使って表す数が**複素数**です。

## このページで扱うこと
- 虚数単位 $i$ と複素数の定義
- 複素数の計算
- 複素平面（ガウス平面）

## 前提知識
- [負数](../negative-numbers/standard.md) — 実数の限界
- [三角関数](../../functions/trigonometric/standard.md) — 極形式に必要

---

## 虚数単位 $i$

$$i^2 = -1$$

「$-1$ の平方根」として $i$ を定義します。
$i$ 自体は実数ではありません。

---

## 複素数の定義

$$z = a + bi \quad (a, b \in \mathbb{R})$$

- $a$：**実部**（実数の部分）
- $b$：**虚部**（$i$ の係数）
- $b = 0$ なら実数、$a = 0$ かつ $b \neq 0$ なら純虚数

---

## 複素数の計算

**足し算**：実部・虚部ごとに計算

$$(3 + 2i) + (1 + 4i) = 4 + 6i$$

**掛け算**：$i^2 = -1$ を使って展開

$$(2 + i)(3 + 2i) = 6 + 4i + 3i + 2i^2 = 6 + 7i - 2 = 4 + 7i$$

**複素共役**：虚部の符号を反転

$$\overline{3 + 2i} = 3 - 2i$$

---

## 複素平面

複素数 $a + bi$ を平面上の点 $(a, b)$ として表します。
- 横軸：実部（**実軸**）
- 縦軸：虚部（**虚軸**）

**絶対値**（原点からの距離）：

$$|z| = \sqrt{a^2 + b^2}$$

---

## 極形式とオイラーの公式

$$z = r(\cos\theta + i\sin\theta) = re^{i\theta}$$

- $r = |z|$：絶対値
- $\theta$：偏角（実軸からの角度）

最も美しい等式：

$$e^{i\pi} + 1 = 0$$

$e$、$i$、$\pi$、$1$、$0$ という $5$ つの数がひとつの式に収まります。

---

## 関連ページ

- [複素関数](../../functions/calculus/complex-functions/standard.md)
- [三角関数](../../functions/trigonometric/standard.md)
- [複素数（発展）](../complex-numbers/advanced.md) — より詳しく学ぶ
