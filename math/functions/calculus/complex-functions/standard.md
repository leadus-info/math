---
title: 複素関数
description: "複素数を変数にとる関数"
difficulty: 3
tags: [math,complex-numbers,complex-functions]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数の操作
    href: /math/functions/calculus/index.html
  - text: 複素関数
    href: /math/functions/calculus/complex-functions/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 複素関数
実数の関数を複素数の世界に拡張したものが**複素関数**です。
「複素数で微分できる」という条件が、実数のときよりずっと強い制約を生み、
豊かな理論が展開されます。

## このページで扱うこと
- 複素関数の定義
- 正則性（複素微分できること）
- コーシー・リーマン方程式

## 前提知識
- [複素数](../../../numbers/complex-numbers/standard.md)
- [微分](../derivatives/standard.md)

---

## 複素関数とは？

複素数 $z$ を入力にとり、複素数を返す関数です。

$$f(z) = z^2, \quad f(z) = e^z, \quad f(z) = \frac{1}{z}$$

$z = x + iy$ とすると $f = u(x,y) + iv(x,y)$ という形になります。

---

## 正則性

実数の微分と同じ形の式で微分できるとき**正則**といいます。

$$f'(z) = \lim_{h \to 0} \frac{f(z+h) - f(z)}{h} \quad (h \in \mathbb{C})$$

実数の微分と違う点：$h$ がどの方向から $0$ に近づいても同じ値になることを要求します。
この条件が強いため、正則関数は非常に良い性質を持ちます。

---

## コーシー・リーマン方程式

$f = u + iv$ が正則であるための必要十分条件：

$$\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}, \qquad \frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x}$$

これを満たすとき $u$ と $v$ は**調和関数**（$\Delta u = 0$）になります。

---

## コーシーの積分定理

正則な $f$ を閉じた曲線 $C$ に沿って積分すると $0$ になります。

$$\oint_C f(z)\,dz = 0$$

これは実数の積分にはない、複素関数特有の性質です。

---

## 留数定理

特異点（$f$ が正則でない点）を持つ場合でも積分が計算できます。

$$\oint_C f(z)\,dz = 2\pi i \sum_k \text{Res}(f, z_k)$$

これを使って、実数の難しい積分（$\int_{-\infty}^{\infty}$ など）が計算できます。

---

## 関連ページ

- [複素数](../../../numbers/complex-numbers/standard.md)
- [複素関数（発展）](../complex-functions/advanced.md) — より詳しく学ぶ
