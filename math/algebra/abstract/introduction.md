---
title: 抽象代数
description: "演算の構造を公理から分析する"
goal: "抽象代数が「演算の共通構造を捉える学問」であることを理解し、群・環・体が身近な数の体系をどう説明するかを説明できるようになる"
tags: [math,algebra,abstract]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 代数
    path: /math/algebra/index.md
  - title: 抽象代数
    path: /math/algebra/abstract/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 式（標準）
    path: /math/algebra/expressions/standard.md
  - title: 集合（標準）
    path: /math/foundations/sets/standard.md
---

## 演算の「共通する性質」を探す

整数の足し算と、時計の数字の足し算（12時の1時間後は1時）——\
これらは見た目が違いますが、「ある演算のもとで閉じている」「単位元がある」という共通の性質を持っています。

抽象代数は「どんな対象かに関わらず、演算の性質だけを取り出して研究する」学問です。

---

## 群——演算の最も基本的な構造

次の4つの性質を持つ「集合と演算の組み合わせ」を**群**といいます。

1. 演算の結果がまた同じ集合に属する（閉じている）
2. どの順番で計算しても結果が変わらない（結合法則）
3. 計算しても変わらない特別な要素がある（単位元）
4. どの要素にも「打ち消す」要素がある（逆元）

**身近な群の例**：
- 整数の足し算——単位元は $0$、$n$ の逆元は $-n$
- 時計の数字（$0$〜$11$）の足し算——単位元は $0$（12時間制）
- 正三角形の回転と反転——6通りの操作が群をなす

---

## 環と体——2つの演算を持つ構造

群に2つ目の演算（掛け算）を加えた構造が**環**、\
さらに0以外の全要素に掛け算の逆元（割り算）が使える環が**体**です。

- 整数 $\mathbb{Z}$：環（割り算はできないことがある）
- 有理数 $\mathbb{Q}$、実数 $\mathbb{R}$、複素数 $\mathbb{C}$：体（自由に四則演算できる）

---

## なぜ抽象化するのか

「整数でも有理数でも成り立つ定理」を毎回別々に証明するのは非効率です。\
「体であれば成り立つ定理」を1回証明すれば、体のすべての例（$\mathbb{Q}$, $\mathbb{R}$, $\mathbb{C}$ など）に自動的に適用できます。

---

## 関連ページ

- [式（標準）](../expressions/standard.md)
- [集合（標準）](../../foundations/sets/standard.md)
- [乗法・べき乗（専門）](../../numbers/arithmetic/professional.md)
