---
title: 指数関数
description: "倍々で増える変化を表す関数"
goal: "指数関数の基本的なアイデアと必要性を日常的な例を使って説明できるようになる"
tags: [math,functions,exponential]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/analysis/index.md
  - title: 指数関数
    path: /math/specific-functions/exponential/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 乗法・べき乗
    path: /math/numbers/arithmetic/introduction.md
---

## 倍々で増える

「毎日2倍になる細菌がいる。今日1匹なら、10日後は？」

| 日 | 1日目 | 2日目 | 3日目 | 4日目 | 5日目 |
|----|-------|-------|-------|-------|-------|
| 匹数 | 2 | 4 | 8 | 16 | 32 |

10日後は $2^{10} = 1024$ 匹になります。「毎日2匹ずつ増える」場合（10日後は21匹）と比べると、その差は圧倒的です。

このように「一定の割合で増え続ける」変化を表す関数が**指数関数**です。

---

## グラフの形

$y = 2^x$ のグラフは最初はゆるやかですが、右に行くほど急激に上がります。逆に、$y = \left(\frac{1}{2}\right)^x$ のグラフは右に行くほど 0 に近づいていきます（但し決して 0 にはなりません）。

「底が1より大きければ増加、1より小さければ減衰」——これが指数関数の基本パターンです。

---

## 身の回りの例

- **複利**：元金が毎年一定の割合で増える
- **放射性物質の半減期**：一定時間ごとに量が半分になる
- **感染症の初期拡大**：感染者が一定の割合で増える

「一定の割合で変化する」現象はすべて指数関数でモデル化できます。

---

## まとめ

指数関数は「一定の割合で増減する」変化を表します。変化のスピード自体が変わっていく（増えるほど速く増える、減るほど遅く減る）のが特徴で、等差数列的な変化とは全く異なります。

---

## 関連ページ

- [乗法・べき乗（入門）](../../numbers/arithmetic/introduction.md)
- [対数関数（入門）](../logarithmic/introduction.md)
