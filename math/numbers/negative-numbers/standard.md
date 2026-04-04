---
title: 負数
description: "0 より小さい数と引き算"
tags: [math,numbers,negative-numbers]
hierarchy:
  - title: 数学
    path: /math/index.html
  - title: 数
    path: /math/numbers/index.html
  - title: 負数
    path: /math/numbers/negative-numbers/standard.html
levels:
  - level: introduction
    path: introduction.html
  - level: standard
  - level: professional
    path: professional.html
level: standard
requires:
  - title: 自然数
    path: /math/numbers/natural-numbers/introduction
---



> この記事は [入門](introduction.md) の続きです。先に入門を読むことを推奨します。

気温 $-5$ 度、残高 $-1000$ 円——0 より小さい数を**負数**といいます。  
[自然数](professional.md)の章で見たように、「3 引く 5」は自然数の中では答えが出ません。  
この「引けない」を解決するために負数を導入します。

## このページで扱うこと
- 負数の意味と数直線
- 絶対値
- 引き算の定義（負数を使って）
- 負数を含む掛け算・割り算の符号ルール

---

## 数直線

0 より左が負数、右が正の数です。

```
<----- 負の数 ------- 0 ------- 正の数 ----->
  -5  -4  -3  -2  -1  0   1   2   3   4   5
```

整数全体は $\ldots, -3, -2, -1, 0, 1, 2, 3, \ldots$ です。

---

## 絶対値

0 からどれだけ離れているかを**絶対値**といいます。

$$|3| = 3, \quad |-5| = 5, \quad |0| = 0$$

符号を取り除いた「大きさだけ」の値です。

---

## 引き算（減法）

引き算は「反対の符号の数を足すこと」として定義します。

$$a - b = a + (-b)$$

**例**：

$$5 - 3 = 5 + (-3) = 2$$
$$3 - 5 = 3 + (-5) = -2 \quad \text{（負数が登場）}$$
$$5 - (-3) = 5 + 3 = 8 \quad \text{（マイナスのマイナスはプラス）}$$

---

## 足し算のルール（符号が混在するとき）

**同じ符号どうし**：絶対値を足して、同じ符号をつけます。

$$(-3) + (-4) = -7$$

**異なる符号**：絶対値の差をとり、絶対値の大きい方の符号をつけます。

$$(-3) + 5 = 2, \quad 3 + (-7) = -4$$

---

## 掛け算・割り算の符号ルール

負数が加わっても、掛け算・割り算の仕組み自体は変わりません。  
変わるのは**符号の扱い**だけです。

| 組み合わせ | 結果の符号 |
|-----------|-----------|
| 正 × 正 | 正 |
| 負 × 負 | 正 |
| 正 × 負 | 負 |
| 負 × 正 | 負 |

$$(-3) \times (-4) = 12, \quad (-3) \times 4 = -12$$

割り算も同じ符号ルールが適用されます。

$$(-12) \div (-4) = 3, \quad (-12) \div 4 = -3$$

---

## 関連ページ

- [自然数](professional.md) — 加法・乗法の基礎
- [分数](professional.md) — 割り算が閉じないことから生まれる数
- [不等号・不等式](professional.md) — 大小の比較
- [負数（専門）](professional.md) — 整数環の代数的構造
