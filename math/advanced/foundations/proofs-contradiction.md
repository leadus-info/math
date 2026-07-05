---
title: 背理法
description: "命題の否定を仮定して矛盾を導き元の命題を証明する背理法の考え方を、素数が無限に存在することの証明を例に扱う"
goal: "背理法の考え方を理解し、存在や無限性に関する命題を背理法で証明できるようになる"
tags: [math, foundations, proofs]
stage: advanced
subject: 基礎
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 応用編
    path: ../index.md
  - title: 背理法
    path: proofs-contradiction.md
requires:
  - title: 証明法
    path: proofs.md
---

## 否定を仮定して矛盾を導く

「$P$ が成り立たない」と仮定して矛盾を導き、「$P$ は成り立つ」と結論します。「存在しない」「無限に多い」など直接示しにくい命題に使います。

**定理**：素数は無限に存在する。

**証明**：素数が有限個 $p_1, p_2, \ldots, p_k$ しかないと仮定します。$N = p_1 p_2 \cdots p_k + 1$ を考えると、$N$ はどの $p_i$ で割っても余り1で割り切れません。よって $N$ は新たな素数を因数に持つか、$N$ 自身が素数——いずれも「素数は有限個」という仮定に矛盾します。$\square$

---

## まとめ

背理法は、示したい命題の否定を仮定し、矛盾を導くことで元の命題が正しいと結論する証明法です。

---

## 関連ページ

- [数学的帰納法（応用編）](proofs-induction.md)
