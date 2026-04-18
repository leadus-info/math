---
title: 乗法・べき乗
description: "指数法則と累乗根の体系的な扱い"
goal: "指数法則を整数・有理数の指数に拡張し、累乗根との関係を理解して計算できるようになる"
tags: [math,numbers,arithmetic]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 乗法・べき乗
    path: /math/numbers/arithmetic/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 乗法・べき乗（入門）
    path: /math/numbers/arithmetic/introduction.md
  - title: 自然数（標準）
    path: /math/numbers/natural-numbers/standard.md
  - title: 負数（標準）
    path: /math/numbers/negative-numbers/standard.md
  - title: 分数（標準）
    path: /math/numbers/fractions/standard.md
---

## 自然数の指数から始める

乗法・べき乗（入門）で、$a^n$ を「$a$ を $n$ 回掛ける」として定義しました。ここでは指数を整数・有理数へ拡張します。

---

## 指数法則

$a > 0$、$m, n$ が自然数のとき、以下の法則が成り立ちます。

$$a^m \times a^n = a^{m+n}$$
$$a^m \div a^n = a^{m-n}$$
$$(a^m)^n = a^{mn}$$
$$(ab)^n = a^n b^n$$

**例**：$2^5 \div 2^3 = 2^{5-3} = 2^2 = 4$、$(3^2)^4 = 3^8 = 6561$

---

## 指数を0と負の整数に拡張する

$a^3 \div a^3 = 1$ ですが、指数法則を使うと $a^{3-3} = a^0$ になります。この矛盾を避けるために定義します。

$$a^0 = 1 \quad (a \neq 0)$$

さらに $a^1 \div a^3 = \frac{1}{a^2}$ ですが、指数法則では $a^{1-3} = a^{-2}$ なので、

$$a^{-n} = \frac{1}{a^n} \quad (a \neq 0)$$

と定義します。これにより指数法則が整数全体で成り立ちます。

**例**：$2^{-3} = \frac{1}{8}$、$10^{-2} = \frac{1}{100} = 0.01$

---

## 指数を有理数に拡張する

$a^{1/2}$ はどう定義すればよいでしょうか。指数法則 $(a^{1/2})^2 = a^1 = a$ から、$a^{1/2}$ は「2乗すると $a$ になる数」、つまり $\sqrt{a}$ です。

$$a^{1/n} = \sqrt[n]{a} \quad (a \geq 0, n \in \mathbb{N})$$

$$a^{m/n} = (a^{1/n})^m = (\sqrt[n]{a})^m \quad (a \geq 0)$$

**例**：$8^{2/3} = (\sqrt[3]{8})^2 = 2^2 = 4$、$4^{3/2} = (\sqrt{4})^3 = 2^3 = 8$

---

## 累乗根の計算規則

$$\sqrt[n]{ab} = \sqrt[n]{a} \cdot \sqrt[n]{b}$$
$$\sqrt[n]{\frac{a}{b}} = \frac{\sqrt[n]{a}}{\sqrt[n]{b}}$$
$$\sqrt[m]{\sqrt[n]{a}} = \sqrt[mn]{a}$$

**例題**：$\sqrt{12}$ を簡単にしてください。

$\sqrt{12} = \sqrt{4 \times 3} = \sqrt{4} \cdot \sqrt{3} = 2\sqrt{3}$

**例題**：$\frac{\sqrt{18}}{\sqrt{2}}$ を計算してください。

$\frac{\sqrt{18}}{\sqrt{2}} = \sqrt{\frac{18}{2}} = \sqrt{9} = 3$

---

## 関連ページ

- [指数関数（標準）](../../functions/exponential/standard.md)
- [対数関数（標準）](../../functions/logarithmic/standard.md)
