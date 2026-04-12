---
title: 複素数
description: "複素数体の構成と代数学の基本定理"
goal: "$\\mathbb{C}$ の代数的構成を説明でき、代数学の基本定理の証明の方針を述べられるようになる"
tags: [math,numbers,complex-numbers]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 複素数
    path: /math/numbers/complex-numbers/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 複素数（標準）
    path: /math/numbers/complex-numbers/standard.md
  - title: 負数（専門）
    path: /math/numbers/negative-numbers/professional.md
  - title: 集合（入門）
    path: /math/math-language/sets/introduction.md
---

## $\mathbb{C}$ の代数的構成

複素数（標準）では $i^2 = -1$ を満たす数 $i$ を「導入した」と述べましたが、ここではそのような数が矛盾なく存在することを構成的に示します。

$\mathbb{R}[x]$ を実数係数多項式環とします。$x^2 + 1$ は $\mathbb{R}[x]$ の既約多項式です（実数の範囲では根を持たない）。剰余環

$$\mathbb{C} := \mathbb{R}[x] / (x^2 + 1)$$

を定義します。$(x^2 + 1)$ はイデアルであり、$x^2 + 1$ が既約なのでこのイデアルは極大イデアルです。よって $\mathbb{C}$ は体です。

$\mathbb{C}$ の元は $a + bx \pmod{x^2 + 1}$（$a, b \in \mathbb{R}$）の形で一意に表され、$x$ の剰余類が虚数単位 $i$ に対応します。$x^2 \equiv -1 \pmod{x^2 + 1}$ なので $i^2 = -1$ が成り立ちます。

---

## $\mathbb{C}$ の体としての性質

$\mathbb{C}$ は以下の性質を持ちます。

- 加法について可換群：単位元 $0$、$a + bi$ の逆元は $-a - bi$
- 乗法について可換群（$0$ を除く）：単位元 $1$、$a + bi$ の逆元は $\frac{a - bi}{a^2 + b^2}$
- 分配法則

$\mathbb{R}$ は $\mathbb{C}$ の部分体です。$\mathbb{C}$ は $\mathbb{R}$ 上の $2$ 次元ベクトル空間であり、基底は $\{1, i\}$ です。

$\mathbb{C}$ は順序体ではありません。$\mathbb{C}$ 上には、体の演算と両立する全順序を定義することができません。

証明：$i > 0$ と仮定すると $i^2 = -1 > 0$ となり矛盾。$i < 0$ と仮定すると $-i > 0$ なので $(-i)^2 = -1 > 0$ となりやはり矛盾。$\square$

---

## 代数学の基本定理

**定理**：$n \geq 1$ 次の複素係数多項式は、$\mathbb{C}$ 内に少なくとも1つの根を持つ。

同値な言い換え：$\mathbb{C}$ は**代数的閉体**である。すなわち、$\mathbb{C}$ の代数的拡大は $\mathbb{C}$ 自身のみである。

**系**：$n$ 次の複素係数多項式は（重複を込めて）$n$ 個の根を持ち、$\mathbb{C}$ 上で1次式の積に分解される。

$$p(z) = c(z - z_1)(z - z_2) \cdots (z - z_n)$$

### 証明の方針（リュービルの定理による）

$p(z)$ を $n \geq 1$ 次多項式とし、$p(z) \neq 0$（$\forall z \in \mathbb{C}$）と仮定します。$f(z) = \frac{1}{p(z)}$ は $\mathbb{C}$ 全体で正則です。$|z| \to \infty$ で $|p(z)| \to \infty$ なので $|f(z)| \to 0$ です。よって $f$ は有界な整関数であり、リュービルの定理より $f$ は定数。しかし $p$ は $n \geq 1$ 次なので $f$ は定数ではなく矛盾。$\square$

この証明は複素解析の道具（リュービルの定理）を用います。純代数的な証明も存在しますが、$\mathbb{R}$ の完備性を本質的に使います。

**参考文献**：Lang, S. (2002). *Algebra* (Revised 3rd ed.). Springer.

---

## 関連ページ

- [複素数（標準）](standard.md)
- [負数（専門）](../negative-numbers/professional.md)
- [複素関数（専門）](../../functions/complex-functions/professional.md)