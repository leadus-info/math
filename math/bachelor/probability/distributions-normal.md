---
title: 正規分布
description: "左右対称の釣り鐘型の分布"
goal: "正規分布の定義・標準化・68-95-99.7則を理解し、中心極限定理により正規分布が幅広い現象に現れる理由を説明できるようになる"
tags: [math, probability, distributions]
stage: 発展編
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

$$f(x) = \frac{1}{\sqrt{2\pi}\sigma} \exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right), \qquad E[X] = \mu, \quad \mathrm{Var}(X) = \sigma^2$$

**標準化**：$Z = \dfrac{X - \mu}{\sigma} \sim N(0, 1)$

**68-95-99.7則**：$\mu \pm \sigma$ に約68%、$\mu \pm 2\sigma$ に約95%、$\mu \pm 3\sigma$ に約99.7%のデータが入ります。「偏差値」はこの分布を使って計算されています。

---

## 中心極限定理

なぜ身長や測定誤差のように、由来のまったく異なる量が同じ釣り鐘型の分布に従うのでしょうか。その答えが**中心極限定理**です。

**定理**：$X_1, X_2, \ldots, X_n$ を、平均 $\mu$・分散 $\sigma^2$（有限）を持つ同一分布に従う独立な確率変数とする。このとき、標本平均 $\bar{X}_n = \dfrac{1}{n}\sum_{i=1}^n X_i$ を標準化した

$$Z_n = \frac{\bar{X}_n - \mu}{\sigma/\sqrt{n}}$$

は、$n \to \infty$ のとき分布として標準正規分布 $N(0,1)$ に収束する。

重要なのは、**もとの確率変数 $X_i$ 自身がどんな分布に従っていてもよい**という点です（正規分布はおろか、離散分布でも構いません）。多数の独立な要因の和・平均として現れる量が正規分布に近づくのはこのためで、二項分布 $B(n,p)$（応用編で見た正規分布近似）はベルヌーイ分布に従う $X_i$ の和という特別な場合にあたります。

**参考文献**：Feller, W. (1968). *An Introduction to Probability Theory and Its Applications*, Vol. 1 (3rd ed.). Wiley.

---

## まとめ

正規分布は多くの自然・社会現象が従う釣り鐘型の分布で、標準化により平均0・分散1の分布に変換でき、68-95-99.7則でデータの分布範囲を見積もれます。中心極限定理により、もとの分布によらず独立な確率変数の平均が正規分布に近づくことが保証され、これが正規分布が幅広い場面に現れる理論的な根拠になっています。

---

## 関連ページ

- [指数分布（発展編）](distributions-exponential.md)
- [統計（発展編）](statistics.md)
