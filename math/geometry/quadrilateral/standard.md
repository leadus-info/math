---
title: 四角形
description: "4辺で囲まれた図形の種類と性質"
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
  - title: 三角形
    path: /math/geometry/triangle/introduction.md
  - title: 直線
    path: /math/geometry/line/introduction.md
---

## 四角形の種類と定義

**定義**：4本の直線で囲まれた多角形が**四角形**です。

内角の和は $360°$（三角形 $180°$ × 2、対角線で分割）。

各種類の定義と包含関係：

| 図形 | 定義 |
|------|------|
| 四角形 | 4辺の多角形 |
| 台形 | 1組の対辺が平行 |
| 平行四辺形 | 2組の対辺が平行 |
| 長方形 | 平行四辺形かつ全角が直角 |
| ひし形 | 平行四辺形かつ全辺が等長 |
| 正方形 | 長方形かつひし形 |

「正方形は長方形であり、ひし形でもあり、平行四辺形でもある」——より条件が多いほど特別な図形です。

---

## 各図形の性質

**平行四辺形**：
- 対辺は等長かつ平行：$AB = CD$、$AD = BC$
- 対角は等しい：$\angle A = \angle C$、$\angle B = \angle D$
- 対角線は互いを二等分する

**長方形**（平行四辺形の性質 + ）：
- 対角線の長さが等しい
- 対角線の長さ $= \sqrt{a^2 + b^2}$（$a, b$ は辺の長さ）

**ひし形**（平行四辺形の性質 + ）：
- 対角線が垂直に交わる
- 対角線が各頂点の角を二等分する

**正方形**：長方形とひし形の両方の性質を持つ。

---

## 面積の公式

| 図形 | 面積 | 導出のポイント |
|------|------|--------------|
| 平行四辺形 | 底辺 × 高さ | 長方形から三角形を移動 |
| 長方形 | 縦 × 横 | 定義から直接 |
| ひし形 | 対角線₁ × 対角線₂ ÷ 2 | 外接長方形の半分 |
| 台形 | (上底 + 下底) × 高さ ÷ 2 | 平行四辺形の半分として導出 |

**台形の面積の導出**：\
台形を 2 個組み合わせると平行四辺形になります。\
平行四辺形の底辺は「上底 + 下底」、高さは同じなので、台形の面積はその半分。

---

## 例題

**例題**：平行四辺形 $ABCD$ で $AB = 8$、$BC = 5$、$\angle B = 60°$ のとき面積を求めます。\
高さ $= BC \sin 60° = 5 \times \frac{\sqrt{3}}{2} = \frac{5\sqrt{3}}{2}$\
面積 $= 8 \times \frac{5\sqrt{3}}{2} = 20\sqrt{3}$

---

## 関連ページ

- [三角形](../triangle/introduction.md)
- [多角形](../polygon/introduction.md)
