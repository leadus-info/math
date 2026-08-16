---
title: 無理数
description: "2の平方根が整数の比である分数で表せない無理数であることを、既約分数で表せると仮定して矛盾を導く背理法によって証明する方法を扱う"
goal: "平方根を例に無理数が存在することを、背理法を使って説明できるようになる"
tags: [math, numbers, real-numbers]
stage: intermediate
subject: 数
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 中級編
    path: ../index.md
  - title: 無理数
    path: irrational-numbers.md
requires:
  - title: 有理数
    path: rational-numbers.md
  - title: 平方根
    path: arithmetic-square-root.md
---

## 平方根と無理数の存在

$\sqrt{2}$（2乗すると2になる正の数）は、分数で表すことができません。これを確かめてみましょう。

**証明**：$\sqrt{2}$ が有理数だと仮定し、これ以上約分できない分数（既約分数）$\dfrac{p}{q}$ で表せるとします。

$$\sqrt{2} = \frac{p}{q} \implies 2 = \frac{p^2}{q^2} \implies p^2 = 2q^2$$

$p^2$ が偶数なので $p$ も偶数です（奇数の2乗は必ず奇数になるので、$p$ が奇数だと $p^2$ も奇数になってしまい、$p^2$ が偶数であることに矛盾します）。$p = 2m$ とおくと、

$$(2m)^2 = 2q^2 \implies 4m^2 = 2q^2 \implies q^2 = 2m^2$$

同じ理由で $q$ も偶数になります。しかし $p, q$ がどちらも偶数だと、既約分数（それ以上約分できない）という最初の仮定に矛盾します。よって $\sqrt{2}$ は有理数ではありません。$\square$

この証明は、証明法で扱う**背理法**の代表的な例です。$\sqrt{2}$ は小数で書くと $1.41421356\ldots$ と、繰り返しのパターンなく永遠に続く無理数です。

---

## まとめ

$\sqrt{2}$ のように分数でどうしても表せない数（無理数）が存在することが、背理法によって証明できます。有理数と無理数を合わせた数の全体は、実数でさらに詳しく扱います。

---

## 関連ページ

- [背理法](../../advanced/foundations/proofs-contradiction.md)
- [実数](../../bachelor/numbers/real-numbers.md)
