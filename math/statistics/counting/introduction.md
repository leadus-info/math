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

## 「何通り」を数える

コインを1回投げると「表・裏」の2通り。\
2回投げると「表表・表裏・裏表・裏裏」の4通り。\
3回投げると何通りでしょう？

「何通りあるか」を数えるのが**場合の数**です。

---

## 組み合わせる——掛け算

服が3着、ズボンが4本あるとき、コーディネートは何通り？\
服の選び方3通りそれぞれに、ズボンの選び方が4通りあります。

$3 \times 4 = 12$ 通り。

2つの選択が独立して組み合わさるとき、**掛け算**を使います。

---

## どちらか——足し算

バス停が2か所あって、バスの本数が「停留所Aから3本、Bから5本」なら\
乗れるバスは合計何本？

$3 + 5 = 8$ 本。

「AかBのどちらか一方を選ぶ」（同時には使えない）とき、**足し算**を使います。

---

## 並び方と選び方の違い

5人から3人を「1位・2位・3位」に選ぶ——順番が意味を持ちます。\
5人から3人のチームを作る——誰と誰が選ばれるかだけが問題で順番は無関係。

同じ「5人から3人」でも、前者の方が後者より多くなります。\
（前者には「田中1位・鈴木2位・佐藤3位」と「鈴木1位・田中2位・佐藤3位」が区別されるため）

---

## 関連ページ

- [確率](../probability/introduction.md)
