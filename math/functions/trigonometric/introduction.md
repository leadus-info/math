---
title: 三角関数
description: "角度と波をつなぐ関数"
goal: "三角関数の基本的なアイデアと必要性を日常的な例を使って説明できるようになる"
tags: [math,functions,trigonometric]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/functions/index.md
  - title: 三角関数
    path: /math/functions/trigonometric/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 円
    path: /math/geometry/circle/introduction.md
---

## 円と角度から生まれる

半径1の円（単位円）の上を点が動きます。スタート地点（右端）から角度 $\theta$ だけ動いたとき、その点の「縦の座標」が $\sin \theta$（サイン）、「横の座標」が $\cos \theta$（コサイン）です。

円をぐるっと一周すると、点は元の位置に戻ります。つまり $\sin$ も $\cos$ も、一周ごとに値が繰り返します——これが**周期性**です。

---

## 波の形

$\sin \theta$ の値を角度に対してグラフに描くと、波のような形になります。

- 0から始まり、頂点（最大値1）に達し、また0に戻り、底（最小値−1）に達して0に戻る
- これを繰り返す

音・光・電波・地震波——あらゆる「波」はこのサイン波の組み合わせで表せます。

---

## 直角三角形での意味

$\sin$ と $\cos$ は、直角三角形の辺の比としても理解できます。

角度 $\theta$ の直角三角形において：
- $\sin \theta$ = 向かいの辺 ÷ 斜辺
- $\cos \theta$ = 隣の辺 ÷ 斜辺

これが「三角関数」という名前の由来です。

---

## どこで使われるか

- 振動・波動の記述（物理、音響、電気工学）
- 3D グラフィクスでの回転計算
- GPS の誤差補正

「周期的な変化」や「回転」が関わる場面で三角関数は欠かせません。

---

## まとめ

三角関数（$\sin$・$\cos$ など）は、単位円上の点の座標として定義されます。グラフは周期的な波形であり、音・光・電波など自然界の波現象を記述するための基本的な道具です。

---

## 関連ページ

- [円（入門）](../../geometry/circle/introduction.md)
- [複素数（入門）](../../numbers/complex-numbers/introduction.md)
