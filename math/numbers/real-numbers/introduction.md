---
title: 実数
description: "数直線上のすべての数"
goal: "実数が有理数と無理数を合わせたものであることを理解し、無理数の存在を具体例で説明できるようになる"
tags: [math,numbers,real-numbers]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 実数
    path: /math/numbers/real-numbers/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 分数（入門）
    path: /math/numbers/fractions/introduction.md
  - title: 小数（入門）
    path: /math/numbers/decimals/introduction.md
---

## 数直線に「穴」がある？

$1$、$2$、$3$……自然数は数直線の上にポツポツと並んでいます。分数を加えると、$\frac{1}{2}$ や $\frac{1}{3}$ がその間を埋めます。どんな2つの有理数の間にも別の有理数が入るので、隙間なく並んでいるように思えます。

ところが実際には「穴」があります。

$\sqrt{2}$ ——「2乗すると2になる数」は、どんな分数でも表せません。数直線の上には確かにその場所があるのに、有理数の世界には存在しない。

---

## 有理数と無理数

分数 $\frac{p}{q}$（$p, q$ は整数、$q \neq 0$）で表せる数を**有理数**といいます。有限小数や循環小数はすべて有理数です。

一方、$\sqrt{2}$ や円周率 $\pi$ のように、どんな分数でも表せない数を**無理数**といいます。無理数を小数で書くと、永遠に続いて繰り返しもありません。

$$\sqrt{2} = 1.41421356\ldots, \quad \pi = 3.14159265\ldots$$

---

## 実数とは

有理数と無理数を合わせた数全体を**実数**といいます。実数は数直線上の点と1対1に対応し、数直線に「穴」を残しません。

$$\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R}$$

---

## $\sqrt{2}$ が無理数であること

$\sqrt{2} = \frac{p}{q}$（既約分数）と仮定すると——$p^2 = 2q^2$ なので $p$ は偶数。$p = 2m$ とおくと $q^2 = 2m^2$ となり $q$ も偶数になります。$p$ と $q$ がともに偶数では既約分数にならないので、矛盾です。

これは証明法（入門）で見た**背理法**の典型的な応用です。

---

## 関連ページ

- [小数（入門）](../decimals/introduction.md)
- [分数（入門）](../fractions/introduction.md)
- [証明法（入門）](../../foundations/proofs/introduction.md)
