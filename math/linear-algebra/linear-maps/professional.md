---
title: 線形写像
description: "線形写像の圏・双対写像・テンソル積"
goal: "線形写像のなす圏の構造を理解し、双対写像の定義とテンソル積との関係を説明できるようになる"
tags: [math,linear-algebra,linear-maps]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 線形代数
    path: /math/linear-algebra/index.md
  - title: 線形写像
    path: /math/linear-algebra/linear-maps/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 線形写像（標準）
    path: /math/linear-algebra/linear-maps/standard.md
  - title: ベクトル（専門）
    path: /math/linear-algebra/vectors/professional.md
  - title: 抽象代数（標準）
    path: /math/algebra/abstract/standard.md
---

## 線形写像のなす圏

体 $F$ 上のベクトル空間と線形写像は**圏**（category）を形成します。

- **対象**：$F$ 上のベクトル空間
- **射**：線形写像
- **合成**：写像の合成（結合律・単位元を満たす）

$\mathrm{Hom}_F(V, W) = \{T: V \to W : T \text{ は線形}\}$ 自身が $F$ 上のベクトル空間になります。

$$\dim \mathrm{Hom}_F(V, W) = (\dim V)(\dim W)$$

---

## 双対写像

$T: V \to W$ に対して**双対写像** $T^*: W^* \to V^*$（$V^*$, $W^*$ は双対空間）を：

$$T^*(f) = f \circ T \quad (f \in W^*)$$

で定義します。

**性質**：
- $(S \circ T)^* = T^* \circ S^*$（順序が逆転）
- $T$ が単射 $\iff$ $T^*$ が全射
- $T$ が全射 $\iff$ $T^*$ が単射
- 有限次元では $(T^*)^{**} \cong T$（自然な同型）

有限次元では双対写像の表現行列は $T$ の表現行列の転置 $A^\top$ です。

---

## 線形写像のテンソル積

$T: V \to V'$ と $S: W \to W'$ に対して**テンソル積写像**：

$$T \otimes S: V \otimes W \to V' \otimes W'$$

$$（T \otimes S)(v \otimes w) = T(v) \otimes S(w)$$

これは普遍性から一意に定まります。表現行列はクロネッカー積 $A \otimes B$ です。

---

## 固有多項式と最小多項式

$T: V \to V$（有限次元）に対して：

**固有多項式**：$p_T(\lambda) = \det(\lambda I - A)$（$n$ 次多項式）

**最小多項式** $m_T(\lambda)$：$m_T(T) = 0$ を満たす最小次数のモニック多項式

**ケーリー＝ハミルトンの定理**：$p_T(T) = 0$（固有多項式は $T$ を零化する）

最小多項式は固有多項式を割り切り、同じ根（ただし重複度は最小多項式の方が小さくなりうる）を持ちます。

**参考文献**：Lang, S. (1987). *Linear Algebra* (3rd ed.). Springer.

---

## 関連ページ

- [線形写像（標準）](standard.md)
- [ベクトル（専門）](../vectors/professional.md)
- [行列（専門）](../matrices/professional.md)
- [固有値（専門）](../eigenvalues/professional.md)
