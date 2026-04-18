---
title: 代数
description: "展開公式・因数分解・剰余定理"
goal: "主要な展開公式と因数分解の手法を使いこなし、剰余定理・因数定理を適用できるようになる"
tags: [math,math-language,algebra]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数学の言語
    path: /math/algebra/index.md
  - title: 代数
    path: /math/algebra/expressions/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 代数（入門）
    path: /math/algebra/expressions/introduction.md
  - title: 負数（標準）
    path: /math/numbers/integers/standard.md
---

## 展開公式

代数（入門）では分配法則を使って括弧を外す方法を見ました。よく使う展開の結果を公式としてまとめます。

$$(a + b)^2 = a^2 + 2ab + b^2$$

$$(a - b)^2 = a^2 - 2ab + b^2$$

$$(a + b)(a - b) = a^2 - b^2$$

$$(a + b)^3 = a^3 + 3a^2b + 3ab^2 + b^3$$

これらはすべて分配法則を繰り返し適用した結果です。たとえば $(a + b)^2 = (a + b)(a + b) = a^2 + ab + ba + b^2 = a^2 + 2ab + b^2$。

---

## 因数分解の手法

展開公式を逆方向に使うのが因数分解の基本です。

### 共通因数のくくり出し

$$6x^2 + 9x = 3x(2x + 3)$$

各項に共通する因数を先に外します。

### 和と積による分解

$x^2 + 5x + 6$ を因数分解するには、「足して5、掛けて6になる2数」を探します。$2 + 3 = 5$、$2 \times 3 = 6$ なので、

$$x^2 + 5x + 6 = (x + 2)(x + 3)$$

### 差の平方公式の利用

$$x^2 - 9 = x^2 - 3^2 = (x + 3)(x - 3)$$

---

## 剰余定理と因数定理

**剰余定理**：多項式 $f(x)$ を $(x - a)$ で割ったときの余りは $f(a)$ です。

**因数定理**：$f(a) = 0$ ならば $(x - a)$ は $f(x)$ の因数です。

因数定理は剰余定理の特別な場合です。$f(x) = (x - a) \times q(x) + f(a)$ と書けるので、$f(a) = 0$ なら $f(x) = (x - a) \times q(x)$ となります。

**例**：$f(x) = x^2 - 5x + 6$。$f(2) = 4 - 10 + 6 = 0$ なので $(x - 2)$ は因数。割り算すると $f(x) = (x - 2)(x - 3)$。

---

## 関連ページ

- [等号・等式（標準）](../equations/standard.md) — 方程式の解法
- [多項式（入門）](../polynomials/introduction.md)