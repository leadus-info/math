---
title: 複素関数
description: "複素数を変数にとる関数"
goal: "複素関数の定義・主要な定理・代表的な計算を理解し、後続のトピックに進める基礎を身につける"
tags: [math,complex-numbers,complex-functions]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数の操作
    path: /math/analysis/index.md
  - title: 複素関数
    path: /math/analysis/complex-analysis/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 複素数
    path: /math/numbers/complex-numbers/introduction.md
  - title: 微分
    path: /math/analysis/derivatives/introduction.md
  - title: 積分
    path: /math/analysis/integrals/introduction.md
---

## 複素関数とは

$f: \mathbb{C} \to \mathbb{C}$ の形、つまり複素数を入れて複素数が出る関数を**複素関数**といいます。

$z = x + iy$ とおくと $f(z) = u(x,y) + iv(x,y)$ と書け、実部 $u$ と虚部 $v$ はそれぞれ2変数実関数です。

**例**：$e^z = e^x(\cos y + i\sin y)$（オイラーの公式の拡張）

---

## 正則性

**定義**：$f(z)$ が $z_0$ で**正則（holomorphic）**とは、

$$f'(z_0) = \lim_{h \to 0} \frac{f(z_0+h) - f(z_0)}{h} \quad (h \in \mathbb{C})$$

が存在すること。$h$ がどの方向の複素数でも同じ値に収束する必要があります。

これは実数の微分可能性より強い条件です。

---

## コーシー・リーマン方程式

$f = u + iv$ が正則であるための必要十分条件：

$$\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}, \qquad \frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x}$$

---

## コーシーの積分定理

$f$ が正則なら、閉曲線 $C$ に沿った積分はゼロ：

$$\oint_C f(z)\,dz = 0$$

---

## 留数定理

$$\oint_C f(z)\,dz = 2\pi i \sum_k \mathrm{Res}(f, z_k)$$

$z_k$ は $C$ の内側の特異点、$\mathrm{Res}$ は留数（特異点近傍での振る舞いを表す量）。

この定理を使うと、実数の難しい積分が複素関数の理論で計算できます。

---

## 関連ページ

- [複素関数（入門）](introduction.md)
- [複素数（標準）](../../numbers/complex-numbers/standard.md)
