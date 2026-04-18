---
title: 必要・十分条件
description: "論理記号と対偶・証明技法"
goal: "命題論理の記号を使って必要条件・十分条件・同値を表し、対偶や背理法による証明の仕組みを説明できるようになる"
tags: [math,math-language,conditions]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数学の言語
    path: /math/algebra/index.md
  - title: 必要・十分条件
    path: /math/foundations/logic/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 必要・十分条件（入門）
    path: /math/foundations/logic/introduction.md
  - title: 集合（入門）
    path: /math/foundations/sets/introduction.md
---

## 命題と論理記号

真偽が定まる文を**命題**といいます。命題 $P$, $Q$ から次の複合命題が作れます。

| 記号 | 読み方 | 意味 |
|------|--------|------|
| $\neg P$ | $P$ でない | $P$ の否定 |
| $P \wedge Q$ | $P$ かつ $Q$ | 両方が真 |
| $P \vee Q$ | $P$ または $Q$ | 少なくとも一方が真 |
| $P \Rightarrow Q$ | $P$ ならば $Q$ | $P$ が真のとき $Q$ も真 |
| $P \Leftrightarrow Q$ | $P$ と $Q$ は同値 | $P \Rightarrow Q$ かつ $Q \Rightarrow P$ |

$P \Rightarrow Q$ が成り立つとき、$P$ は $Q$ の**十分条件**、$Q$ は $P$ の**必要条件**です。

---

## 逆・裏・対偶

命題 $P \Rightarrow Q$ から派生する3つの命題があります。

| 名前 | 式 | 元の命題との関係 |
|------|----|----|
| 逆 | $Q \Rightarrow P$ | 一般に同値でない |
| 裏 | $\neg P \Rightarrow \neg Q$ | 一般に同値でない |
| **対偶** | $\neg Q \Rightarrow \neg P$ | **常に同値** |

**なぜ対偶は元の命題と同値か**：$P \Rightarrow Q$ は「$P$ が真で $Q$ が偽という状況は存在しない」という意味です。これは「$Q$ が偽で $P$ が真という状況は存在しない」、すなわち $\neg Q \Rightarrow \neg P$ と同じです。

**例**：「整数 $n$ が偶数ならば $n^2$ は偶数」の対偶は「$n^2$ が奇数ならば $n$ は奇数」。対偶の証明は $n = 2k+1$ とおくと $n^2 = 4k^2+4k+1$ が奇数。$\square$

---

## 対偶による証明

直接「$P$ ならば $Q$」を示しにくいとき、対偶「$\neg Q$ ならば $\neg P$」を示すことで証明できます。

**例題**：「$n^2$ が偶数ならば $n$ は偶数」を証明してください。

対偶：「$n$ が奇数ならば $n^2$ は奇数」を示します。$n = 2k+1$ とおくと $n^2 = 4k^2 + 4k + 1 = 2(2k^2+2k)+1$ で奇数。$\square$

---

## 背理法

「$P$ を仮定して矛盾を導くことで $\neg P$ が偽、すなわち $P$ が真」と示す証明法です。

**例題**：$\sqrt{2}$ が無理数であることを証明してください。

$\sqrt{2} = \frac{p}{q}$（$p, q$ は互いに素な整数）と仮定します。$2 = \frac{p^2}{q^2}$ より $p^2 = 2q^2$。$p^2$ が偶数なので $p$ は偶数。$p = 2m$ とおくと $4m^2 = 2q^2$ より $q^2 = 2m^2$。$q$ も偶数になり、$p, q$ が互いに素であることに矛盾。$\square$

---

## 集合との対応

「$P$ ならば $Q$」は集合の言葉で表せます。$A = \{x : P(x)\}$、$B = \{x : Q(x)\}$ とすると、

$$P \Rightarrow Q \iff A \subset B$$

同値 $P \Leftrightarrow Q$ は $A = B$ に対応します。

---

## 関連ページ

- [集合（標準）](../sets/standard.md)
- [必要・十分条件（専門）](professional.md)
