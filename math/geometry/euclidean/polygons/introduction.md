---
title: 多角形
description: "3辺以上の直線で囲まれた図形"
goal: "多角形の内角の和の法則と正多角形の特徴を説明できるようになる"
tags: [math,geometry,polygon]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 多角形
    path: /math/geometry/euclidean/polygons/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 三角形（入門）
    path: /math/geometry/euclidean/triangles/introduction.md
---

## 多角形とは

3辺以上の直線で囲まれた図形が**多角形**です。三角形（3辺）、四角形（4辺）、五角形（5辺）……。

---

## 内角の和

三角形の内角の和は180度、四角形は360度でした。規則があります。

1つの頂点から対角線を引いて三角形に分割してみましょう。$n$ 角形は $(n-2)$ 個の三角形に分けられます。

$$\text{$n$ 角形の内角の和} = (n-2) \times 180°$$

| 形 | 内角の和 |
|----|---------|
| 三角形 | $180°$ |
| 四角形 | $360°$ |
| 五角形 | $540°$ |
| 六角形 | $720°$ |

---

## 正多角形

すべての辺が等しく、すべての角が等しい多角形を**正多角形**といいます。

正三角形、正方形（正四角形）、正五角形、正六角形……。ハチの巣は正六角形で敷き詰められています。同じ面積を最も効率よく埋め尽くせる形の一つです。

---

## 円に近づく

正多角形の辺の数を増やすと、どんどん円に近づきます。コンピュータのグラフィクスでは、円を「辺が非常に多い正多角形」として近似して描いています。

---

## まとめ

$n$ 角形の内角の和は $(n-2) \times 180°$。辺の数を増やすほど円に近づきます。正多角形はすべての辺と角が等しく、タイリング（敷き詰め）の問題など様々な場面で現れます。

---

## 関連ページ

- [三角形（入門）](../triangles/introduction.md)
- [四角形（入門）](../quadrilaterals/introduction.md)
- [円（入門）](../circles/introduction.md)
