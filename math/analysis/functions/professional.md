---
title: 関数
description: "関数空間・連続性・一様連続・リプシッツ条件"
goal: "位相空間上の連続写像の定義・一様連続とリプシッツ条件の関係・関数空間のノルムを説明できるようになる"
tags: [math,analysis,functions]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 解析
    path: /math/analysis/index.md
  - title: 関数
    path: /math/analysis/functions/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 関数（標準）
    path: /math/analysis/functions/standard.md
  - title: 極限（専門）
    path: /math/analysis/limits/professional.md
  - title: 集合（専門）
    path: /math/foundations/sets/professional.md
---

## 位相空間上の連続写像

位相空間 $(X, \mathcal{T}_X)$ から $(Y, \mathcal{T}_Y)$ への写像 $f$ が**連続**であるとは、任意の開集合 $V \in \mathcal{T}_Y$ に対して $f^{-1}(V) \in \mathcal{T}_X$ が成り立つことです。

距離空間では $\varepsilon$-$\delta$ による定義と一致します：\
任意の $\varepsilon > 0$ に対して $\delta > 0$ が存在し、$d_X(x, x_0) < \delta \Rightarrow d_Y(f(x), f(x_0)) < \varepsilon$。

---

## 一様連続

$f: X \to Y$ が**一様連続**であるとは、任意の $\varepsilon > 0$ に対して $\delta > 0$ が存在して、

$$d_X(x, y) < \delta \Rightarrow d_Y(f(x), f(y)) < \varepsilon \quad (\forall x, y \in X)$$

通常の連続と違い、$\delta$ が $x_0$ に依存せず一様に選べます。

**定理**：コンパクト距離空間上の連続関数は一様連続（ハイネ＝カントールの定理）。

**例**：$f(x) = x^2$ は $\mathbb{R}$ 上で連続だが一様連続でない。$[0, 1]$ 上では一様連続。

---

## リプシッツ条件

$f: X \to Y$ が**リプシッツ連続**であるとは、定数 $L > 0$ が存在して

$$d_Y(f(x), f(y)) \leq L \cdot d_X(x, y) \quad (\forall x, y \in X)$$

$L$ を**リプシッツ定数**といいます。

包含関係：リプシッツ連続 $\subset$ 一様連続 $\subset$ 連続。

微分可能で導関数が有界な関数はリプシッツ連続（平均値定理より）。

---

## 関数空間

$C([a,b])$：$[a,b]$ 上の連続関数全体のなす線形空間。

**上限ノルム**（一様ノルム）：$\|f\|_\infty = \sup_{x \in [a,b]} |f(x)|$

$(C([a,b]), \|\cdot\|_\infty)$ は完備（バナッハ空間）です。これはコーシー列の収束が一様収束に対応することから従います。

**$L^p$ ノルム**（$1 \leq p < \infty$）：$\|f\|_p = \left(\int_a^b |f(x)|^p dx\right)^{1/p}$

$L^2([a,b])$ は内積 $\langle f, g \rangle = \int_a^b f(x)g(x) dx$ を持つヒルベルト空間です。

**参考文献**：Rudin, W. (1976). *Principles of Mathematical Analysis* (3rd ed.). McGraw-Hill.

---

## 関連ページ

- [極限（専門）](../limits/professional.md)
- [積分（専門）](../integrals/professional.md)
- [ベクトル（専門）](../../linear-algebra/vectors/professional.md)
