---
title: 関数
description: "入力に対して出力が一意に定まる対応"
goal: "関数が「入力と出力の対応」であることを理解し、定義域・値域・グラフの意味を説明できるようになる"
tags: [math,analysis,functions]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 解析
    path: /math/analysis/index.md
  - title: 関数
    path: /math/analysis/functions/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 等号・等式（入門）
    path: /math/algebra/equations/introduction.md
---

## 入力と出力の対応

自動販売機にボタンを押すと、決まった飲み物が出てきます。\
「押したボタン」が入力、「出てくる飲み物」が出力——これが**関数**のイメージです。

数学では、数を入力すると数が出力される対応を関数といいます。

$$x \mapsto x^2$$

$x$ に $3$ を入れると $9$ が出る。$-2$ を入れると $4$ が出る。

---

## 関数の書き方

$$f(x) = x^2$$

「$f$ という名前の関数で、$x$ を入れると $x^2$ が出る」という意味です。\
$f(3) = 9$、$f(-2) = 4$ のように、括弧の中に入力を書いて値を求めます。

---

## 定義域と値域

関数が受け付ける入力の範囲を**定義域**、出力がとりうる値の範囲を**値域**といいます。

$f(x) = \sqrt{x}$ は $x < 0$ のとき値が定まりません（負の数の平方根は実数でない）。\
この場合、定義域は $x \geq 0$ です。

---

## グラフ

関数のすべての入出力ペア $(x, f(x))$ を平面に点として描いたものが**グラフ**です。

グラフを見ると「$x$ が増えると $f(x)$ は増えるか減るか」「最大値・最小値はどこか」が一目でわかります。

---

## 1つの入力に1つの出力

関数の重要なルール：同じ入力には必ず同じ出力が対応します。\
「$x = 3$ を入れたら今日は $9$、明日は $10$」では関数になりません。

逆に「異なる入力が同じ出力になる」のはOKです。\
$f(2) = 4$ かつ $f(-2) = 4$ ——これは問題ありません。

---

## 関連ページ

- [一次関数（入門）](../../specific-functions/linear/introduction.md)
- [数列（入門）](../sequences/introduction.md)
