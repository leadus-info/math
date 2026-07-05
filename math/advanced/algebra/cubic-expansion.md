---
title: 三次の乗法公式
description: "立方の展開と因数分解の公式"
goal: "三次の乗法公式を使って式を展開・因数分解できるようになる"
tags: [math, algebra, expressions]
stage: advanced
subject: 代数
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 応用編
    path: ../index.md
  - title: 三次の乗法公式
    path: cubic-expansion.md
requires:
  - title: 展開・因数分解
    path: ../../intermediate/algebra/expressions-expansion-factoring.md
---

## 立方の展開

展開・因数分解（中級編）で見た2次の乗法公式には、3次のバージョンがあります。

$$(a+b)^3 = a^3 + 3a^2b + 3ab^2 + b^3$$
$$(a-b)^3 = a^3 - 3a^2b + 3ab^2 - b^3$$

**例**：$(x+2)^3 = x^3 + 3\cdot x^2\cdot2 + 3\cdot x\cdot4 + 8 = x^3+6x^2+12x+8$

---

## 立方の和・差の因数分解

$a^3+b^3$、$a^3-b^3$ は、次の公式で因数分解できます。

$$a^3+b^3 = (a+b)(a^2-ab+b^2)$$
$$a^3-b^3 = (a-b)(a^2+ab+b^2)$$

これらは、右辺を実際に展開して確かめられます。$(a+b)(a^2-ab+b^2) = a^3-a^2b+ab^2+a^2b-ab^2+b^3 = a^3+b^3$。

**例**：$x^3-8 = x^3-2^3 = (x-2)(x^2+2x+4)$

---

## 公式を使いこなす

これらの公式は、2次の乗法公式と組み合わせて使うことがよくあります。

**例題**：$x^3+3x^2+3x+1$ を因数分解する。$(a+b)^3$ の形とみると $a=x$、$b=1$ で、$x^3+3x^2\cdot1+3x\cdot1^2+1^3=(x+1)^3$。

---

## まとめ

3次の乗法公式 $(a\pm b)^3$ と、立方の和・差の因数分解 $a^3\pm b^3=(a\pm b)(a^2\mp ab+b^2)$ を使うと、3次式の展開・因数分解が素早くできます。

---

## 関連ページ

- [整式の除法と剰余の定理（応用編）](polynomial-division.md)
