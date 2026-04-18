---
title: 複素関数
description: "リーマン面・解析接続・モジュラー形式"
goal: "複素関数を厳密に定義し、主要な定理を証明できるようになる"
tags: [math,complex-numbers,complex-functions]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 解析
    path: /math/analysis/index.md
  - title: 複素関数
    path: /math/analysis/complex-analysis/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 複素関数
    path: /math/analysis/complex-analysis/introduction.md
  - title: 対数関数（専門）
    path: ../../logarithmic/professional.md
  - title: 点（専門）
    path: ../../../geometry/point/professional.md
---

## リーマン面

多価関数（$\log z$、$\sqrt{z}$ など）を一価関数として扱うための「複数枚重なった面」が**リーマン面**です。

$\log z = \ln|z| + i\arg(z)$ は $\arg(z)$ が $2\pi$ の不定性を持つため多価。$\log z$ のリーマン面は無限枚のシートが階段状にらせんをなす構造です。

---

## 解析接続

$f$ が領域 $D$ で正則なとき、より大きな領域 $D' \supset D$ への正則な拡張がただ一つ存在することがあります（**一意性定理**）。

**例**：$\zeta(s) = \sum_{n=1}^\infty n^{-s}$（$\mathrm{Re}(s) > 1$ で定義）をリーマンゼータ関数として全複素平面（$s = 1$ を除く）に解析接続できます。

---

## モノドロミー

解析接続して閉曲線を一周したとき、関数値がどう変化するかを追跡する群論的構造です。$\log z$ を原点を囲む閉曲線に沿って解析接続すると $2\pi i$ だけずれます。

---

## モジュラー形式

上半平面 $\mathbb{H} = \{z : \mathrm{Im}(z) > 0\}$ 上の正則関数で、

$$f\left(\frac{az+b}{cz+d}\right) = (cz+d)^k f(z) \quad \left(\begin{pmatrix}a&b\\c&d\end{pmatrix} \in SL(2,\mathbb{Z})\right)$$

を満たすものが**重さ $k$ のモジュラー形式**。谷山・志村予想（ワイルズによる証明）を通じてフェルマーの最終定理の証明に使われました。

**参考文献**：Ahlfors, L. V. (1979). *Complex Analysis* (3rd ed.). McGraw-Hill.

---

## 関連ページ

- [複素関数（標準）](standard.md)
- [対数関数（専門）](../../specific-functions/logarithmic/professional.md)
