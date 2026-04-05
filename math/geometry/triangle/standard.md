---
title: 三角形
description: "三点で定まる基本図形"
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
  - title: 点
    path: /math/geometry/point/introduction.md
  - title: 直線
    path: /math/geometry/line/introduction.md
  - title: 三角関数
    path: /math/functions/trigonometric/introduction.md
---

## 基本的な定義

3点 $A, B, C$（同一直線上にない）を頂点とする多角形が**三角形** $\triangle ABC$ です。\
辺 $BC, CA, AB$ の長さをそれぞれ $a, b, c$、\
頂点 $A, B, C$ の内角をそれぞれ $A, B, C$ と書きます。

---

## 内角の和

**定理**：三角形の内角の和は $180°$ です。

**証明**：頂点 $A$ を通り辺 $BC$ に平行な直線 $l$ を引きます。\
平行線の錯角より $\angle BAC$、辺 $AB$ と $l$ のなす角が $B$ に等しく、\
辺 $AC$ と $l$ のなす角が $C$ に等しいので、直線上の角の和より $A + B + C = 180°$。

**系（外角定理）**：三角形の一つの外角は、それに隣り合わない2つの内角の和に等しい。

---

## 面積

$$S = \frac{1}{2} \times a \times h_a = \frac{1}{2}ab\sin C$$

（$h_a$ は辺 $a$ に対する高さ、$\sin C$ を使う式は2辺とその間の角から計算）

**例**：$a = 6, b = 5, C = 30°$ のとき $S = \frac{1}{2} \times 6 \times 5 \times \frac{1}{2} = \frac{15}{2}$

**ヘロンの公式**（3辺 $a, b, c$ から面積を求める）：

$$s = \frac{a+b+c}{2}, \quad S = \sqrt{s(s-a)(s-b)(s-c)}$$

**例**：$a=3, b=4, c=5$ のとき $s=6$、$S = \sqrt{6 \cdot 3 \cdot 2 \cdot 1} = 6$。

---

## 正弦定理

**定理**：外接円の半径を $R$ とすると

$$\frac{a}{\sin A} = \frac{b}{\sin B} = \frac{c}{\sin C} = 2R$$

**使いどころ**：2角と1辺、または2辺と1角（非挟角）がわかるとき。

**例題**：$A = 30°, B = 45°, a = 3$ のとき $b$ を求めます。\
$C = 180° - 75° = 105°$\
$\frac{3}{\sin 30°} = \frac{b}{\sin 45°}$\
$b = 3 \times \frac{\sin 45°}{\sin 30°} = 3 \times \frac{\sqrt{2}/2}{1/2} = 3\sqrt{2}$

---

## 余弦定理

**定理**：

$$a^2 = b^2 + c^2 - 2bc\cos A$$

$A = 90°$ のとき $\cos 90° = 0$ となり**ピタゴラスの定理**の一般化になります。

**使いどころ**：3辺または2辺とその間の角がわかるとき。

**例題**：$b=5, c=7, A=60°$ のとき $a$ を求めます。\
$a^2 = 25 + 49 - 2 \times 5 \times 7 \times \cos 60° = 74 - 35 = 39$\
$a = \sqrt{39}$

---

## 五心

| 点 | 定義 | 座標での求め方 |
|----|------|--------------|
| 重心 $G$ | 3本の中線の交点 | 3頂点の座標の平均 |
| 外心 $O$ | 外接円の中心 | 各辺の垂直二等分線の交点 |
| 内心 $I$ | 内接円の中心 | 各頂点の角の二等分線の交点 |
| 垂心 $H$ | 3本の垂線の交点 | — |
| 傍心 | 傍接円の中心（3個） | — |

**定理（オイラー線）**：重心 $G$、外心 $O$、垂心 $H$ は同一直線（オイラー線）上にあり、\
$\overrightarrow{OG} : \overrightarrow{OH} = 1 : 3$ が成り立ちます。

---

## 関連ページ

- [三角関数](../../functions/trigonometric/introduction.md)
- [円](../circle/introduction.md)
