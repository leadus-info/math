---
title: 正規分布
description: "左右対称の釣り鐘型をした正規分布について、ガウス積分の証明から期待値μ・分散σ²を導出し、標準化・68-95-99.7則を扱い、中心極限定理により正規分布が幅広い現象に現れる理由を解説する"
goal: "ガウス積分を証明して正規分布の期待値・分散を導出し、標準化・68-95-99.7則を理解し、中心極限定理により正規分布が幅広い現象に現れる理由を説明できるようになる"
tags: [math, probability, distributions]
stage: bachelor
subject: 確率
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 正規分布
    path: distributions-normal.md
requires:
  - title: ポアソン分布
    path: distributions-poisson.md
  - title: 正規分布
    path: ../../advanced/probability/normal-distribution.md
---

## $N(\mu, \sigma^2)$

身長・テストの点数・測定誤差——自然界や社会の多くの量が従う、左右対称の釣り鐘型の分布です。

$$f(x) = \frac{1}{\sqrt{2\pi}\sigma} \exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right)$$

**補題（ガウス積分）**：$\displaystyle\int_{-\infty}^{\infty} e^{-u^2/2}\,du = \sqrt{2\pi}$

**証明**：$I = \displaystyle\int_{-\infty}^{\infty} e^{-u^2/2}\,du$ とおき、$I^2$ を2変数の積分とみて極座標に変換します。

$$I^2 = \int_{-\infty}^{\infty}\int_{-\infty}^{\infty} e^{-(u^2+v^2)/2}\,du\,dv = \int_0^{2\pi}\int_0^{\infty} e^{-r^2/2}\, r\,dr\,d\theta$$

（$u=r\cos\theta$、$v=r\sin\theta$、面積要素 $du\,dv = r\,dr\,d\theta$）。内側の積分は $s=r^2/2$ と置換すると $\int_0^\infty e^{-s}\,ds = 1$ となるので、$I^2 = 2\pi \times 1 = 2\pi$。$I>0$ なので $I=\sqrt{2\pi}$。$\blacksquare$

この補題より、$f(x)$ が確率密度関数の条件 $\int_{-\infty}^{\infty}f(x)\,dx=1$ を満たすことが確認できます（$u=(x-\mu)/\sigma$ と置換すれば $\int f(x)\,dx = \frac{1}{\sqrt{2\pi}}\int e^{-u^2/2}\,du = 1$）。

**命題**：$X \sim N(\mu,\sigma^2)$ のとき $E[X]=\mu$、$\mathrm{Var}(X)=\sigma^2$。

**証明**：$u=(x-\mu)/\sigma$ と置換すると、

$$E[X] = \int_{-\infty}^{\infty} x f(x)\,dx = \int_{-\infty}^{\infty} (\mu+\sigma u)\frac{1}{\sqrt{2\pi}}e^{-u^2/2}\,du = \mu\int_{-\infty}^{\infty}\frac{e^{-u^2/2}}{\sqrt{2\pi}}du + \sigma\int_{-\infty}^{\infty}\frac{u\,e^{-u^2/2}}{\sqrt{2\pi}}du$$

右辺第1項は $f$ が確率密度であることから $\mu\times 1=\mu$、第2項は奇関数 $u\,e^{-u^2/2}$ を対称区間で積分するので $0$。よって $E[X]=\mu$。

分散も同様に、

$$\mathrm{Var}(X) = \int_{-\infty}^{\infty}(x-\mu)^2 f(x)\,dx = \sigma^2\int_{-\infty}^{\infty} u^2 \frac{e^{-u^2/2}}{\sqrt{2\pi}}\,du$$

部分積分（$u\,du$ と $u\,e^{-u^2/2}\,du=-d(e^{-u^2/2})$ を使う）により $\int_{-\infty}^{\infty}u^2 e^{-u^2/2}du = \sqrt{2\pi}$ となることが示せるので、$\mathrm{Var}(X)=\sigma^2 \times 1 = \sigma^2$。$\blacksquare$

**標準化**：$Z = \dfrac{X - \mu}{\sigma} \sim N(0, 1)$

**68-95-99.7則**：$\mu \pm \sigma$ に約68%、$\mu \pm 2\sigma$ に約95%、$\mu \pm 3\sigma$ に約99.7%のデータが入ります。「偏差値」はこの分布を使って計算されています。

---

## 中心極限定理

なぜ身長や測定誤差のように、由来のまったく異なる量が同じ釣り鐘型の分布に従うのでしょうか。その答えが**中心極限定理**です。

**定理**：$X_1, X_2, \ldots, X_n$ を、平均 $\mu$・分散 $\sigma^2$（有限）を持つ同一分布に従う独立な確率変数とする。このとき、標本平均 $\bar{X}_n = \dfrac{1}{n}\sum_{i=1}^n X_i$ を標準化した

$$Z_n = \frac{\bar{X}_n - \mu}{\sigma/\sqrt{n}}$$

は、$n \to \infty$ のとき分布として標準正規分布 $N(0,1)$ に収束する。

重要なのは、**もとの確率変数 $X_i$ 自身がどんな分布に従っていてもよい**という点です（正規分布はおろか、離散分布でも構いません）。多数の独立な要因の和・平均として現れる量が正規分布に近づくのはこのためで、二項分布 $B(n,p)$（応用編で見た正規分布近似）はベルヌーイ分布に従う $X_i$ の和という特別な場合にあたります。

**証明の方針**：標準的な証明は特性関数 $\varphi_X(t) = E[e^{itX}]$（フーリエ変換の確率論版）を使います。独立な確率変数の和の特性関数は各特性関数の積になるという性質を使い、$Z_n$ の特性関数を計算してテイラー展開すると、$n\to\infty$ で標準正規分布の特性関数 $e^{-t^2/2}$ に各点収束することが示せます。特性関数の収束から分布の収束を導く手順（レヴィの連続性定理）まで含めた完全な証明は、測度論的な準備が必要なため参考文献に譲ります。

**参考文献**：Feller, W. (1968). *An Introduction to Probability Theory and Its Applications*, Vol. 1 (3rd ed.). Wiley.（中心極限定理の完全な証明を含む）

---

## まとめ

正規分布は多くの自然・社会現象が従う釣り鐘型の分布です。ガウス積分を極座標変換で計算することで密度関数が確率密度の条件を満たすことや、$E[X]=\mu$・$\mathrm{Var}(X)=\sigma^2$ が証明でき、標準化により平均0・分散1の分布に変換して68-95-99.7則でデータの分布範囲を見積もれます。中心極限定理により、もとの分布によらず独立な確率変数の平均が正規分布に近づくことが保証され、これが正規分布が幅広い場面に現れる理論的な根拠になっています。

---

## 関連ページ

- [指数分布（発展編）](distributions-exponential.md)
- [統計（発展編）](statistics.md)
