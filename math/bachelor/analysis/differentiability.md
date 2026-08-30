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

がその例です。各項が有界かつ係数 $a^n$ が幾何級数的に減衰するため、ワイエルシュトラスのM判定法により級数は一様収束し、$f$ は至る所連続になります。ワイエルシュトラスのM判定法とは、各項の絶対値を上から抑える数列 $\{M_n\}$ が存在し、級数 $\sum M_n$ が収束すれば、もとの級数は一様収束するという判定法のことです（ここでは $M_n = a^n$ として、幾何級数 $\sum a^n$ の収束に対応させています）。

一方で微分可能性については、どの点 $x_0$ をとっても差分商 $\frac{f(x_0+h)-f(x_0)}{h}$ が $h\to 0$ で振動して収束しないことが示され（$b$ が十分大きい高周波成分が差分商を支配し続けるため）、至る所微分不可能になります。この証明は級数の評価が煩雑なため、完全な証明は原論文・教科書に譲ります。

**参考文献**：Weierstrass, K. (1872). Über continuirliche Functionen eines reellen Argumentes. *Monatsber. Königl. Preuss. Akad. Wiss. Berlin*, 71–74.\
Rudin, W. (1976). *Principles of Mathematical Analysis* (3rd ed.). McGraw-Hill. (Weierstrass関数の完全な証明を含む)

---

## 多変数への拡張：偏微分と全微分

1変数の微分は、複数の変数を持つ関数 $f: \mathbb{R}^n \to \mathbb{R}$ に一般化できます。

**偏微分**：他の変数を固定して1変数だけ動かす極限。

$$\frac{\partial f}{\partial x_i} = \lim_{h\to 0} \frac{f(x + he_i) - f(x)}{h}$$

しかし、すべての偏微分が存在しても $f$ が連続であるとは限りません。例えば、$f(0,0) = 0$、$(x,y) \neq (0,0)$ のとき $f(x,y) = \dfrac{xy}{x^2+y^2}$ で定める関数を考えます。原点での偏微分は

$$\frac{\partial f}{\partial x}(0,0) = \lim_{h\to 0}\frac{f(h,0)-f(0,0)}{h} = \lim_{h\to 0}\frac{0}{h} = 0$$

となり、同様に $\dfrac{\partial f}{\partial y}(0,0) = 0$ も存在します。しかし $y=x$ に沿って原点に近づくと $f(x,x) = \dfrac{x^2}{2x^2} = \dfrac{1}{2}$（$x\neq 0$）となり $f(0,0)=0$ に収束しないため、$f$ は原点で連続ではありません。このように偏微分の存在だけでは不十分であり、より強い条件が**全微分可能性**です。

**定義**：線形写像 $A$ が存在して $f(x+h) = f(x) + Ah + o(\|h\|)$（$h \to 0$）が成り立つとき、$f$ は**全微分可能**であるといいます。ここで $o(\|h\|)$ とは、$h \to 0$ のとき $\|h\|$ で割った極限が0になるような量を表します。

全微分可能ならば、すべての偏微分が存在します。実際、$h = te_i$（$t$ はスカラー）として定義の式 $f(x+h) = f(x) + Ah + o(\|h\|)$ に代入し、両辺を $t$（$t\neq 0$）で割ると、

$$\frac{f(x+te_i)-f(x)}{t} = \frac{t\,Ae_i + o(|t|)}{t} = Ae_i + \frac{o(|t|)}{t}$$

ここで $t\to 0$ のとき $\dfrac{o(|t|)}{t}\to 0$ となるので、

$$\lim_{t\to 0}\frac{f(x+te_i)-f(x)}{t} = Ae_i$$

すなわち $\dfrac{\partial f}{\partial x_i} = Ae_i$ であり、線形写像 $A$ の第 $i$ 成分は $\dfrac{\partial f}{\partial x_i}$ に一致します。したがって $Ah = \sum_i \dfrac{\partial f}{\partial x_i}h_i$ であり、$df = \sum_i \dfrac{\partial f}{\partial x_i}dx_i$ を**全微分**といいます。

