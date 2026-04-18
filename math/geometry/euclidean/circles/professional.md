---
title: 円
description: "反転・リーマン球面・メビウス変換"
goal: "円反転の性質・リーマン球面の構成・メビウス変換の群構造を説明できるようになる"
tags: [math,geometry,circle]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 円
    path: /math/geometry/euclidean/circles/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 円（標準）
    path: /math/geometry/euclidean/circles/standard.md
  - title: 複素関数（標準）
    path: /math/analysis/complex-analysis/standard.md
---

## 円反転

基準円 $|z| = r$（複素平面上）について、点 $z \neq 0$ の**反転像**：

$$z^* = \frac{r^2}{\bar{z}}$$

**性質**：
- 円と直線を円または直線に写す（「広義の円」を保存）
- 角度を保存する（共形写像）
- 基準円上の点は固定

反転は共形写像（角度を保つ変換）の一例であり、ポテンシャル論や電磁気学で有用です。

---

## リーマン球面

複素平面 $\mathbb{C}$ に無限遠点 $\infty$ を加えた $\hat{\mathbb{C}} = \mathbb{C} \cup \{\infty\}$ を**リーマン球面**（複素射影直線 $\mathbb{P}^1$）といいます。

$\hat{\mathbb{C}}$ と $S^2 = \{(x,y,z) \in \mathbb{R}^3 : x^2+y^2+z^2=1\}$ の対応は**立体射影**で与えられます：

$$z = \frac{x + iy}{1 - w} \quad (S^2 \ni (x,y,w) \mapsto z \in \hat{\mathbb{C}})$$

北極 $(0,0,1)$ が $\infty$ に対応します。

---

## メビウス変換

$$f(z) = \frac{az+b}{cz+d}, \quad ad - bc \neq 0 \quad (a,b,c,d \in \mathbb{C})$$

$\hat{\mathbb{C}}$ 上の全単射共形写像です。広義の円（円または直線）を広義の円に写します。

メビウス変換の全体は群をなし（$PSL(2,\mathbb{C}) \cong SL(2,\mathbb{C})/\{\pm I\}$）、3点を任意の3点に送る変換がちょうど1つ存在します。

**実係数**（$a,b,c,d \in \mathbb{R}$）のメビウス変換は上半平面 $\mathbb{H}$ を保存し、$PSL(2,\mathbb{R})$ として双曲幾何の等長変換群になります。

**参考文献**：Ahlfors, L. V. (1979). *Complex Analysis* (3rd ed.). McGraw-Hill.

---

## 関連ページ

- [円（標準）](standard.md)
- [複素関数（専門）](../../../analysis/complex-analysis/professional.md)
- [直線（専門）](../../coordinate/line/professional.md)
