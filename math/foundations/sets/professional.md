---
title: 集合
description: "ZFC公理系・濃度・順序数"
goal: "ZFC公理系の主要公理を述べ、可算・非可算の区別とカントールの定理を説明できるようになる"
tags: [math,math-language,sets]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数学の言語
    path: /math/algebra/index.md
  - title: 集合
    path: /math/foundations/sets/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 集合（標準）
    path: /math/foundations/sets/standard.md
  - title: 自然数（専門）
    path: /math/numbers/natural-numbers/professional.md
---

## ZFC公理系

現代数学の基礎をなす公理系がZFC（ツェルメロ＝フレンケル＋選択公理）です。主な公理を挙げます。

| 公理 | 内容 |
|------|------|
| 外延性 | 同じ要素を持つ集合は等しい |
| 空集合 | $\emptyset$ が存在する |
| 対 | $\{a, b\}$ が存在する |
| 合併 | $\bigcup \mathcal{F}$ が存在する |
| 冪集合 | $\mathcal{P}(A) = \{X : X \subset A\}$ が存在する |
| 無限 | 無限集合が存在する |
| 置換 | 写像による像が集合になる |
| **選択公理（AC）** | 空でない集合族に選択関数が存在する |

選択公理は直感的には明らかですが、バナッハ＝タルスキのパラドックスなどの奇妙な結果を導くため独立した公理として扱われます。

**参考文献**：Jech, T. (2003). *Set Theory* (3rd ed.). Springer.

---

## 濃度

集合 $A$ と $B$ の間に全単射が存在するとき、$|A| = |B|$（同じ**濃度**を持つ）といいます。

**可算集合**：$\mathbb{N}$ と全単射が存在する集合。$\mathbb{Z}$, $\mathbb{Q}$ は可算です。

$\mathbb{Z}$ が可算の証明：$0, 1, -1, 2, -2, \ldots$ と列挙できます。

$\mathbb{Q}$ が可算の証明：$\frac{p}{q}$（$q > 0$、$\gcd(p,q)=1$）を $|p|+q$ の昇順で並べ、同値なものを除けば列挙できます（カントールの対角線論法ではない方法）。

---

## カントールの定理

**定理**：任意の集合 $A$ に対して $|A| < |\mathcal{P}(A)|$（冪集合は元の集合より真に大きい濃度を持つ）。

**証明**：単射 $f: A \to \mathcal{P}(A)$ はすべて全射にはなれないことを示します。$D = \{a \in A : a \notin f(a)\}$ とおくと、$D \in \mathcal{P}(A)$ です。もし $D = f(d)$ となる $d$ があれば、$d \in D \iff d \notin f(d) = D$ で矛盾。$\square$

**系**：$|\mathbb{R}| = |\mathcal{P}(\mathbb{N})| > |\mathbb{N}|$（実数は非可算）。

---

## 連続体仮説

$\aleph_0 = |\mathbb{N}|$、$\mathfrak{c} = |\mathbb{R}| = 2^{\aleph_0}$ とします。

**連続体仮説（CH）**：$\aleph_0 < |A| < \mathfrak{c}$ となる集合 $A$ は存在しない。

CHはZFCから独立です——ゲーデル（1940）はZFCと矛盾しないことを、コーエン（1963）はZFCから証明できないことを示しました。

**参考文献**：Cohen, P. J. (1963). "The independence of the continuum hypothesis." *Proceedings of the National Academy of Sciences*, 50(6), 1143–1148.

---

## 関連ページ

- [集合（標準）](standard.md)
- [必要・十分条件（専門）](../logic/professional.md)
- [自然数（専門）](../../numbers/natural-numbers/professional.md)
