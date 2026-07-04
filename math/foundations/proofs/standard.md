---
title: 証明法
description: "証明技法の体系的な整理"
goal: "直接証明・対偶・背理法・数学的帰納法を状況に応じて使い分け、簡単な命題の証明を書けるようになる"
tags: [math,foundations,proofs]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 基礎
    path: /math/foundations/index.md
  - title: 証明法
    path: /math/foundations/proofs/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 証明法（入門）
    path: /math/foundations/proofs/introduction.md
  - title: 論理・必要十分条件（標準）
    path: /math/foundations/logic/standard.md
  - title: 自然数（標準）
    path: /math/numbers/natural-numbers/standard.md
---

## 証明の構造

数学的証明は次の要素からなります。

- **仮定**：何を前提とするか
- **結論**：何を示すか
- **論理の連鎖**：仮定から結論に至る有限のステップ

証明を書くとき、「何を使ってよいか（既知の定理・定義）」と「何を示すか（結論）」を最初に明確にします。

---

## 直接証明

仮定 $P$ から出発し、論理的推論で $Q$ を導きます。

**定理**：整数 $a, b$ が奇数ならば $ab$ は奇数。

**証明**：$a = 2m+1$、$b = 2n+1$（$m, n \in \mathbb{Z}$）とおくと$ab = (2m+1)(2n+1) = 4mn+2m+2n+1 = 2(2mn+m+n)+1$$2mn+m+n \in \mathbb{Z}$ なので $ab$ は奇数。$\square$

---

## 対偶証明

$P \Rightarrow Q$ と $\lnot Q \Rightarrow \lnot P$ は論理的に同値（論理・必要十分条件（標準）参照）。

**使いどころ**：$Q$ が「でない」という形で書きやすいとき。

**定理**：$n^2$ が3の倍数ならば $n$ は3の倍数。

**証明**（対偶）：$n$ が3の倍数でないとき $n^2$ は3の倍数でないことを示します。$n = 3k+1$ のとき $n^2 = 9k^2+6k+1 = 3(3k^2+2k)+1$（3の倍数でない）。$n = 3k+2$ のとき $n^2 = 9k^2+12k+4 = 3(3k^2+4k+1)+1$（3の倍数でない）。$\square$

---

## 背理法

$P$ を否定して矛盾を導くことで $P$ を証明します。

**使いどころ**：「存在しない」「無限に多い」など直接示しにくい命題。

**定理**：素数は無限に存在する。

**証明**：素数が有限個 $p_1, p_2, \ldots, p_k$ しかないと仮定します。$N = p_1 p_2 \cdots p_k + 1$ を考えると、$N$ はどの $p_i$ でも割り切れません（余り1）。よって $N$ は新たな素数を因数に持つか、$N$ 自身が素数——いずれも仮定に矛盾。$\square$

---

## 数学的帰納法

**定理（数学的帰納法の原理）**：命題 $P(n)$（$n \in \mathbb{N}$）について、(i) $P(1)$ が成立し、(ii) $P(k)$ が成立するとき $P(k+1)$ も成立するならば、すべての $n \in \mathbb{N}$ で $P(n)$ が成立する。

**例題**：$\sum_{k=1}^n k^2 = \frac{n(n+1)(2n+1)}{6}$ を示してください。

基底：$n=1$ のとき両辺 $= 1$。✓

帰納段階：$n=m$ で成立と仮定します。$n=m+1$ のとき$\sum_{k=1}^{m+1} k^2 = \frac{m(m+1)(2m+1)}{6} + (m+1)^2$$= (m+1)\left(\frac{m(2m+1)}{6} + (m+1)\right) = (m+1) \cdot \frac{2m^2+7m+6}{6}$$= \frac{(m+1)(m+2)(2m+3)}{6}$。$\square$

---

## 強い帰納法

通常の帰納法では「$k$ のとき成立」を仮定しますが、強い帰納法では「$1, 2, \ldots, k$ のすべてで成立」を仮定できます。

**使いどころ**：$P(k+1)$ の証明に $P(k)$ だけでなく $P(k-1), \ldots$ も必要なとき。

**例**：算術の基本定理（すべての自然数は素因数分解を持つ）の存在証明（自然数（専門）参照）。

---

## 関連ページ

- [論理・必要十分条件（標準）](../logic/standard.md)
- [自然数（専門）](../../numbers/natural-numbers/professional.md)
