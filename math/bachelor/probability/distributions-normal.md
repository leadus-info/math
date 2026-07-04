---
title: 正規分布
description: "左右対称の釣り鐘型の分布"
goal: "正規分布の定義・標準化・68-95-99.7則を理解し使えるようになる"
tags: [math, probability, distributions]
stage: 発展編
subject: 確率
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 発展編
    path: /math/bachelor/index.md
  - title: 正規分布
    path: /math/bachelor/probability/distributions-normal.md
requires:
  - title: ポアソン分布
    path: distributions-poisson.md
  - title: 正規分布
    path: /math/advanced/probability/normal-distribution.md
---

## $N(\mu, \sigma^2)$

身長・テストの点数・測定誤差——自然界や社会の多くの量が従う、左右対称の釣り鐘型の分布です。

$$f(x) = \frac{1}{\sqrt{2\pi}\sigma} \exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right), \qquad E[X] = \mu, \quad \mathrm{Var}(X) = \sigma^2$$

**標準化**：$Z = \dfrac{X - \mu}{\sigma} \sim N(0, 1)$

**68-95-99.7則**：$\mu \pm \sigma$ に約68%、$\mu \pm 2\sigma$ に約95%、$\mu \pm 3\sigma$ に約99.7%のデータが入ります。「偏差値」はこの分布を使って計算されています。

---

## まとめ

正規分布は多くの自然・社会現象が従う釣り鐘型の分布で、標準化により平均0・分散1の分布に変換でき、68-95-99.7則でデータの分布範囲を見積もれます。

---

## 関連ページ

- [ポアソン分布（発展編）](distributions-poisson.md)
- [指数分布（発展編）](distributions-exponential.md)
- [統計（発展編）](statistics.md)
