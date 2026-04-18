---
title: 直線
description: "射影幾何・デザルグの定理・双対性"
goal: "射影平面の構造と双対原理を理解し、デザルグの定理を説明できるようになる"
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
  - title: 直線（標準）
    path: /math/geometry/line/standard.md
  - title: 行列（専門）
    path: /math/linear-algebra/matrices/professional.md
---

## 射影平面

ユークリッド平面では「平行な2直線は交わらない」ですが、**射影幾何**ではこの制約を取り除きます。

ユークリッド平面に無限遠点の集合（無限遠直線）を加えた空間 $\mathbb{P}^2$（射影平面）では、**任意の2直線はちょうど1点で交わります**（平行な直線は無限遠点で交わる）。

**同次座標**：ユークリッド平面の点 $(x, y)$ を $[x : y : 1]$ と表します。スカラー倍は同一視：$[x:y:z] = [\lambda x : \lambda y : \lambda z]$（$\lambda \neq 0$）。無限遠点は $z = 0$ の点。

直線 $ax + by + c = 0$ は点 $[a : b : c]$（双対）として表せます。

---

## 双対原理

$\mathbb{P}^2$ では「点」と「直線」を入れ替えても定理が成り立ちます。

| 元の命題 | 双対命題 |
|----------|---------|
| 2点がただ1直線を決定する | 2直線がただ1点を決定する |
| 3点が共線（1直線上にある） | 3直線が共点（1点を通る） |

---

## デザルグの定理

**定理**：2つの三角形 $ABC$ と $A'B'C'$ が透視対応（$AA'$、$BB'$、$CC'$ が1点 $O$ で交わる）ならば、対応する辺の延長線上の交点 $P = BC \cap B'C'$、$Q = CA \cap C'A'$、$R = AB \cap A'B'$ は同一直線（デザルグ軸）上にある。逆も成立。

この定理は射影幾何の根本定理の一つです。$\mathbb{P}^3$ では組み合わせ論的に証明でき、$\mathbb{P}^2$ での成立は公理として採用されることもあります。

---

## 交比

直線上の4点 $A, B, C, D$ の**交比**：

$$(A,B;C,D) = \frac{AC \cdot BD}{BC \cdot AD}$$

交比は射影変換の下で不変（射影幾何の基本的な不変量）です。

**参考文献**：Coxeter, H. S. M. (1993). *The Real Projective Plane* (3rd ed.). Springer.

---

## 関連ページ

- [直線（標準）](standard.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
