---
title: 位相幾何学
description: "位相空間・連続写像・基本的な位相的概念"
goal: "位相空間の定義・開集合・連続写像・コンパクト性・連結性の概念を理解し、基本的な例で確認できるようになる"
tags: [math,geometry,topology]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 位相幾何学
    path: /math/geometry/topology/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 位相幾何学（入門）
    path: /math/geometry/topology/introduction.md
  - title: 集合（標準）
    path: /math/foundations/sets/standard.md
  - title: 点（専門）
    path: /math/geometry/coordinate/point/professional.md
---

## 位相空間

**定義**：集合 $X$ と開集合族 $\mathcal{T} \subseteq 2^X$ の組 $(X, \mathcal{T})$ が**位相空間**であるとは：

1. $\emptyset, X \in \mathcal{T}$
2. 有限個の開集合の共通部分は開集合
3. 任意個の開集合の合併は開集合

**例**：
- 距離空間では開球 $B_r(x)$ から生成される位相（距離位相）
- 離散位相：$\mathcal{T} = 2^X$（すべての部分集合が開集合）
- 密着位相：$\mathcal{T} = \{\emptyset, X\}$

---

## 連続写像と同相

$(X, \mathcal{T}_X)$ から $(Y, \mathcal{T}_Y)$ への写像 $f$ が**連続**：任意の開集合 $V \in \mathcal{T}_Y$ に対して $f^{-1}(V) \in \mathcal{T}_X$。

全単射で $f$ も $f^{-1}$ も連続な写像を**同相写像**（homeomorphism）といい、$X \cong Y$（$X$ と $Y$ は**同相**）と書きます。

同相な空間は位相的に「同じ」です。コーヒーカップとドーナツは同相です。

---

## コンパクト性

$(X, \mathcal{T})$ が**コンパクト**であるとは：$X$ の任意の開被覆が有限部分被覆を持つこと。

$$X = \bigcup_{\alpha} U_\alpha \implies \exists \text{ 有限部分集合 } X = U_{\alpha_1} \cup \cdots \cup U_{\alpha_n}$$

**例**：$[0, 1]$（閉区間）はコンパクト。$(0, 1)$（開区間）はコンパクトでない。

**ハイネ＝ボレルの定理**：$\mathbb{R}^n$ の部分集合はコンパクト $\iff$ 有界かつ閉集合。

コンパクト空間上の連続関数は最大値・最小値を持ちます（最大値定理）。

---

## 連結性

$(X, \mathcal{T})$ が**連結**であるとは：$X$ が2つの空でない互いに素な開集合の合併に表せないこと。

**弧状連結**：任意の2点を結ぶ連続曲線が存在する。弧状連結 $\Rightarrow$ 連結（逆は一般に不成立）。

**中間値定理**（連結性から）：$f: X \to \mathbb{R}$ が連続、$X$ が連結、$f(a) < c < f(b)$ ならば $f(p) = c$ となる $p$ が存在します。

---

## ハウスドルフ空間

$(X, \mathcal{T})$ が**ハウスドルフ**であるとは：任意の相異なる2点 $x, y$ に対して、互いに素な開近傍が存在すること。

距離空間はすべてハウスドルフ。ハウスドルフ空間ではコンパクト集合は閉集合。

---

## 関連ページ

- [点（専門）](../coordinate/point/professional.md)
- [集合（専門）](../../foundations/sets/professional.md)
- [位相幾何学（専門）](professional.md)