各成分 $f_i$ に対して同様の議論を適用すると、$f: \mathbb{R}^n \to \mathbb{R}^m$ の微分は、偏微分を並べた**ヤコビ行列** $Jf = \left(\dfrac{\partial f_i}{\partial x_j}\right)$ で表され、連鎖律は行列の積の形になります。

具体例として $f(x,y) = (x^2y,\ x+y)$（$f: \mathbb{R}^2 \to \mathbb{R}^2$）を考えると、各成分の偏微分は $\dfrac{\partial f_1}{\partial x}=2xy$、$\dfrac{\partial f_1}{\partial y}=x^2$、$\dfrac{\partial f_2}{\partial x}=1$、$\dfrac{\partial f_2}{\partial y}=1$ なので、ヤコビ行列は

$$Jf(x,y) = \begin{pmatrix} 2xy & x^2 \\ 1 & 1 \end{pmatrix}$$

となります。

$$J(g \circ f)(x) = Jg(f(x)) \cdot Jf(x)$$

ここで $Jg(f(x))$ は $y=f(x)$ における $g$ のヤコビ行列、$Jf(x)$ は $x$ における $f$ のヤコビ行列であり、異なる点での評価どうしの積であることに注意します。

この連鎖律は、全微分可能性の定義から次のようにスケッチできます。$f$ が $x$ で、$g$ が $y=f(x)$ でそれぞれ全微分可能であるとすると、$f(x+h) = f(x) + (Jf)h + o(\|h\|)$、$g(y+k) = g(y) + (Jg)k + o(\|k\|)$ が成り立ちます。

> [!NOTE]
> 以下、式中の $Jf$ は $x$ での、$Jg$ は $y=f(x)$ での評価を表すものとし、簡潔のため評価点の表記は省略します。

ここで $k = (Jf)h + o(\|h\|)$ を代入すると、

$$g(f(x+h)) = g(f(x)) + (Jg)\bigl[(Jf)h + o(\|h\|)\bigr] + o(\|k\|)$$

となります。$Jg$ は行列（線形写像）なので和に分配でき、$(Jg)\bigl[(Jf)h+o(\|h\|)\bigr] = (Jg)(Jf)h + (Jg)\,o(\|h\|)$ と展開できます。$Jg$ は行列なのでノルムを一定の定数倍で抑えられるため、$(Jg)\,o(\|h\|)$ は依然として $o(\|h\|)$ です。また $k = (Jf)h + o(\|h\|)$ より、$h\to 0$ のとき $k$ は $\|h\|$ の定数倍程度の大きさに収まる（$k = O(\|h\|)$）ため、$o(\|k\|) = o(\|h\|)$ となります。$\|k\|\le C\|h\|$（ある定数 $C$ について）と評価できるため、$\|k\|\to 0$ で $\|k\|$ より速く0に収束する量である $o(\|k\|)$ は、$\|h\|$ についても同じ速さで0に収束する量、すなわち $o(\|h\|)$ として扱えます。以上をまとめると、

$$g(f(x+h)) = g(f(x)) + Jg(f(x))\cdot Jf(x)\,h + o(\|h\|)$$

が得られ、これは合成関数 $g\circ f$ が $x$ で全微分可能であり、そのヤコビ行列が $J(g\circ f)(x) = Jg(f(x)) \cdot Jf(x)$ という評価点付きの形で線形写像の合成に一致することを示しています。$o(\|h\|)$ の項が実際に $o(\|h\|)$ になることの厳密な評価は煩雑になるため、ここでは証明の概略にとどめます。

具体例として、先ほどの $f(x,y) = (x^2y,\ x+y)$ に対し、$g(u,v) = (u+v^2,\ uv)$（$g: \mathbb{R}^2 \to \mathbb{R}^2$）を考えます。各成分の偏微分は $\dfrac{\partial g_1}{\partial u}=1$、$\dfrac{\partial g_1}{\partial v}=2v$、$\dfrac{\partial g_2}{\partial u}=v$、$\dfrac{\partial g_2}{\partial v}=u$ なので、ヤコビ行列は

$$Jg(u,v) = \begin{pmatrix} 1 & 2v \\ v & u \end{pmatrix}$$

です。$f$ の第1成分 $u=x^2y$、第2成分 $v=x+y$ を代入すると、

