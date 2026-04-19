---
title: 固有値
description: "行列を掛けても方向が変わらないベクトル"
goal: "固有値・固有ベクトルの意味を直感的に理解し、対角化が何を意味するかを説明できるようになる"
tags: [math,linear-algebra,eigenvalues]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 線形代数
    path: /math/linear-algebra/index.md
  - title: 固有値
    path: /math/linear-algebra/eigenvalues/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 行列（入門）
    path: /math/linear-algebra/matrices/introduction.md
  - title: ベクトル（入門）
    path: /math/linear-algebra/vectors/introduction.md
---

## 方向が変わらないベクトル

行列を掛けると、普通はベクトルの方向が変わります。しかしある特別なベクトルは、行列を掛けても方向が変わらず、大きさだけが変わります。

$$A\boldsymbol{v} = \lambda \boldsymbol{v}$$

この $\boldsymbol{v}$ を**固有ベクトル**、$\lambda$ を対応する**固有値**といいます。

---

## 具体的なイメージ

鏡の変換（$y$ 軸に関する反射）を考えます。ほとんどのベクトルは方向が変わりますが、$x$ 軸方向 $(1, 0)$ は左右反転で $(-1, 0)$（$-1$ 倍）、$y$ 軸方向 $(0, 1)$ は変わらず $(0, 1)$（$1$ 倍）のままです。

- 固有ベクトル $(1, 0)$、固有値 $-1$
- 固有ベクトル $(0, 1)$、固有値 $1$

---

## なぜ重要か

固有値・固有ベクトルを知ると、行列を繰り返し掛ける計算が一気に簡単になります。

$A^{100}\boldsymbol{v}$ を直接計算するのは大変ですが、$\boldsymbol{v}$ が固有ベクトルなら：

$$A^{100}\boldsymbol{v} = \lambda^{100}\boldsymbol{v}$$

数を100乗するだけです。Google のページランクアルゴリズム、量子力学のエネルギー準位、主成分分析など、固有値は科学・工学の中心にあります。

---

## 関連ページ

- [行列（入門）](../matrices/introduction.md)
- [線形写像（入門）](../linear-maps/introduction.md)
