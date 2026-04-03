---
title: 対数関数（専門）
description: "情報エントロピー・複素対数・$p$-進対数"
difficulty: 5
tags: [math,functions,logarithmic,professional]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 対数関数（専門）
    href: /math/functions/logarithmic/professional.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
    href: advanced.html
  - text: 専門
---








# 対数関数（発展）
情報理論・複素対数・$p$-進対数を扱います。

## このページで扱うこと
- 情報エントロピーと対数
- 複素対数（多価性とリーマン面）
- KL ダイバージェンス

## 前提知識
- [対数関数](../logarithmic/standard.md)
- [複素数](../../numbers/complex-numbers/standard.md)
- [確率](../../statistics/probability/standard.md)

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

- [対数関数](../logarithmic/standard.md)
- [複素関数](../calculus/complex-functions/standard.md)
- [確率（専門）](../../statistics/probability/professional.md)
