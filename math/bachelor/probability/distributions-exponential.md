---
title: 指数分布
description: "ポアソン過程における次の事象までの待ち時間が従う指数分布の定義・期待値・分散と、過去の経過時間に依存しない無記憶性という性質を解説する"
goal: "指数分布の定義と無記憶性を理解できるようになる"
tags: [math, probability, distributions]
stage: bachelor
subject: 確率
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 指数分布
    path: distributions-exponential.md
requires:
  - title: 正規分布
    path: distributions-normal.md
---

## $\mathrm{Exp}(\lambda)$

ポアソン過程での待ち時間の分布：

$$f(x) = \lambda e^{-\lambda x} \quad (x \geq 0), \qquad E[X] = \frac{1}{\lambda}, \quad \mathrm{Var}(X) = \frac{1}{\lambda^2}$$

**無記憶性**：$P(X > s + t \mid X > s) = P(X > t)$（すでに $s$ 待った事実が、追加の待ち時間の分布に影響しない）。

---

## まとめ

指数分布は、ポアソン過程における待ち時間を表す分布で、無記憶性（過去の経過時間が今後の待ち時間の分布に影響しない）という特徴的な性質を持ちます。

---

## 関連ページ

- [確率分布（発展編）](distributions.md)
