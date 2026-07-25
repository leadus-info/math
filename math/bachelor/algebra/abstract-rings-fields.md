---
title: 環と体
description: "群に掛け算を加えた環、零因子を持たない整域、0以外の全要素に逆元を持つ体の定義と、体・整域・可換環・環という包含関係を解説する"
goal: "環・整域・体の定義とその包含関係を理解できるようになる"
tags: [math, algebra, abstract]
stage: bachelor
subject: 代数
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 環と体
    path: abstract-rings-fields.md
requires:
  - title: 群
    path: abstract-groups.md
---

## 環と体の定義

群に2つ目の演算（掛け算）を加えた構造が**環**、さらに $0$ 以外の全要素に乗法逆元がある可換環が**体**です。

**環** $(R, +, \cdot)$：$(R, +)$ が可換群、$\cdot$ について結合律・分配律が成立し、乗法の単位元 $1$（$1 \cdot a = a \cdot 1 = a$）を持つ（この単位元の存在を仮定しない流儀もありますが、ここでは単位的環として扱います）。

**整域**：零因子を持たない可換単位環（$ab=0 \Rightarrow a=0$ または $b=0$）。

$$\text{体} \subset \text{整域} \subset \text{可換環} \subset \text{環}$$

**体はなぜ整域か**：体$F$で$ab=0$、$a\neq0$とします。$a\neq0$なら体の定義より逆元$a^{-1}$が存在するので、両辺に左から$a^{-1}$を掛けると $a^{-1}(ab)=a^{-1}\cdot0$、すなわち $b=0$。よって $ab=0$ ならば $a=0$ または $b=0$ が成り立ち、体は零因子を持たない、つまり整域です。$\blacksquare$

整数 $\mathbb{Z}$ は環（割り算はできないことがある）、有理数 $\mathbb{Q}$・実数 $\mathbb{R}$・複素数 $\mathbb{C}$ は体（自由に四則演算できる）です。

---

## まとめ

環は群に掛け算を加えた構造で、体は環の中でも0以外のすべての要素に乗法逆元がある特別な場合です。体・整域・可換環・環はこの順に包含関係にあります。

---

## 関連ページ

- [準同型・同型（発展編）](abstract-homomorphisms.md)
