---
title: ベクトル
description: "内積空間・ヒルベルト空間・双対空間"
goal: "内積空間の公理とグラム＝シュミット直交化を理解し、ヒルベルト空間とリース表現定理の内容を説明できるようになる"
tags: [math,linear-algebra,vectors]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 線形代数
    path: /math/linear-algebra/index.md
  - title: ベクトル
    path: /math/linear-algebra/vectors/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: ベクトル（標準）
    path: /math/linear-algebra/vectors/standard.md
  - title: 行列（専門）
    path: /math/linear-algebra/matrices/professional.md
  - title: 極限（専門）
    path: /math/analysis/limits/professional.md
---

## 内積空間

**定義**：体 $\mathbb{F}$（$\mathbb{R}$ または $\mathbb{C}$）上のベクトル空間 $V$ が**内積空間**であるとは、内積 $\langle \cdot, \cdot \rangle: V \times V \to \mathbb{F}$ が存在して以下を満たすことです。

1. 線形性：$\langle \alpha u + v, w \rangle = \alpha \langle u, w \rangle + \langle v, w \rangle$
2. 共役対称性：$\langle u, v \rangle = \overline{\langle v, u \rangle}$
3. 正定値性：$\langle v, v \rangle \geq 0$（等号は $v = 0$ のとき）

**コーシー＝シュワルツ不等式**：$|\langle u, v \rangle| \leq \|u\| \|v\|$（等号は $u, v$ が比例するとき）

---

## グラム＝シュミット直交化

線形独立な $\{v_1, \ldots, v_n\}$ から正規直交基底を構成します。

$$u_1 = v_1, \quad u_k = v_k - \sum_{j=1}^{k-1} \frac{\langle v_k, e_j \rangle}{\|u_j\|^2} u_j, \quad e_k = \frac{u_k}{\|u_k\|}$$

これにより $\langle e_i, e_j \rangle = \delta_{ij}$（クロネッカーのデルタ）を満たす基底が得られます。

---

## ヒルベルト空間

**定義**：完備な内積空間を**ヒルベルト空間**といいます。「完備」とは任意のコーシー列が収束することです。

**例**：$L^2([0,1]) = \{f: [0,1] \to \mathbb{R} \mid \int_0^1 |f|^2 < \infty\}$（ルベーグ可積分関数の空間）

フーリエ級数はヒルベルト空間 $L^2$ での正規直交展開として理解できます。

---

## リース表現定理

**定理**：ヒルベルト空間 $H$ 上の有界線形汎関数 $f: H \to \mathbb{F}$ に対して、一意の $u \in H$ が存在して：

$$f(v) = \langle v, u \rangle \quad \forall v \in H$$

これは「有界線形汎関数はすべて内積で書ける」ことを意味し、$H$ とその双対空間 $H^*$ が等長同型であることを示します。

**参考文献**：Reed, M. & Simon, B. (1980). *Methods of Modern Mathematical Physics I: Functional Analysis*. Academic Press.

---

## 関連ページ

- [ベクトル（標準）](standard.md)
- [行列（専門）](../matrices/professional.md)
- [積分（専門）](../../analysis/integrals/professional.md)
