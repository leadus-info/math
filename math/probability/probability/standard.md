---
title: 確率
description: "確率の定義・条件付き確率・ベイズの定理"
goal: "確率の基本法則・独立・条件付き確率・ベイズの定理を使って確率を計算できるようになる"
tags: [math,statistics,probability]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 統計・確率
    path: /math/probability/index.md
  - title: 確率
    path: /math/probability/probability/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 確率（入門）
    path: /math/probability/probability/introduction.md
  - title: 場合の数（標準）
    path: /math/probability/counting/standard.md
---

## 確率の定義（古典的確率）

同様に確からしい $n$ 個の根元事象から成る試行で、事象 $A$ に含まれる根元事象が $m$ 個のとき：

$$P(A) = \frac{m}{n}$$

**公理**（コルモゴロフ）：

1. $0 \leq P(A) \leq 1$
2. $P(\Omega) = 1$（全事象）
3. 互いに排反な $A, B$：$P(A \cup B) = P(A) + P(B)$

---

## 加法定理

$$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$

**例**：サイコロで「偶数または3以上」。$P(\text{偶数}) = \frac{1}{2}$、$P(\text{3以上}) = \frac{4}{6}$、$P(\text{偶数かつ3以上}) = P(\{4,6\}) = \frac{1}{3}$。$P = \frac{1}{2} + \frac{2}{3} - \frac{1}{3} = \frac{5}{6}$。

---

## 余事象

$$P(\bar{A}) = 1 - P(A)$$

**例題**：コインを3回投げて「少なくとも1回表が出る確率」。

余事象「3回とも裏」：$P = \left(\frac{1}{2}\right)^3 = \frac{1}{8}$。求める確率：$1 - \frac{1}{8} = \frac{7}{8}$。

---

## 独立と積の法則

事象 $A$ と $B$ が**独立**とは $P(A \cap B) = P(A) P(B)$ が成り立つことです（一方の結果が他方に影響しない）。

**例**：コインを2回投げるとき「1回目が表」と「2回目が表」は独立。$P(\text{両方表}) = \frac{1}{2} \times \frac{1}{2} = \frac{1}{4}$。

---

## 条件付き確率

$B$ が起きたとわかった上での $A$ の確率：

$$P(A \mid B) = \frac{P(A \cap B)}{P(B)} \quad (P(B) > 0)$$

**例題**：赤玉3個・白玉2個の袋から2個取り出す。「1個目が赤のとき2個目も赤である確率」：

残りは赤2・白2の4個。$P = \frac{2}{4} = \frac{1}{2}$。

---

## ベイズの定理

$$P(A \mid B) = \frac{P(B \mid A) P(A)}{P(B)}$$

「結果 $B$ が観測されたとき原因 $A$ の確率」を求めます。

**例題**：罹患率1%の病気で、感度99%・特異度95%の検査が陽性だったとき実際に罹患している確率は？

$P(\text{陽性}) = 0.99 \times 0.01 + 0.05 \times 0.99 = 0.0594$

$P(\text{罹患} \mid \text{陽性}) = \frac{0.99 \times 0.01}{0.0594} \approx 0.167$（約17%のみ）

「陽性 $=$ 罹患」ではないという直感に反する重要な結果です。

---

## 関連ページ

- [場合の数（標準）](../counting/standard.md)
- [確率（専門）](professional.md)
