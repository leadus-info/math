---
title: 複素解析
description: "複素数を変数にとる複素関数を扱う複素解析について、正則性の定義から出発してコーシー・リーマン方程式を証明し、グリーンの定理を用いてコーシーの積分定理を証明し、留数定理とその工学的な応用までを解説する"
goal: "正則性の定義からコーシー・リーマン方程式を証明し、コーシーの積分定理の証明の概略を説明し、留数定理の使いどころを説明できるようになる"
tags: [math, analysis, complex-analysis]
stage: bachelor
subject: 解析
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 複素解析
    path: complex-analysis.md
requires:
  - title: 複素数
    path: ../../advanced/numbers/complex-numbers.md
  - title: 微分の厳密な定義
    path: differentiability.md
---

## 関数の「入力」を複素数にする

$f(x) = x^2$ では実数 $x$ を入れて実数が出ますが、複素数 $z = a+bi$ を入れると $f(z) = z^2 = a^2-b^2+2abi$ という複素数が出ます。このように「複素数を入れて複素数が出る」関数を**複素関数**といいます。

$z = x + iy$ とおくと $f(z) = u(x,y) + iv(x,y)$ と書け、実部 $u$ と虚部 $v$ はそれぞれ2変数の実関数になります。

実数の関数のグラフは2次元平面に描けますが、複素関数は「複素平面（2次元）から複素平面（2次元）への対応」なので、グラフを描こうとすると4次元が必要になります。そのため、複素関数は「ある領域の形が別の形にどう変換されるか」として視覚化されることが多いです。

---

## 正則性

**定義**：$f(z)$ が $z_0$ で**正則**（holomorphic）であるとは、

$$f'(z_0) = \lim_{h \to 0} \frac{f(z_0+h) - f(z_0)}{h} \quad (h \in \mathbb{C})$$

が存在することです。$h$ がどの方向の複素数から近づいても同じ値に収束する必要があり、これは実数の微分可能性より強い条件です。

「どの方向から見ても微分できる」関数は、実数の関数にはない強力な性質を持ちます。（詳しくは本記事の範囲を超えますが）正則関数はべき級数として展開できるため、ある点の近くの値の並びによって関数全体の振る舞いが決まってしまう——「部分を知れば全体がわかる」という性質です。

---

## コーシー・リーマン方程式

**定理**：$f = u + iv$ が $z_0=x_0+iy_0$ で正則ならば、次の偏微分方程式（**コーシー・リーマン方程式**）が成り立つ。

$$\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}, \qquad \frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x}$$

**証明**：正則性の定義より、極限 $f'(z_0) = \lim_{h\to 0}\dfrac{f(z_0+h)-f(z_0)}{h}$ は $h$（複素数）がどの方向から $0$ に近づいても同じ値に収束します。特に次の2つの近づき方で計算し、結果を比較します。

*$h$ が実数（$h = t$、$t \to 0$）の場合*：

$$f'(z_0) = \lim_{t \to 0} \frac{u(x_0+t,y_0) + iv(x_0+t,y_0) - u(x_0,y_0) - iv(x_0,y_0)}{t} = \frac{\partial u}{\partial x} + i\frac{\partial v}{\partial x}$$

*$h$ が純虚数（$h = it$、$t \to 0$）の場合*：

$$f'(z_0) = \lim_{t \to 0} \frac{u(x_0,y_0+t) + iv(x_0,y_0+t) - u(x_0,y_0) - iv(x_0,y_0)}{it} = \frac{1}{i}\frac{\partial u}{\partial y} + \frac{\partial v}{\partial y} = \frac{\partial v}{\partial y} - i\frac{\partial u}{\partial y}$$

ここで $\dfrac{1}{i}=-i$（$i\cdot(-i)=1$ より、あるいは分母分子に $-i$ を掛けて $\dfrac{1}{i}=\dfrac{-i}{i\cdot(-i)}=\dfrac{-i}{1}=-i$ と確認できます）を用いました。

正則性より、この2つは同じ値 $f'(z_0)$ に等しいので、実部どうし・虚部どうしを比較すると、

$$\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}, \qquad \frac{\partial v}{\partial x} = -\frac{\partial u}{\partial y}$$

が得られます。$\blacksquare$

> [!NOTE]
> 逆は単純には成り立ちません。コーシー・リーマン方程式を満たすだけでは正則性は保証されません。$u, v$ が $C^1$ 級（偏導関数が連続）であるという条件を追加すれば、コーシー・リーマン方程式から正則性を導くことができます。この意味で、必要十分条件として述べる場合は「$C^1$ 級かつコーシー・リーマン方程式を満たす」がより正確な言い方です。

