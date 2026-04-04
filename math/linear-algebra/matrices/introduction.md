---
title: 行列
description: "数を格子状に並べた構造"
tags: [math,linear-algebra]
level: introduction
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 線形代数
    href: /math/linear-algebra/index.html
  - text: 行列
    href: /math/linear-algebra/matrices/introduction.html
levels:
  - level: introduction
  - level: standard
    url: standard.html
  - level: professional
    url: professional.html

requires:
  - title: ベクトル
    url: /math/linear-algebra/vectors/introduction
  - title: 等号・等式
    url: /math/math-language/equations/introduction
---

# 行列
$egin{pmatrix}1 & 2 \ 3 & 4\end{pmatrix}$

数を格子状に並べたものが**行列**です。
連立方程式をまとめて扱ったり、空間の変換（回転・拡大・縮小）を表したりできます。

---

## 連立方程式と行列

$egin{cases}2x + y = 5 \ x - y = 1\end{cases}$

このような方程式を行列で書くと、まとめて操作できます。
2本の方程式が2000本になっても、行列の仕組みは同じです。

---

## 変換としての行列

行列はベクトルを「変換」する操作です。

回転：点を原点を中心に回す
拡大・縮小：大きさを変える
反転：鏡に映す

コンピュータグラフィクスで3Dの物体を動かすとき、行列を使って計算しています。

---

## なぜ掛け算の順序が重要か

行列の掛け算では $AB 
eq BA$ が一般的です。
「先に回転してから拡大」と「先に拡大してから回転」では結果が違う——
現実の変換の組み合わせ方と同じです。

---

## 関連ページ

- [ベクトル](../vectors/introduction.md)
