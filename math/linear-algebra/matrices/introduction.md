---
title: 行列
description: "数を格子状に並べた構造"
tags: [math,linear-algebra]
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
  - title: ベクトル
    path: /math/linear-algebra/vectors/introduction.md
  - title: 等号・等式
    path: /math/math-language/equations/introduction.md
---

## 連立方程式をまとめて書く

$$\begin{cases} 2x + y = 5 \\ x - y = 1 \end{cases}$$

この連立方程式を、係数だけ取り出して並べたものが**行列**です。

$$\begin{pmatrix} 2 & 1 \\ 1 & -1 \end{pmatrix}$$

方程式が3本に増えても4本に増えても、同じ枠組みで書けます。

---

## 変換として見る

行列は「ベクトルを変形する操作」としても読めます。

点 $(1, 0)$ を90度回転させると $(0, 1)$ になります。\
この「90度回転」という操作は、決まった行列で表せます。

拡大・縮小・反転・回転——こうした変換がすべて行列で統一的に扱えます。\
コンピュータグラフィクスで3Dの物体を動かすとき、まさにこの計算が使われています。

---

## 掛け算の順序が大事

「先に回転してから2倍に拡大する」のと\
「先に2倍に拡大してから回転する」では、結果が違います。

行列の掛け算では順序を変えると一般に答えが変わります。\
これは現実の変換の組み合わせ方と同じです。

---

## 関連ページ

- [ベクトル](../vectors/introduction.md)
- [等号・等式](../../math-language/equations/introduction.md)
