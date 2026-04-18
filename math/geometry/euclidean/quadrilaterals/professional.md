---
title: 四角形
description: "ブレーシュナイダーの公式・調和共役・射影的性質"
goal: "一般四角形の面積公式（ブレーシュナイダー）とトレミーの定理の証明を説明できるようになる"
tags: [math,geometry,quadrilateral]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 四角形
    path: /math/geometry/euclidean/quadrilaterals/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 四角形（標準）
    path: /math/geometry/euclidean/quadrilaterals/standard.md
  - title: 三角形（専門）
    path: /math/geometry/euclidean/triangles/professional.md
---

## ブレーシュナイダーの公式

辺 $a, b, c, d$、対角の和の半角 $\sigma = \frac{A+C}{2}$ を持つ一般四辺形の面積：

$$S = \sqrt{(s-a)(s-b)(s-c)(s-d) - abcd\cos^2\sigma}$$

（$s = \frac{a+b+c+d}{2}$）

**内接四辺形**（$A + C = 180°$、$\sigma = 90°$、$\cos\sigma = 0$）の場合、**ブラーマグプタの公式**：

$$S = \sqrt{(s-a)(s-b)(s-c)(s-d)}$$

ヘロンの公式（三角形（専門）参照）は $d = 0$ の特殊ケースです。

**参考文献**：Coolidge, J. L. (1939). "A historically interesting formula for the area of a quadrilateral." *American Mathematical Monthly*, 46(6), 345–347.

---

## トレミーの定理の証明

**定理**：円に内接する四辺形 $ABCD$ において $AC \cdot BD = AB \cdot CD + AD \cdot BC$

**証明**：$BD$ 上に $\angle BAP = \angle CAD$ となる点 $P$ をとります。$\angle ABP = \angle ACD$（同弧に対する円周角）なので $\triangle ABP \sim \triangle ACD$。よって $\frac{BP}{CD} = \frac{AB}{AC}$、$BP = \frac{AB \cdot CD}{AC}$。

同様に $\triangle ABC \sim \triangle APD$ から $PD = \frac{AD \cdot BC}{AC}$。

$BD = BP + PD = \frac{AB \cdot CD + AD \cdot BC}{AC}$ より $AC \cdot BD = AB \cdot CD + AD \cdot BC$。$\square$

---

## 調和共役と完全四点形

直線上の4点 $A, B, C, D$ の交比 $(A,B;C,D) = -1$ のとき $C$ と $D$ は**調和共役**といいます。

完全四点形（4直線の6交点からなる図形）において、対角3点のそれぞれが残りの辺から調和共役の対を作ります。これは射影幾何の基本的な構成です。

---

## 関連ページ

- [四角形（標準）](standard.md)
- [円（専門）](../circles/professional.md)
- [直線（専門）](../../coordinate/line/professional.md)
