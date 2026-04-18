---
title: 行列
description: "数を格子状に並べた構造"
goal: "行列が連立方程式の係数をまとめたものであること、変換として捉えることができることを説明できるようになる"
tags: [math,linear-algebra,matrices]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 線形代数
    path: /math/linear-algebra/index.md
  - title: 行列
    path: /math/linear-algebra/matrices/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: ベクトル（入門）
    path: /math/linear-algebra/vectors/introduction.md
  - title: 等号・等式（入門）
    path: /math/math-language/equations/introduction.md
---

## 数を格子状に並べる

$$\begin{pmatrix} 2 & 1 \\ 1 & -1 \end{pmatrix}$$

こんな「数の表」が**行列**です。横の並びを「行」、縦の並びを「列」と呼びます。

---

## 連立方程式をコンパクトに書く

$$\begin{cases} 2x + y = 5 \\ x - y = 1 \end{cases}$$

この連立方程式の係数を取り出して行列にすると：

$$\begin{pmatrix} 2 & 1 \\ 1 & -1 \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 5 \\ 1 \end{pmatrix}$$

2本でも100本でも、同じ形で書けます。これが行列の強みのひとつです。

---

## 変換として見る

行列はベクトルを「変換する操作」とも読めます。行列をベクトルに掛けると、別のベクトルが得られます。

回転・拡大縮小・反転——こうした変換がすべて行列で統一的に表せます。コンピュータグラフィクスで3Dの物体を動かすとき、まさにこの計算が使われています。

---

## 掛け算の順序が大事

行列の掛け算では、順序を変えると結果が変わることがあります。

「先に回転してから拡大」と「先に拡大してから回転」では違う結果になる——現実の変換の組み合わせ方と同じです。

---

## まとめ

行列は「数を格子状に並べた構造」で、連立方程式をひとつの式で表す道具として登場しました。同時に「ベクトルを変換する操作」でもあり、2つの視点が線形代数を理解する鍵になります。

---

## 関連ページ

- [ベクトル（入門）](../vectors/introduction.md)
- [等号・等式（入門）](../../math-language/equations/introduction.md)
