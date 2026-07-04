---
title: 三角形
description: "3本の辺で囲まれた最も基本的な多角形"
goal: "三角形の内角の和が180度である理由と、三平方の定理の意味を説明できるようになる"
tags: [math,geometry,triangle]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 三角形
    path: /math/geometry/euclidean/triangles/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 直線（入門）
    path: /math/geometry/coordinate/line/introduction.md
---

## 最もシンプルな多角形

3本の直線で囲まれた図形が**三角形**です。3本の直線で囲めばどんな形でも三角形になります——細長くても、ほぼ直角でも。

どんな複雑な多角形も三角形に分割できるため、三角形は幾何学の基本単位です。

---

## 内角の和は必ず180度

三角形のどんな形でも、3つの角を足すと必ず180度になります。

頂点 A から辺 BC に平行な直線を引いてみましょう。平行線の性質（錯角）から、三角形の3つの角が直線上に並ぶことがわかり、合計が180度になります。

**「2つの角がわかれば、3つ目の角が自動的に決まる」**——これが三角形の強力な性質です。

---

## 三平方の定理（ピタゴラスの定理）

直角三角形では「斜辺の2乗は、他の2辺の2乗の和に等しい」という関係があります。

$$3^2 + 4^2 = 5^2 \quad (9 + 16 = 25)$$

3・4・5の組み合わせは直角三角形になります。古代エジプトでは建築の直角確認にこの性質が使われました。

---

## 辺と角の対応

大きい角に向かい合う辺ほど長くなります。最も大きい角が直角なら、向かい合う辺が最も長い——これが斜辺です。

---

## まとめ

三角形は3辺・3角で構成される最もシンプルな多角形です。内角の和は常に180度。直角三角形では三平方の定理が成り立ち、辺と角の対応関係があります。これらは正弦定理・余弦定理（標準で扱います）の基礎になります。

---

## 関連ページ

- [点（入門）](../../coordinate/point/introduction.md)
- [直線（入門）](../../coordinate/line/introduction.md)
- [三角関数（入門）](../../trigonometry/introduction.md)
