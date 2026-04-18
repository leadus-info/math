---
title: 小数
description: "実数の構成と完備性"
goal: "デデキント切断またはコーシー列による実数の構成を説明でき、完備性公理とその帰結を証明できるようになる"
tags: [math,numbers,decimals]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 小数
    path: /math/numbers/decimals/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 分数（専門）
    path: /math/numbers/fractions/professional.md
  - title: 数列（専門）
    path: /math/functions/sequences/professional.md
  - title: 集合（入門）
    path: /math/math-language/sets/introduction.md
---

## 実数の構成の動機

小数（標準）で、有理数だけでは数直線に「穴」があることを見ました。$\sqrt{2}$ は有理数ではありませんが、数直線上には明確な位置を持つはずです。この穴を埋めて完全な数直線を得るために、実数を厳密に構成します。

構成法は2つあります。どちらも同型な順序体を与えます。

---

## デデキント切断

**定義**：有理数の部分集合の組 $(A, B)$ で、$A \cup B = \mathbb{Q}$、$A \cap B = \emptyset$、$A \neq \emptyset$、$B \neq \emptyset$、かつ任意の $a \in A$、$b \in B$ に対して $a < b$ を満たすものを**デデキント切断**といいます。

実数全体 $\mathbb{R}$ をデデキント切断全体の集合として定義します。

**例**：$\sqrt{2}$ に対応する切断は $(A, B)$ で $A = \{q \in \mathbb{Q} \mid q < 0 \text{ または } q^2 < 2\}$、$B = \mathbb{Q} \setminus A$。$A$ には最大元がなく、$B$ には最小元がありません。

切断上の演算（加法・乗法）と順序を定義し、$\mathbb{R}$ が順序体となることを確認します。

**参考文献**：Dedekind, R. (1872). *Stetigkeit und irrationale Zahlen*. Vieweg.

---

## コーシー列による構成

**定義**：有理数列 $\{a_n\}$ が**コーシー列**であるとは、任意の $\varepsilon > 0$（$\varepsilon \in \mathbb{Q}$）に対して、ある $N$ が存在し $m, n > N \implies |a_m - a_n| < \varepsilon$ が成り立つことです。

コーシー列全体の集合に同値関係 $\{a_n\} \sim \{b_n\} \iff \lim_{n \to \infty} |a_n - b_n| = 0$ を定め、同値類として実数を定義します。

**例**：$\sqrt{2}$ に対応するコーシー列の一つは $\{1, 1.4, 1.41, 1.414, \ldots\}$ です。

演算は項ごとに定義します。$[\{a_n\}] + [\{b_n\}] = [\{a_n + b_n\}]$、$[\{a_n\}] \times [\{b_n\}] = [\{a_n \times b_n\}]$。

well-defined性の証明：$\{a_n\} \sim \{a'_n\}$ かつ $\{b_n\} \sim \{b'_n\}$ のとき $|(a_n + b_n) - (a'_n + b'_n)| \leq |a_n - a'_n| + |b_n - b'_n| \to 0$。$\square$

---

## 完備性公理

実数の本質的な性質は**完備性**です。

**上限の公理**：$\mathbb{R}$ の空でない上に有界な部分集合は上限（supremum）を持つ。

$$A = \{x \in \mathbb{R} \mid x^2 < 2\} \implies \sup A = \sqrt{2} \in \mathbb{R}$$

$\mathbb{Q}$ ではこの性質が成り立ちません。$A' = \{q \in \mathbb{Q} \mid q^2 < 2\}$ は $\mathbb{Q}$ 内に上限を持ちません。

デデキント切断による構成では、完備性は構成から直接従います。コーシー列による構成では、すべてのコーシー列が収束することとして完備性が得られます。

---

## 完備性の同値な定式化

以下の命題は、順序体において上限の公理と同値です。

- **区間縮小法**：$[a_n, b_n] \supset [a_{n+1}, b_{n+1}]$ かつ $b_n - a_n \to 0$ ならば $\bigcap [a_n, b_n] = \{c\}$。
- **ボルツァーノ・ワイエルシュトラスの定理**：有界な実数列は収束する部分列を持つ。
- **コーシー列の収束**：$\mathbb{R}$ のすべてのコーシー列は $\mathbb{R}$ 内に極限を持つ。

---

## $\mathbb{R}$ の非可算性

**定理**（カントール）：$\mathbb{R}$ は非可算である。

証明（対角線論法）：$\mathbb{R}$ が可算であると仮定し、$[0,1)$ の実数を小数展開で列挙します。$r_1 = 0.d_{11}d_{12}d_{13}\ldots$、$r_2 = 0.d_{21}d_{22}d_{23}\ldots$、…。$d_{nn}$ と異なる数字 $e_n$（$0, 9$ を避ける）を選び $s = 0.e_1 e_2 e_3 \ldots$ とすると、$s$ はリストのどの $r_n$ とも異なります。矛盾。$\square$

分数（専門）で $\mathbb{Q}$ が可算であることを見ました。$\mathbb{R}$ が非可算であることから、$\mathbb{R} \setminus \mathbb{Q}$（無理数全体）は非可算です。

**参考文献**：Rudin, W. (1976). *Principles of Mathematical Analysis* (3rd ed.). McGraw-Hill.

---

## 関連ページ

- [小数（標準）](standard.md)
- [分数（専門）](../fractions/professional.md)
- [極限（専門）](../../functions/limits/professional.md)
- [数列（専門）](../../functions/sequences/professional.md)