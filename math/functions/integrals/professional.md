---
title: 積分
description: "ルベーグ積分・広義積分・多重積分"
goal: "積分を厳密に定義し、主要な定理を証明できるようになる"
tags: [math,operations,integrals]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数の操作
    path: /math/functions/index.md
  - title: 積分
    path: /math/functions/integrals/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 積分
    path: /math/functions/integrals/introduction.md
  - title: 微分（専門）
    path: ../derivatives/professional.md
  - title: 集合（専門）
    path: ../../../math-language/sets/professional.md
---

## リーマン積分の定義

区間 $[a,b]$ の分割 $P: a = x_0 < x_1 < \cdots < x_n = b$ に対して、

$$S(f, P) = \sum_{k=1}^n f(t_k)(x_k - x_{k-1}) \quad (t_k \in [x_k, x_{k-1}])$$

$\|P\| = \max_k(x_k - x_{k-1}) \to 0$ のとき $S(f, P)$ が一定値に収束するとき $f$ は**リーマン積分可能**といいます。

---

## ルベーグ積分

リーマン積分は「縦に切る」発想。ルベーグ積分は「横に切る」発想：

$$\int f\,d\mu = \int_0^\infty \mu(\{x: f(x) > t\})\,dt$$

**優収束定理**：$|f_n| \leq g$（$g$ 積分可能）かつ $f_n \to f$ 各点収束なら $\int f_n\,d\mu \to \int f\,d\mu$。

これはリーマン積分では成立しない強力な性質です。

---

## フビニの定理

$$\int_{A \times B} f(x,y)\,d(x,y) = \int_A\left(\int_B f(x,y)\,dy\right)dx$$

（$f$ が可測かつ非負、または絶対値が積分可能なとき）

---

## 変数変換公式

$\phi: U \to V$ が微分同相のとき：

$$\int_V f(y)\,dy = \int_U f(\phi(x))|\det J\phi(x)|\,dx$$

**例（極座標）**：$\iint f(x,y)\,dxdy = \iint f(r\cos\theta, r\sin\theta)\,r\,dr\,d\theta$

---

## ストークスの定理（一般形）

$$\int_{\partial M}\omega = \int_M d\omega$$

グリーンの定理・発散定理・古典的ストークスの定理を統一します。

**参考文献**：Royden, H. L. & Fitzpatrick, P. M. (2010). *Real Analysis* (4th ed.). Prentice Hall.

---

## 関連ページ

- [積分（標準）](standard.md)
- [微分（専門）](../derivatives/professional.md)
