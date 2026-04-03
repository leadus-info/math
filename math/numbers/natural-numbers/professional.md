---
title: 自然数（専門）
description: "自然数の厳密な構成・ペアノ公理・数論的性質"
difficulty: 4
tags: [math,numbers,natural-numbers,professional]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数
    href: /math/numbers/index.html
  - text: 自然数（専門）
    href: /math/numbers/natural-numbers/professional.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
    href: advanced.html
  - text: 専門
---








# 自然数（発展）
このページでは、自然数を公理から厳密に構築し、数論・整除論の基礎を扱います。  
初等的な自然数の概念は[自然数（入門）](../natural-numbers/standard.md)を参照してください。

## このページで扱うこと
- ペアノ公理による自然数の公理的定義
- 整除・最大公約数・ユークリッドの互除法
- 算術の基本定理（素因数分解の一意性）の証明

## 前提知識
- [自然数](../natural-numbers/standard.md)
- [必要・十分条件](../../math-language/conditions/standard.md)
- [集合](../../math-language/sets/standard.md)

---

## ペアノ公理

自然数を以下の5つの公理で定義します。

1. $1 \in \mathbb{N}$
2. 各 $n \in \mathbb{N}$ に対して、その**後者** $S(n) \in \mathbb{N}$ が存在する
3. $S(n) = 1$ となる $n$ は存在しない（1 は後者でない）
4. $S(m) = S(n) \Rightarrow m = n$（後者写像は単射）
5. **帰納公理**: $1 \in M$ かつ $n \in M \Rightarrow S(n) \in M$ ならば $M = \mathbb{N}$

これにより加算・乗算も帰納的に定義できます。

---

## 整除と最大公約数

$a = bq$（$q \in \mathbb{N}_0$）を満たすとき「$b$ は $a$ を割り切る」といい $b \mid a$ と書きます。

**最大公約数** $\gcd(a,b)$: $a$ と $b$ の公約数のうち最大のもの。

### ユークリッドの互除法

$$\gcd(a, b) = \gcd(b, r) \quad (a = bq + r)$$

**例**: $\gcd(48, 18)$

$$48 = 18 \times 2 + 12,\quad 18 = 12 \times 1 + 6,\quad 12 = 6 \times 2 + 0$$

$\therefore \gcd(48, 18) = 6$

### ベズーの等式

任意の $a, b \in \mathbb{N}$ に対して $ax + by = \gcd(a,b)$ を満たす整数 $x, y$ が存在します。

---

## 算術の基本定理

**定理**: 1 より大きい任意の自然数は素数の積として一意に表せる（順序を除く）。

**存在**（帰納法）: $n$ が素数なら自明。合成数なら $n = ab$（$a,b < n$）と書け、帰納仮定より各因数が素因数分解を持つ。

**一意性**: 背理法。異なる素因数分解が存在すると仮定すると、ユークリッドの補題（$p \mid ab \Rightarrow p \mid a$ または $p \mid b$）に矛盾する。

---

## 整除論の応用

| 概念 | 定義 | 応用 |
|------|------|------|
| 最小公倍数 | $\text{lcm}(a,b) = \frac{ab}{\gcd(a,b)}$ | 通分 |
| 合同式 | $a \equiv b \pmod{m} \iff m \mid (a-b)$ | 暗号理論 |
| フェルマーの小定理 | $p$ が素数, $p \nmid a$ ならば $a^{p-1} \equiv 1 \pmod{p}$ | RSA暗号 |

---

## 関連ページ

- [自然数](../natural-numbers/standard.md) — 入門編
- [集合](../../math-language/sets/standard.md) — $\mathbb{N}$ の集合論的構成
- [必要・十分条件（専門）](../../math-language/conditions/professional.md) — 証明技法
- [場合の数（専門）](../../statistics/counting/professional.md) — 整数の数え上げ
