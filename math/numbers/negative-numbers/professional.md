---
title: 負数（専門）
description: "整数環の代数的構造・整域・Z上のモジュール"
difficulty: 4
tags: [math,numbers,negative-numbers,professional]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数
    href: /math/numbers/index.html
  - text: 負数（専門）
    href: /math/numbers/negative-numbers/professional.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
    href: advanced.html
  - text: 専門
---








# 負数（発展）
整数の代数的構造（整域・単項イデアル整域）について扱います。

## このページで扱うこと
- 整数環 $\mathbb{Z}$ の代数的性質
- イデアルと剰余環
- $\mathbb{Z}/n\mathbb{Z}$（合同算術）の構造

## 前提知識
- [負数](../negative-numbers/standard.md)
- [自然数（専門）](../natural-numbers/professional.md)
- [集合](../../math-language/sets/standard.md)

---

## 整数環 $\mathbb{Z}$

$\mathbb{Z}$ は加算・減算・乗算について閉じた**環（ring）**です。  
さらに零因子を持たない**整域（integral domain）**でもあります。

$$ab = 0 \implies a = 0 \text{ または } b = 0$$

---

## イデアル

$\mathbb{Z}$ のイデアルはすべて主イデアルです（$\mathbb{Z}$ は**主イデアル整域**）。

$$n\mathbb{Z} = \{\ldots, -2n, -n, 0, n, 2n, \ldots\}$$

$\gcd(a, b)$ はイデアル $a\mathbb{Z} + b\mathbb{Z}$ の生成元に対応します。

---

## 剰余環 $\mathbb{Z}/n\mathbb{Z}$

$$\mathbb{Z}/n\mathbb{Z} = \{[0], [1], \ldots, [n-1]\}$$

- $n$ が素数のとき: **体**（逆元が存在）
- $n$ が合成数のとき: 零因子が存在する

**例**: $\mathbb{Z}/5\mathbb{Z}$ は体、$\mathbb{Z}/6\mathbb{Z}$ は体でない（$[2][3]=[0]$）

---

## 関連ページ

- [負数](../negative-numbers/standard.md)
- [集合（専門）](../../math-language/sets/professional.md)
- [複素数（専門）](../complex-numbers/professional.md)