**例**：$e^z = e^x(\cos y + i\sin y)$ は、実数の指数関数を複素数に拡張する自然な定義であり、$u=e^x\cos y$、$v=e^x\sin y$ とおくと、$\dfrac{\partial u}{\partial x}=e^x\cos y=\dfrac{\partial v}{\partial y}$、$\dfrac{\partial u}{\partial y}=-e^x\sin y=-\dfrac{\partial v}{\partial x}$ となり、この方程式を満たす正則関数です。

---

## コーシーの積分定理と留数定理

**コーシーの積分定理**：$f$ が単連結な領域（穴のない領域）$D$ で正則で、$C$ が $D$ 内の区分的に滑らかな（有限個の滑らかな弧をつないでできた）単純閉曲線（自己交差せず出発点に戻る閉曲線）ならば、

$$\oint_C f(z)\,dz = 0$$

**証明の概略**：$f=u+iv$、$dz=dx+i\,dy$ とすると、

$$f\,dz = (u+iv)(dx+i\,dy) = u\,dx + iu\,dy + iv\,dx - v\,dy = (u\,dx - v\,dy) + i(v\,dx + u\,dy)$$

より、線積分は

$$\oint_C f\,dz = \oint_C (u\,dx - v\,dy) + i\oint_C (v\,dx + u\,dy)$$

と実部・虚部に分解できます。$u,v$ が $C^1$ 級であれば、グリーンの定理（閉曲線 $C$ に沿った線積分 $\oint_C (P\,dx+Q\,dy)$ が、内部領域 $R$ 上の面積分 $\iint_R \left(\dfrac{\partial Q}{\partial x}-\dfrac{\partial P}{\partial y}\right)dA$ に等しいという定理）により、各線積分は $R$ 上の面積分に書き換えられます（1つ目の積分は $P=u,\,Q=-v$、2つ目の積分は $P=v,\,Q=u$ とした場合にあたります）。

$$\oint_C (u\,dx - v\,dy) = \iint_R \left(-\frac{\partial v}{\partial x} - \frac{\partial u}{\partial y}\right)dA, \qquad \oint_C (v\,dx + u\,dy) = \iint_R \left(\frac{\partial u}{\partial x} - \frac{\partial v}{\partial y}\right)dA$$

$f$ が正則なのでコーシー・リーマン方程式（上で証明済み）$\dfrac{\partial u}{\partial x}=\dfrac{\partial v}{\partial y}$、$\dfrac{\partial u}{\partial y}=-\dfrac{\partial v}{\partial x}$ が成り立ち、これを代入すると両方の被積分関数がゼロになります。よって $\oint_C f\,dz = 0$。$\blacksquare$

（この証明はグリーンの定理を使うため $u,v$ の偏導関数の連続性を仮定していますが、実際にはこの仮定なしでも成り立つことが知られています。この一般の場合の証明はグルサの定理と呼ばれ、三角形分割による別のアプローチが必要になるため、完全な証明は参考文献に譲ります。）

特異点を囲む場合は、次の**留数定理**が成り立ちます。

$$\oint_C f(z)\,dz = 2\pi i \sum_k \mathrm{Res}(f, z_k)$$

$z_k$ は $C$ の内側の特異点、$\mathrm{Res}$ は留数（特異点近傍での $f$ の振る舞いを表す量）です。留数定理は、$f$ を特異点のまわりでローラン級数展開し、コーシーの積分定理を特異点を除いた領域に適用することで証明されます（ローラン級数の詳細な扱いが必要なため、完全な証明は参考文献に譲ります）。この定理を使うと、実数の範囲では手強い積分が複素関数の理論で計算できます。

**参考文献**：Ahlfors, L. V. (1979). *Complex Analysis* (3rd ed.). McGraw-Hill.（グルサの定理・ローラン級数・留数定理の完全な証明を含む）

---

## 応用

- 流体力学（水や空気の流れ）
- 電気工学（交流回路の解析）
- 信号処理

複素解析は理論的な美しさだけでなく、工学の実践でも欠かせない道具です。

---

## まとめ

複素関数は複素数を入力・出力とする関数で、正則性（どの方向から近づいても同じ微分係数を持つ）という強い条件のもとで、コーシー・リーマン方程式が成り立つことを証明できます。この方程式とグリーンの定理を組み合わせるとコーシーの積分定理が証明でき、これを特異点のまわりに拡張したものが留数定理です。これらは実数の解析学にはない豊かな理論を形作ります。

---

## 関連ページ

- [リーマン積分](riemann-integral.md)
