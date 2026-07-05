---
title: 微分の厳密な定義
description: "微分可能性を極限を用いて厳密に定義し、微分可能ならば連続であることの証明、絶対値関数を用いた連続だが微分不可能な反例の証明、至る所微分不可能なワイエルシュトラス関数を示したうえで、偏微分・全微分・ヤコビ行列による多変数への拡張とフレシェ微分への一般化を扱う"
goal: "微分可能ならば連続であることを証明し、連続だが微分不可能な例を証明つきで説明し、偏微分・全微分・ヤコビ行列による多変数への一般化を扱えるようになる"
tags: [math, analysis, derivatives]
stage: bachelor
subject: 解析
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 微分の厳密な定義
    path: differentiability.md
requires:
  - title: 微分
    path: ../../advanced/analysis/derivatives.md
  - title: 極限の厳密な定義
    path: epsilon-delta.md
  - title: 行列の積
    path: ../linear-algebra/matrices-product.md
---

## 微分可能性と連続性

**定義**：$f: \mathbb{R} \to \mathbb{R}$ が $x_0$ で微分可能であるとは、

$$f'(x_0) = \lim_{h \to 0} \frac{f(x_0+h) - f(x_0)}{h}$$

がε-δ論法の意味で存在することです。

**定理**：$f$ が $x_0$ で微分可能ならば、$f$ は $x_0$ で連続である。

**証明**：$f$ が $x_0$ で微分可能であるとは、極限 $f'(x_0) = \displaystyle\lim_{h \to 0} \frac{f(x_0+h) - f(x_0)}{h}$ が存在することです。$h \neq 0$ のとき、

$$f(x_0+h) - f(x_0) = \frac{f(x_0+h) - f(x_0)}{h} \cdot h$$

と書けるので、両辺の $h \to 0$ での極限を考えると、極限の積の性質（それぞれの極限が存在すれば積の極限は極限の積に等しい）から、

$$\lim_{h \to 0} \bigl(f(x_0+h) - f(x_0)\bigr) = \left(\lim_{h \to 0} \frac{f(x_0+h) - f(x_0)}{h}\right) \cdot \left(\lim_{h \to 0} h\right) = f'(x_0) \cdot 0 = 0$$

よって $\displaystyle\lim_{h \to 0} f(x_0+h) = f(x_0)$、すなわち $f$ は $x_0$ で連続です。$\blacksquare$

---

## 逆は成り立たない：連続だが微分不可能な例

上の定理の逆、すなわち「連続ならば微分可能」は成り立ちません。最も基本的な反例は $f(x) = |x|$ です。

**命題**：$f(x) = |x|$ は $x=0$ で連続だが微分可能でない。

**証明**：連続性は $\displaystyle\lim_{h\to 0}|h| = 0 = f(0)$ より明らかです。微分可能性を調べるため、右側極限と左側極限をそれぞれ計算します。

$$\lim_{h \to 0^+} \frac{f(0+h)-f(0)}{h} = \lim_{h \to 0^+} \frac{|h|}{h} = \lim_{h \to 0^+} \frac{h}{h} = 1$$

$$\lim_{h \to 0^-} \frac{f(0+h)-f(0)}{h} = \lim_{h \to 0^-} \frac{|h|}{h} = \lim_{h \to 0^-} \frac{-h}{h} = -1$$

右側極限と左側極限が一致しない（$1 \neq -1$）ため、$\displaystyle\lim_{h\to 0}\frac{f(h)-f(0)}{h}$ 自体は存在しません。よって $f$ は $x=0$ で微分可能ではありません。$\blacksquare$

グラフで見ると、$x=0$ で折れ曲がっており、接線の傾きが左右で食い違う（$-1$ と $1$）ため、ただ1つの接線が定まらないことに対応します。

**至る所微分不可能な連続関数（ワイエルシュトラス関数）**：$|x|$ の非微分可能性は $x=0$ という1点だけでしたが、もっと極端に、**定義域のどの点でも微分不可能**でありながら**至る所連続**であるような関数も存在します。

$$f(x) = \sum_{n=0}^{\infty} a^n \cos(b^n \pi x) \quad (0 < a < 1,\ b\text{ は奇数},\ ab > 1 + 3\pi/2)$$

がその例です。各項が有界かつ係数 $a^n$ が幾何級数的に減衰するためワイヤストラスのM判定法により級数は一様収束し、$f$ は至る所連続になります。一方で微分可能性については、どの点 $x_0$ をとっても差分商 $\frac{f(x_0+h)-f(x_0)}{h}$ が $h\to 0$ で振動して収束しないことが示され（$b$ が十分大きい高周波成分が差分商を支配し続けるため）、至る所微分不可能になります。この証明は級数の評価が煩雑なため、完全な証明は原論文・教科書に譲ります。

**参考文献**：Weierstrass, K. (1872). Über continuirliche Functionen eines reellen Argumentes. *Monatsber. Königl. Preuss. Akad. Wiss. Berlin*, 71–74.\
Rudin, W. (1976). *Principles of Mathematical Analysis* (3rd ed.). McGraw-Hill. (Weierstrass関数の完全な証明を含む)

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

微分可能性は極限として厳密に定義され、微分可能ならば連続であることは差分商の極限の積として証明できます。逆は成り立たず、$f(x)=|x|$ が $x=0$ で連続だが微分不可能な最も基本的な反例（左右の微分係数が一致しない）で、ワイエルシュトラス関数はさらに極端な「至る所連続・至る所微分不可能」な例です。多変数関数では偏微分だけでは不十分で、全微分可能性という強い条件のもとでヤコビ行列による一般化が意味を持ち、これはさらに無限次元のフレシェ微分へと一般化されます。

---

## 関連ページ

- [リーマン積分（発展編）](riemann-integral.md)
