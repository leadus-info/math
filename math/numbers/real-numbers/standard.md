---
title: 実数
description: "実数の性質・上限・下限・連続性"
goal: "実数の完備性（上限の存在）を理解し、有界な数列の収束定理など基本的な結果を説明できるようになる"
tags: [math,numbers,real-numbers]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 実数
    path: /math/numbers/real-numbers/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 実数（入門）
    path: /math/numbers/real-numbers/introduction.md
  - title: 分数（標準）
    path: /math/numbers/fractions/standard.md
  - title: 極限（入門）
    path: /math/analysis/limits/introduction.md
---

## 有理数と実数の違い

有理数は分数で表せる数の全体 $\mathbb{Q}$ でした。実数 $\mathbb{R}$ はさらに無理数を加えたものですが、その本質的な違いは**完備性**にあります。

$\mathbb{Q}$ の中には「穴」があります。$\{x \in \mathbb{Q} : x^2 < 2\}$ という有理数の集合は上に有界ですが、その上限 $\sqrt{2}$ が $\mathbb{Q}$ の中に存在しません。

---

## 上限と下限

空でない実数の集合 $A$ が**上に有界**（$A$ のすべての元より大きい実数が存在する）とき、$A$ の最小の上界を**上限**（supremum）といい $\sup A$ と書きます。

同様に下に有界なとき最大の下界を**下限**（infimum）といい $\inf A$ と書きます。

**例**：$A = \{x \in \mathbb{R} : x^2 < 2\}$ のとき $\sup A = \sqrt{2}$、$\inf A = -\sqrt{2}$。

---

## 実数の完備性

**公理（上限の存在）**：空でなく上に有界な実数の集合は必ず上限を持ちます。

この性質が $\mathbb{Q}$ との決定的な違いです。$\mathbb{Q}$ では $\sup A = \sqrt{2} \notin \mathbb{Q}$ となる場合があります。

完備性から多くの重要な定理が従います。

---

## 完備性から導かれる定理

**単調収束定理**：単調増加かつ上に有界な数列は収束します。

**ボルツァーノ＝ワイエルシュトラスの定理**：有界な数列は収束する部分列を持ちます。

**中間値の定理**：$f$ が $[a,b]$ 上で連続かつ $f(a) < 0 < f(b)$ ならば、$f(c) = 0$ となる $c \in (a,b)$ が存在します。

---

## 実数の濃度

$\mathbb{Q}$ は可算集合（$\mathbb{N}$ と全単射が存在）ですが、$\mathbb{R}$ は**非可算**です。

カントールの対角線論法：$[0,1]$ の実数を列挙 $x_1, x_2, \ldots$ と仮定し、各 $x_n$ の $n$ 桁目と異なる小数を構成すると、その数はリストに現れない——矛盾。

$$|\mathbb{Q}| = \aleph_0 < |\mathbb{R}| = 2^{\aleph_0}$$

---

## 関連ページ

- [実数（入門）](introduction.md)
- [極限（標準）](../../analysis/limits/standard.md)
- [小数（専門）](../decimals/professional.md)
