---
title: 四角形
description: "各種四角形の性質・面積・内接四辺形"
goal: "各種四角形の定義と性質を使って面積を求め、内接四辺形の性質を説明できるようになる"
tags: [math,geometry,quadrilateral]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 四角形
    path: /math/geometry/quadrilateral/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 四角形（入門）
    path: /math/geometry/quadrilateral/introduction.md
  - title: 三角形（標準）
    path: /math/geometry/triangle/standard.md
---

## 各種四角形の性質まとめ

| 図形 | 対辺 | 対角 | 対角線 |
|------|------|------|--------|
| 平行四辺形 | 等長・平行 | 等しい | 互いを二等分 |
| 長方形 | 等長・平行 | すべて直角 | 等長・互いを二等分 |
| ひし形 | すべて等長 | 対角が等しい | 垂直に二等分 |
| 正方形 | すべて等長 | すべて直角 | 等長・垂直に二等分 |

---

## 面積の導出

**平行四辺形**：長方形から三角形を移動することで、底辺 × 高さとなります。

**台形**：同じ台形を2枚用意して平行四辺形を作ると、面積は $(上底 + 下底) \times 高さ \div 2$。

**ひし形**：対角線が垂直に交わるので、外接長方形の面積の半分。面積 $= \frac{d_1 \times d_2}{2}$。

**例題**：対角線が $6$ と $8$ のひし形の面積：$\frac{6 \times 8}{2} = 24$

---

## 平行四辺形の面積（一般形）

2辺 $a, b$ とその間の角 $\theta$ から：$S = ab\sin\theta$

**例**：$a=5, b=4, \theta=60°$ のとき $S = 5 \times 4 \times \frac{\sqrt{3}}{2} = 10\sqrt{3}$

---

## 内接四辺形

円に内接する四辺形を**内接四辺形**といいます。

**定理**：内接四辺形の対角の和は $180°$。

**証明**：同じ弧に対する円周角の関係（円周角の定理）から導きます。

**トレミーの定理**：内接四辺形 $ABCD$ で：

$$AC \cdot BD = AB \cdot CD + AD \cdot BC$$

---

## 関連ページ

- [三角形（標準）](../triangle/standard.md)
- [円（標準）](../circle/standard.md)
