---
title: 四角形
description: "双対多面体・四辺形の射影的性質"
tags: [math,geometry,quadrilateral]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 四角形
    path: /math/geometry/quadrilateral/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 四角形
    path: /math/geometry/quadrilateral/introduction.md
  - title: 円
    path: /math/geometry/circle/introduction.md
  - title: 直線（専門）
    path: ../line/professional.md
---

## 内接四辺形の性質

円に内接する四辺形（内接四辺形）には特別な性質があります。

**定理**：円に内接する四辺形の対角の和は $180°$。

**証明**：円周角の定理から、同じ弧に対する円周角は等しいため、\
対角 $\angle A$ と $\angle C$ を足すと中心角 $360°$ の半分 $= 180°$ になります。

---

## トレミーの定理

内接四辺形 $ABCD$ において：

$$AC \cdot BD = AB \cdot CD + AD \cdot BC$$

対角線の積は、向かい合う辺の積の和に等しい。

**証明の概略**：$BD$ 上に $\angle BAE = \angle CAD$ となる点 $E$ をとり、\
相似な三角形の関係から導きます。

---

## 四辺形の面積の一般公式

一般の四辺形（内接・外接でなくてよい）の面積は対角線を使って表せます。

対角線が $d_1$、$d_2$、交角が $\theta$ のとき：

$$S = \frac{1}{2} d_1 d_2 \sin\theta$$

ひし形は $\theta = 90°$ の特別な場合（$S = \frac{d_1 d_2}{2}$）。

---

## ブレーシュナイダーの公式

辺の長さ $a, b, c, d$ と対角の和の半分 $s = \frac{a+b+c+d}{2}$ を使った一般四辺形の面積：

$$S = \sqrt{(s-a)(s-b)(s-c)(s-d) - abcd\cos^2\frac{A+C}{2}}$$

内接四辺形（$A + C = 180°$）のときはブラーマグプタの公式：

$$S = \sqrt{(s-a)(s-b)(s-c)(s-d)}$$

**参考文献**：Pedoe, D. (1988). *Geometry: A Comprehensive Course*. Dover.

---

## 関連ページ

- [四角形](standard.md)
- [三角形（専門）](../triangle/professional.md)
- [円（専門）](../circle/professional.md)
