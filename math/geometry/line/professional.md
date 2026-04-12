---
title: 直線
description: "射影空間・デザルグ定理・射影幾何"
tags: [math,geometry,line]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 直線
    path: /math/geometry/line/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 直線
    path: /math/geometry/line/introduction.md
  - title: ベクトル
    path: /math/linear-algebra/vectors/introduction.md
  - title: 集合
    path: /math/math-language/sets/introduction.md
---

## アフィン幾何における直線

ユークリッド幾何では「平行な2直線は交わらない」が基本ですが、\
**射影幾何**ではこの制約を取り除きます。

平面に「無限遠点」の集合（無限遠直線）を加えた空間 $\mathbb{P}^2$（射影平面）では、\
**2直線は必ずただ1点で交わります**（平行な直線は無限遠点で交わる）。

---

## 射影空間と同次座標

ユークリッド平面の点 $(x, y)$ を射影平面では $(x : y : 1)$（**同次座標**）で表します。\
スカラー倍は同一視：$(x : y : z) = (\lambda x : \lambda y : \lambda z)$（$\lambda \neq 0$）。

無限遠点は $z = 0$ の点：$(x : y : 0)$。

直線 $ax + by + c = 0$ は射影平面でも $(a : b : c)$ という点（双対）で表せます。

---

## 双対原理

$\mathbb{P}^2$ では「点」と「直線」を入れ替えても定理が成り立ちます。

| 元の命題 | 双対命題 |
|----------|---------|
| 2点がただ1直線を決定する | 2直線がただ1点を決定する |
| 3点が1直線上にある（共線） | 3直線が1点を通る（共点） |

---

## デザルグの定理

**定理**：2つの三角形 $ABC$ と $A'B'C'$ が透視対応（$AA'$、$BB'$、$CC'$ が1点 $O$ で交わる）であるとき、\
対応する辺の延長線上の交点 $P = BC \cap B'C'$、$Q = CA \cap C'A'$、$R = AB \cap A'B'$ は同一直線上にある。

この定理は射影幾何の根本定理の一つです。逆も成立します。

---

## 調和共役と交比

直線上の4点 $A, B, C, D$ の**交比**：

$$(A, B; C, D) = \frac{AC \cdot BD}{BC \cdot AD} \quad \text{（符号付き比）}$$

交比 $= -1$ のとき $C$ と $D$ は調和共役といいます。

交比は射影変換で不変（射影幾何の基本的な不変量）。

**参考文献**：Coxeter, H. S. M. (1993). *The Real Projective Plane* (3rd ed.). Springer.

---

## 関連ページ

- [直線](standard.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