$$Jg(f(x,y)) = \begin{pmatrix} 1 & 2(x+y) \\ x+y & x^2y \end{pmatrix}$$

となるので、連鎖律 $J(g\circ f)(x,y) = Jg(f(x,y)) \cdot Jf(x,y)$ に先ほど求めた $Jf(x,y) = \begin{pmatrix} 2xy & x^2 \\ 1 & 1 \end{pmatrix}$ を代入して評価点ごとに具体的に計算すると、

$$J(g\circ f)(x,y) = \begin{pmatrix} 1 & 2(x+y) \\ x+y & x^2y \end{pmatrix}\begin{pmatrix} 2xy & x^2 \\ 1 & 1 \end{pmatrix} = \begin{pmatrix} 2xy+2x+2y & x^2+2x+2y \\ 3x^2y+2xy^2 & x^3+2x^2y \end{pmatrix}$$

となります。実際 $g(f(x,y)) = \bigl(x^2y+(x+y)^2,\ x^2y(x+y)\bigr) = (x^2y+x^2+2xy+y^2,\ x^3y+x^2y^2)$ を直接偏微分しても同じ結果が得られ、連鎖律が成り立っていることが確認できます。

なお、行列の積は一般に非可換（$AB \neq BA$）でしたが、ここでの積の順序 $Jg \cdot Jf$ は関数合成の順序 $g \circ f$ に対応しており、順序を入れ替えた $Jf \cdot Jg$（あるいは $J(f\circ g)$）とは一般に異なります。

---

## さらに一般の空間での微分

ベクトルや行列にとどまらず、無限次元の空間の間の写像にも微分の概念は拡張できます。完備性（コーシー列が必ず収束するという性質）を持つノルム空間（ベクトルの大きさを測る量であるノルムを備えたベクトル空間）を**バナッハ空間**といいます。無限次元の関数空間（例えば連続関数全体の空間）や、有限次元の $\mathbb{R}^n$ 自身も、適切なノルムを入れればいずれもバナッハ空間の例になります。

バナッハ空間 $X, Y$ 上の写像 $F: X \to Y$ が $x_0$ で**フレシェ微分可能**であるとは、**有界線形写像** $A: X \to Y$ が存在して

$$\lim_{\|h\|\to 0} \frac{\|F(x_0+h) - F(x_0) - Ah\|}{\|h\|} = 0$$

が成り立つことです。ここで有界線形写像とは、ある定数 $C > 0$ が存在して任意の $h$ に対し $\|Ah\| \le C\|h\|$ を満たす線形写像のことです。この $A$ をフレシェ微分といいます。

$n$ 変数関数のヤコビ行列による微分は、この一般的な定義の特別な場合にあたります。実際、$X = \mathbb{R}^n$、$Y = \mathbb{R}^m$ として標準的な内積・ノルムを入れた場合、有界線形写像はすべて行列で表され、$A$ はヤコビ行列 $Jf$ に一致します。

**参考文献**：Spivak, M. (1965). *Calculus on Manifolds*. Benjamin.

---

## まとめ

微分可能性は極限として厳密に定義され、微分可能ならば連続であることは差分商の極限の積として証明できます。逆は成り立たず、$f(x)=|x|$ が $x=0$ で連続だが微分不可能な最も基本的な反例（左右の微分係数が一致しない）で、ワイエルシュトラス関数はさらに極端な「至る所連続・至る所微分不可能」な例です。

多変数関数では、すべての偏微分が存在していても連続であるとは限らず（$f(x,y)=xy/(x^2+y^2)$ が反例）、偏微分だけでは不十分です。より強い条件である全微分可能性のもとでは、線形写像 $A$ の各成分が偏微分に一致することが示され、ヤコビ行列による一般化と連鎖律 $J(g\circ f)(x) = Jg(f(x)) \cdot Jf(x)$ が意味を持ちます。

これらの議論はさらに、無限次元のバナッハ空間の間の写像に対するフレシェ微分へと一般化されます。$X=\mathbb{R}^n, Y=\mathbb{R}^m$ の場合には有界線形写像がヤコビ行列に一致し、多変数の議論と整合します。

---

## 関連ページ

- [リーマン積分](riemann-integral.md)
