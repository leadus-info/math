---
title: 場合の数
description: "「何通りあるか」を数える"
tags: [math,statistics]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 統計・確率
    path: /math/statistics/index.md
  - title: 場合の数
    path: /math/statistics/counting/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 自然数
    path: /math/numbers/natural-numbers/introduction.md
---

## 「何通りあるか」を数える

ランチセットで「ごはんかパン」「魚か肉か野菜」を選ぶとします。\
組み合わせは全部で何通りあるでしょう？

表にして数えてみましょう：

| | 魚 | 肉 | 野菜 |
|--|----|----|------|
| ごはん | ごはん＋魚 | ごはん＋肉 | ごはん＋野菜 |
| パン | パン＋魚 | パン＋肉 | パン＋野菜 |

2 × 3 = 6 通りあります。

「何通りあるか」を数えるのが**場合の数**です。

---

## 掛け算で数える

ごはんかパンの選び方が 2 通り、おかずの選び方が 3 通り。\
それぞれ独立して選べるので、組み合わせは $2 \times 3 = 6$ 通りです。

**独立して選べる場合は掛け算を使います。**

### 練習

Tシャツが 4 色、ズボンが 3 色あるとき、組み合わせは何通り？\
$4 \times 3 = 12$ 通りです。

---

## 足し算で数える

家から駅まで「バス」または「自転車」で行くとします。\
バスのルートが 3 通り、自転車のルートが 2 通りあります。

どちらか 1 つを使うので、合計は $3 + 2 = 5$ 通りです。

**どちらか一方を選ぶ場合は足し算を使います。**（同時に使えない場合）

---

## 並べ方と選び方の違い

A・B・C の 3 人から 2 人を「1 位・2 位」に選ぶとき：\
AB、AC、BA、BC、CA、CB の **6 通り**（順番が大事）

A・B・C の 3 人から 2 人をチームに選ぶとき：\
AB、AC、BC の **3 通り**（順番は関係ない）

同じ「3 人から 2 人」でも、順番を区別するかしないかで答えが変わります。

---

## 関連ページ

- [確率](../probability/introduction.md)
