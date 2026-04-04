---
title: 集合
description: "公理的集合論・順序数・基数"
tags: [math,math-language,sets]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 数学の言語
    url: /math/math-language/index.html
  - title: 集合
    url: /math/math-language/sets/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: 集合
    url: /math/math-language/sets/introduction
  - title: 必要・十分条件（専門）
    url: ../conditions/professional.md
---


> この記事は [標準](standard.md) の続きです。先に標準を読むことを推奨します。

ZFC公理系・順序数・基数・連続体仮説を扱います。

## このページで扱うこと
- ZFC公理系（ツェルメロ・フレンケル＋選択公理）
- 順序数と超限帰納法
- 基数と連続体仮説

---

## ZFC公理系（概要）

| 公理 | 内容 |
|------|------|
| 外延性 | 同じ要素を持つ集合は等しい |
| 空集合 | $\emptyset$ の存在 |
| 対 | $\{a, b\}$ の存在 |
| 冪集合 | $\mathcal{P}(A)$ の存在 |
| 置換 | 写像による集合の像 |
| 選択公理 | 空でない集合族の選択関数の存在 |

---

## 順序数

整列集合の同型類。$0, 1, 2, \ldots, \omega, \omega+1, \ldots, \omega^2, \ldots$

**超限帰納法**: 順序数に対する帰納法。

---

## 基数と連続体仮説

$$|\mathbb{N}| = \aleph_0 < |\mathbb{R}| = 2^{\aleph_0}$$

**連続体仮説**: $2^{\aleph_0} = \aleph_1$（ZFC で独立——証明も反証もできない）

---

## 関連ページ

- [集合](introduction.md)
- [必要・十分条件（専門）](../conditions/professional.md)
- [自然数（専門）](../../numbers/natural-numbers/professional.md)
