---
title: 行列
description: "数を格子状に並べた構造"
tags: [math,linear-algebra]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 線形代数
    path: /math/linear-algebra/index.html
  - title: 行列
    path: /math/linear-algebra/matrices/introduction.html
levels:
  - level: 入門
  - level: 標準
    path: standard.html
  - level: 専門
    path: professional.html

requires:
  - title: ベクトル
    path: /math/linear-algebra/vectors/introduction.html
  - title: 等号・等式
    path: /math/math-language/equations/introduction.html
---


## 連立方程式と行列

2つ、3つの方程式を同時に解く問題を連立方程式といいます。
行列を使うとこれをまとめて一つの式で書けます。
2本の方程式が200本になっても、行列の仕組みは同じです。

---

## 変換としての行列

行列はベクトルを「変換」する操作として見ることもできます。
回転・拡大縮小・反転——コンピュータグラフィクスで3Dの物体を動かすとき、
行列を使って計算しています。

---

## 掛け算の順序が重要

行列の掛け算では、順序を変えると結果が変わることがあります。
「先に回転してから拡大」と「先に拡大してから回転」では結果が違う——
現実の変換の組み合わせ方と同じです。

---

## 関連ページ

- [ベクトル](../vectors/introduction.md)
