---
title: 微分の厳密な定義
description: "微分可能性の厳密な定義と多変数への拡張"
goal: "微分可能性を厳密に定義し、連続性との関係と反例を説明し、偏微分・全微分・ヤコビ行列による多変数への一般化を扱えるようになる"
tags: [math, analysis, derivatives]
stage: 発展編
subject: 解析
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 発展編
    path: /math/bachelor/index.md
  - title: 微分の厳密な定義
    path: /math/bachelor/analysis/differentiability.md
requires:
  - title: 微分
    path: /math/advanced/analysis/derivatives.md
  - title: 極限の厳密な定義
    path: /math/bachelor/analysis/epsilon-delta.md
  - title: 行列の積
    path: /math/bachelor/linear-algebra/matrices-product.md
---

## 微分可能性と連続性

**定義**：$f: \mathbb{R} \to \mathbb{R}$ が $x_0$ で微分可能であるとは、

$$f'(x_0) = \lim_{h \to 0} \frac{f(x_0+h) - f(x_0)}{h}$$

がε-δ論法の意味で存在することです。

**定理**：微分可能 $\Rightarrow$ 連続。

逆は成り立ちません。連続でも微分可能とは限らないのです。

**反例（ワイエルシュトラス関数）**：

$$f(x) = \sum_{n=0}^{\infty} a^n \cos(b^n \pi x) \quad (0 < a < 1,\ b\text{ は奇数},\ ab > 1 + 3\pi/2)$$

は至る所連続であるにもかかわらず、至る所微分不可能です。応用編の「微分」で扱った直感的な理解（接線が引ける）が、実は連続性だけからは保証されないことを示す典型例です。

**参考文献**：Weierstrass, K. (1872). Über continuirliche Functionen eines reellen Argumentes. *Monatsber. Königl. Preuss. Akad. Wiss. Berlin*, 71–74.

---

## 多変数への拡張：偏微分と全微分

1変数の微分は、複数の変数を持つ関数 $f: \mathbb{R}^n \to \mathbb{R}$ に一般化できます。

**偏微分**：他の変数を固定して1変数だけ動かす極限。

$$\frac{\partial f}{\partial x_i} = \lim_{h\to 0} \frac{f(x + he_i) - f(x)}{h}$$

しかし、すべての偏微分が存在しても $f$ が「なめらか」とは限りません。より強い条件が**全微分可能性**です。

**定義**：線形写像 $A$ が存在して $f(x+h) = f(x) + Ah + o(\|h\|)$（$h \to 0$）が成り立つとき、$f$ は**全微分可能**であるといい、$df = \sum_i \dfrac{\partial f}{\partial x_i}dx_i$ を**全微分**といいます。

$f: \mathbb{R}^n \to \mathbb{R}^m$ の微分は、偏微分を並べた**ヤコビ行列** $Jf = \left(\dfrac{\partial f_i}{\partial x_j}\right)$ で表され、連鎖律は行列の積の形になります。

$$J(g \circ f) = Jg \cdot Jf$$

---

## さらに一般の空間での微分

ベクトルや行列にとどまらず、無限次元の関数空間（バナッハ空間）の間の写像にも微分の概念は拡張できます。バナッハ空間 $X, Y$ 上の写像 $F: X \to Y$ が $x_0$ で**フレシェ微分可能**であるとは、有界線形写像 $A: X \to Y$ が存在して

$$\lim_{\|h\|\to 0} \frac{\|F(x_0+h) - F(x_0) - Ah\|}{\|h\|} = 0$$

が成り立つことです。この $A$ をフレシェ微分といい、$n$ 変数関数のヤコビ行列による微分は、この一般的な定義の特別な場合にあたります。

**参考文献**：Spivak, M. (1965). *Calculus on Manifolds*. Benjamin.

---

## まとめ

微分可能性は極限として厳密に定義され、微分可能ならば連続ですが逆は成り立ちません（ワイエルシュトラス関数が反例）。多変数関数では偏微分だけでは不十分で、全微分可能性という強い条件のもとでヤコビ行列による一般化が意味を持ち、これはさらに無限次元のフレシェ微分へと一般化されます。

---

## 関連ページ

- [リーマン積分（発展編）](riemann-integral.md)
