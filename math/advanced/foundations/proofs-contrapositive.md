---
title: 対偶証明
description: "同値な対偶を示す"
goal: "対偶証明の考え方を理解し、対偶を使った証明を書けるようになる"
tags: [math, foundations, proofs]
stage: 応用編
subject: 基礎
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 応用編
    path: /math/advanced/index.md
  - title: 対偶証明
    path: /math/advanced/foundations/proofs-contrapositive.md
requires:
  - title: 証明法
    path: proofs.md
---

## 同値な対偶を示す

必要・十分条件（応用編）で見た通り、「$P$ ならば $Q$」と対偶「$\neg Q$ ならば $\neg P$」は同値です。$Q$ が「でない」という形で書きやすいときに使います。

**例題**：「$n^2$ が偶数ならば $n$ は偶数」を証明する。対偶「$n$ が奇数ならば $n^2$ は奇数」を示す。$n = 2k+1$ とおくと $n^2 = 4k^2+4k+1 = 2(2k^2+2k)+1$ で奇数。$\square$

---

## まとめ

対偶証明は、示したい命題の対偶（同値な命題）を代わりに示す方法です。結論を否定した形が扱いやすいときに有効です。

---

## 関連ページ

- [証明法（応用編）](proofs.md)
- [背理法（応用編）](proofs-contradiction.md)
