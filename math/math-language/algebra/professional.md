---
title: 代数
description: "抽象代数——群・環・体・多項式環"
goal: "群・環・体の定義と基本的な性質を述べ、準同型定理を適用できるようになる"
tags: [math,math-language,algebra]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数学の言語
    path: /math/math-language/index.md
  - title: 代数
    path: /math/math-language/algebra/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 代数（標準）
    path: /math/math-language/algebra/standard.md
  - title: 負数（専門）
    path: /math/numbers/negative-numbers/professional.md
  - title: 集合（入門）
    path: /math/math-language/sets/introduction.md
---

## 代数的構造

代数（標準）までは、具体的な数（自然数、整数、有理数など）の上で文字式の操作を行いました。ここでは「足し算や掛け算のような演算が、どんな性質を持てばどんなことが言えるか」を、具体的な数から離れて考えます。

---

## 群

**定義**：集合 $G$ と二項演算 $\cdot : G \times G \to G$ の組 $(G, \cdot)$ が**群**であるとは、以下を満たすことです。

- **結合律**：$(a \cdot b) \cdot c = a \cdot (b \cdot c)$
- **単位元の存在**：$e \cdot a = a \cdot e = a$ を満たす $e \in G$ が存在する
- **逆元の存在**：各 $a \in G$ に対して $a \cdot a^{-1} = a^{-1} \cdot a = e$ を満たす $a^{-1} \in G$ が存在する

さらに $a \cdot b = b \cdot a$ が常に成り立つとき**可換群（アーベル群）**といいます。

**例**：$(\mathbb{Z}, +)$ は可換群（単位元 $0$、$a$ の逆元は $-a$）。$(\mathbb{Z}, \times)$ は群ではない（$2$ の乗法逆元 $\frac{1}{2}$ は整数でない）。

---

## 環

**定義**：集合 $R$ と二つの二項演算 $+, \times$ の組 $(R, +, \times)$ が**環**であるとは、以下を満たすことです。

- $(R, +)$ が可換群
- $\times$ について結合律が成り立つ
- 分配律：$a \times (b + c) = a \times b + a \times c$、$(a + b) \times c = a \times c + b \times c$

$\times$ が可換なとき**可換環**、乗法単位元 $1$ を持つとき**単位的環**といいます。

**例**：$\mathbb{Z}$ は可換環。負数（専門）で見た通り、$\mathbb{Z}$ は零因子を持たない整域です。

---

## 体

**定義**：可換環 $(F, +, \times)$ で、$0$ 以外のすべての元が乗法逆元を持つとき、$F$ を**体**といいます。

**例**：$\mathbb{Q}$、$\mathbb{R}$、$\mathbb{C}$ は体。$\mathbb{Z}$ は体ではない。$\mathbb{Z}/p\mathbb{Z}$（$p$ 素数）は有限体。

---

## 多項式環

体 $F$ 上の多項式環 $F[x]$ は主イデアル整域（PID）です。

$F[x]$ の既約多項式 $f(x)$ による剰余環 $F[x]/(f(x))$ は体になります。

**例**：$\mathbb{R}[x]/(x^2 + 1) \cong \mathbb{C}$。複素数（専門）で見た $\mathbb{C}$ の構成はこの特殊なケースです。

---

## 準同型と準同型定理

**定義**：群 $(G, \cdot)$ から $(H, *)$ への写像 $\varphi$ が**準同型**であるとは、$\varphi(a \cdot b) = \varphi(a) * \varphi(b)$ が成り立つことです。

**核**：$\ker(\varphi) = \{g \in G \mid \varphi(g) = e_H\}$。核は $G$ の正規部分群です。

**定理（第一同型定理）**：

$$G / \ker(\varphi) \cong \text{Im}(\varphi)$$

この定理は群・環・加群に対して同様の形で成り立ち、代数学の基本的な道具です。

**参考文献**：Hungerford, T. W. (1974). *Algebra*. Springer.

---

## 関連ページ

- [代数（標準）](standard.md)
- [負数（専門）](../../numbers/negative-numbers/professional.md) — 整数環
- [等号・等式（専門）](../equations/professional.md) — ガロア理論への入口