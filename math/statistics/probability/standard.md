---
title: 確率
description: "起こりやすさを数値で表す"
tags: [math,statistics,probability]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 統計・確率
    path: /math/statistics/index.md
  - title: 確率
    path: /math/statistics/probability/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 場合の数
    path: /math/statistics/counting/introduction.md
  - title: 分数
    path: /math/numbers/fractions/introduction.md
---

## 確率の定義（古典的確率）

**定義**：すべての根元事象が同様に確からしい試行において、\
全根元事象が $n$ 個あり、事象 $A$ に含まれる根元事象が $m$ 個のとき

$$P(A) = \frac{m}{n}$$

**性質**：
- $0 \leq P(A) \leq 1$
- $P(\Omega) = 1$（全事象の確率は1）
- $P(\emptyset) = 0$（空事象の確率は0）

**例**：サイコロを1回振るとき $\Omega = \{1,2,3,4,5,6\}$。\
偶数が出る事象 $A = \{2,4,6\}$ の確率 $P(A) = \frac{3}{6} = \frac{1}{2}$。

---

## 余事象

**定義**：$A$ が起きない事象を余事象 $\bar{A}$（または $A^c$）といいます。

$$P(\bar{A}) = 1 - P(A)$$

**「少なくとも」の問題では余事象が強力です。**

**例題**：硬貨を4回投げて少なくとも1回表が出る確率を求めます。\
余事象「4回全部裏」の確率 $= \left(\frac{1}{2}\right)^4 = \frac{1}{16}$\
求める確率 $= 1 - \frac{1}{16} = \frac{15}{16}$

---

## 加法定理

$$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$

$A$ と $B$ が**排反**（$A \cap B = \emptyset$）のとき：

$$P(A \cup B) = P(A) + P(B)$$

**例**：サイコロで偶数または3以上が出る確率。\
$P(\text{偶数}) = \frac{1}{2}$、$P(\text{3以上}) = \frac{4}{6} = \frac{2}{3}$\
$P(\text{偶数かつ3以上}) = P(\{4,6\}) = \frac{1}{3}$\
$P = \frac{1}{2} + \frac{2}{3} - \frac{1}{3} = \frac{5}{6}$

---

## 独立と積の法則

事象 $A$ と $B$ が**独立**とは $P(A \cap B) = P(A)P(B)$ が成り立つことです。

直感的には「$A$ の結果が $B$ の起こりやすさに影響しない」状況です。

**例**：コインを2回投げるとき「1回目表」と「2回目表」は独立。\
$P(\text{両方表}) = \frac{1}{2} \times \frac{1}{2} = \frac{1}{4}$

---

## 条件付き確率

**定義**：$P(B) > 0$ のとき、$B$ が起きたという条件のもとで $A$ が起きる確率を

$$P(A \mid B) = \frac{P(A \cap B)}{P(B)}$$

で定めます。

**例題**：赤玉3個・白玉2個の袋から2個取り出す。\
「1個目が赤」のとき「2個目も赤」である確率を求めます。\
1個目が赤のとき、残りは赤2・白2の4個。\
$P(\text{2個目赤} \mid \text{1個目赤}) = \frac{2}{4} = \frac{1}{2}$

---

## ベイズの定理

$$P(A \mid B) = \frac{P(B \mid A) \cdot P(A)}{P(B)}$$

「結果 $B$ が観測されたとき、原因 $A$ の確率」を求めます。

**例題（医療検査）**：ある病気の罹患率1%、検査の感度99%（罹患者の99%が陽性）、\
特異度95%（非罹患者の95%が陰性）。陽性のとき実際に罹患している確率は？

$P(\text{罹患}) = 0.01$、$P(\text{陽性} \mid \text{罹患}) = 0.99$\
$P(\text{陽性}) = 0.99 \times 0.01 + 0.05 \times 0.99 = 0.0099 + 0.0495 = 0.0594$\
$P(\text{罹患} \mid \text{陽性}) = \frac{0.99 \times 0.01}{0.0594} \approx 0.167$

陽性でも約17%しか罹患していません（偽陽性の多さ）——直感に反する重要な結果です。

---

## 関連ページ

- [場合の数](../counting/introduction.md)
