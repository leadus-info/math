---
title: 代数
description: "抽象代数・環論・多項式環"
tags: [math,math-language,algebra]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 数学の言語
    path: /math/math-language/index.html
  - title: 代数
    path: /math/math-language/algebra/professional.html
levels:
  - level: introduction
    path: introduction.html
  - level: standard
    path: standard.html
  - level: professional
level: professional
requires:
  - title: 代数
    path: /math/math-language/algebra/introduction
  - title: 四則演算（専門）
    path: ../../numbers/arithmetic/professional.md
  - title: 行列
    path: /math/linear-algebra/matrices/introduction
---



> この記事は [標準](standard.md) の続きです。先に標準を読むことを推奨します。

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
