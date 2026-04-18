---
title: 対数関数
description: "情報エントロピー・複素対数・$p$-進対数"
goal: "対数関数を厳密に定義し、主要な定理を証明できるようになる"
tags: [math,functions,logarithmic]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/analysis/index.md
  - title: 対数関数
    path: /math/specific-functions/logarithmic/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 対数関数
    path: /math/specific-functions/logarithmic/introduction.md
  - title: 複素数
    path: /math/numbers/complex-numbers/introduction.md
  - title: 確率
    path: /math/probability/probability/introduction.md
---

## 複素対数

実数では $\ln x$（$x > 0$）は一価関数でしたが、複素数に拡張すると多価になります。

$$\log z = \ln|z| + i\arg(z)$$

$\arg(z)$ は $2\pi$ の不定性があるため**多価関数**です。$-\pi < \arg(z) \leq \pi$（主値）を選ぶと、主値対数 $\mathrm{Log}\,z$ として一価になります。

リーマン面を使うと多価性を一価に「解きほぐす」ことができます。

---

## 情報エントロピー

離散確率分布 $\{p_i\}$ の**シャノン情報量（エントロピー）**：

$$H = -\sum_i p_i \log_2 p_i$$

対数の底を変えると単位が変わります（ビット：底2、ナット：底$e$）。

---

## KL ダイバージェンス

分布 $P$ と $Q$ の「ずれ」の非対称な尺度：

$$D_{KL}(P \| Q) = \sum_x P(x)\ln\frac{P(x)}{Q(x)} \geq 0$$

等号は $P = Q$ のとき。距離の公理を満たしません（非対称・三角不等式不成立）。

---

## 参考文献

Rudin, W. (1987). *Real and Complex Analysis* (3rd ed.). McGraw-Hill.

---

## 関連ページ

- [対数関数（標準）](standard.md)
- [複素関数（専門）](../../analysis/complex-analysis/professional.md)
