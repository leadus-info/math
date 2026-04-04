---
title: 複素数
description: "実数では解けない方程式から生まれた数"
tags: [math,numbers,complex-numbers]
level: introduction
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 数
    url: /math/numbers/index.html
  - title: 複素数
    url: /math/numbers/complex-numbers/introduction.html
levels:
  - level: introduction
  - level: standard
    url: standard.html
  - level: professional
    url: professional.html

requires:
  - title: 負数
    url: /math/numbers/negative-numbers/introduction
  - title: 乗法・べき乗
    url: /math/numbers/arithmetic/introduction
---



「2乗したら$-1$になる数は？」

正の数を2乗しても負の数を2乗しても、答えは必ず正になります。
だから実数の中にはこの問いの答えがありません——
「そういう数が存在することにしよう」と決めたのが複素数の出発点です。

---

## 虚数単位 i

2乗したら$-1$になる数を $i$（アイ）と定めます。
これを**虚数単位**といいます。

「虚数」という名前は「実際には存在しない数」というニュアンスで歴史的につけられましたが、
今日では電気工学・量子力学・信号処理など、きわめて「実用的な」数です。

---

## 複素数の形

$i$ を使って作られる数が**複素数**です。

例：$3 + 2i$、$-1 + i$、$5$（これも複素数、$5 + 0i$）

「実数部分」と「$i$ の係数部分」の組み合わせで表します。

---

## 複素平面

実数は数直線（1次元）で表せましたが、
複素数は平面（2次元）で表せます。

横軸を実部、縦軸を虚部にとった平面を**複素平面**といいます。
$3 + 2i$ は「右に3、上に2」の点です。

---

## なぜ重要なのか

複素数を使うと、すべての多項式方程式が必ず解を持ちます（代数学の基本定理）。
また、回転や波動の数学が非常にシンプルになります。

$e^{i\pi} + 1 = 0$（オイラーの等式）は、
$e$・$i$・$\pi$・$1$・$0$ という5つの数がひとつの式に現れる、
数学で最も美しい等式のひとつと言われます。

---

## 関連ページ

- [負数](../negative-numbers/introduction.md)
- [複素関数](../../functions/complex-functions/introduction.md)
