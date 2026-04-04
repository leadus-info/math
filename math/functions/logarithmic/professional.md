---
title: 対数関数
description: "情報エントロピー・複素対数・$p$-進対数"
tags: [math,functions,logarithmic]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 対数関数
    href: /math/functions/logarithmic/professional.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
    url: standard.html
  - level: professional
level: professional
requires:
  - title: 対数関数
    url: \1/introduction.md
  - title: 複素数
    url: \1/introduction.md
  - title: 確率
    url: \1/introduction.md
---










# 対数関数（発展）
情報理論・複素対数・$p$-進対数を扱います。

## このページで扱うこと
- 情報エントロピーと対数
- 複素対数（多価性とリーマン面）
- KL ダイバージェンス

---

## 情報エントロピー

$$H(X) = -\sum_x p(x)\log_2 p(x)$$

不確実性の定量的な尺度。対数の底を変えることで単位が変わります（ビット、ナット）。

---

## 複素対数

$$\ln z = \ln|z| + i\arg(z)$$

$\arg(z)$ は $2\pi$ の不定性を持つため多価関数。  
主値を選ぶと（$-\pi < \arg \leq \pi$）単価になります。

---

## KL ダイバージェンス

$$D_{KL}(P \| Q) = \sum_x P(x)\ln\frac{P(x)}{Q(x)} \geq 0$$

確率分布間の「距離」（非対称）。

---

## 関連ページ

- [対数関数](introduction.md)
- [複素関数](introduction.md)
- [確率（専門）](../../statistics/probability/professional.md)
