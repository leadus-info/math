---
title: 代数
description: "抽象代数・環論・多項式環"
tags: [math,math-language,algebra]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数学の言語
    href: /math/math-language/index.html
  - text: 代数
    href: /math/math-language/algebra/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: 代数
    url: \1/introduction.md
  - title: 四則演算（専門）
    url: ../../numbers/arithmetic/professional.md
  - title: 行列
    url: \1/introduction.md
---










# 代数（発展）
多項式環・加群・テンソル積など抽象代数の道具を扱います。

## このページで扱うこと
- 多項式環 $R[x]$ の構造
- 加群と自由加群
- テンソル積の定義と普遍性

---

## 多項式環

環 $R$ 上の多項式環 $R[x]$。$R$ が整域なら $R[x]$ も整域。

$\mathbb{Z}[x]$: 整数係数多項式、$\mathbb{Q}[x]$: 有理数係数多項式（主イデアル整域）

---

## 加群

アーベル群 $M$ に環 $R$ が左から作用する構造。  
ベクトル空間は体上の加群。

---

## テンソル積

$R$-加群 $M, N$ のテンソル積 $M \otimes_R N$: 双線形写像の普遍対象。

$$\text{Hom}(M \otimes N, P) \cong \text{Bil}(M \times N, P)$$

---

## 関連ページ

- [代数](introduction.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
- [複素数（専門）](../../numbers/complex-numbers/professional.md)
