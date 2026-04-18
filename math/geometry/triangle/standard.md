---
title: 三角形
description: "面積・正弦定理・余弦定理・五心"
goal: "正弦定理・余弦定理を使って三角形の辺と角を計算し、面積公式やヘロンの公式を適用できるようになる"
tags: [math,geometry,triangle]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 三角形
    path: /math/geometry/triangle/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 三角形（入門）
    path: /math/geometry/triangle/introduction.md
  - title: 三角関数（標準）
    path: /math/functions/trigonometric/standard.md
---

## 基本的な定義

3点 $A, B, C$ を頂点とする三角形 $\triangle ABC$ で、辺 $BC, CA, AB$ の長さをそれぞれ $a, b, c$、頂点の内角をそれぞれ $A, B, C$ と書きます。

**定理（内角の和）**：$A + B + C = 180°$

**証明**：頂点 $A$ を通り辺 $BC$ に平行な直線を引くと、錯角の関係から3角の和が直線（$180°$）に一致する。$\square$

---

## 面積の公式

$$S = \frac{1}{2} \times \text{底辺} \times \text{高さ} = \frac{1}{2}ab\sin C$$

$\sin C$ を使う公式は「2辺 $a, b$ とその間の角 $C$ から面積を求める」場合に便利です。

**例**：$a = 6, b = 5, C = 30°$ のとき $S = \frac{1}{2} \times 6 \times 5 \times \frac{1}{2} = \frac{15}{2}$

**ヘロンの公式**（3辺 $a, b, c$ から面積）：

$$s = \frac{a+b+c}{2}, \quad S = \sqrt{s(s-a)(s-b)(s-c)}$$

**例**：$a=3, b=4, c=5$ のとき $s=6$、$S = \sqrt{6 \cdot 3 \cdot 2 \cdot 1} = 6$。

---

## 正弦定理

外接円の半径を $R$ とするとき：

$$\frac{a}{\sin A} = \frac{b}{\sin B} = \frac{c}{\sin C} = 2R$$

**使いどころ**：2角と1辺がわかるとき、または2辺と対角（挟まない角）がわかるとき。

**例題**：$A = 30°, B = 45°, a = 3$ のとき $b$ を求めます。

$C = 105°$。$\frac{3}{\sin 30°} = \frac{b}{\sin 45°}$ より $b = 3 \times \frac{\sqrt{2}/2}{1/2} = 3\sqrt{2}$。

---

## 余弦定理

$$a^2 = b^2 + c^2 - 2bc\cos A$$

$A = 90°$ のとき $\cos 90° = 0$ となり三平方の定理の一般化になります。

**使いどころ**：3辺がわかるとき（角を求める）、または2辺とその間の角がわかるとき（辺を求める）。

**例題**：$b=5, c=7, A=60°$ のとき $a$ を求めます。

$a^2 = 25 + 49 - 2 \times 5 \times 7 \times \frac{1}{2} = 74 - 35 = 39$、$a = \sqrt{39}$。

---

## 五心

| 点 | 定義 | 座標 |
|----|------|------|
| 重心 $G$ | 3中線の交点 | 3頂点の座標の平均 |
| 外心 $O$ | 外接円の中心 | 各辺の垂直二等分線の交点 |
| 内心 $I$ | 内接円の中心 | 各角の二等分線の交点 |
| 垂心 $H$ | 3高さの足の交点 | — |

$G$, $O$, $H$ は同一直線（オイラー線）上にあり、$OG : GH = 1 : 2$。

---

## 関連ページ

- [三角関数（標準）](../../functions/trigonometric/standard.md)
- [円（標準）](../circle/standard.md)
