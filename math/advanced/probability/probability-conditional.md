---
title: 条件付き確率とベイズの定理
description: "情報が加わったときに確率を更新する"
goal: "条件付き確率の意味を理解し、ベイズの定理を使って結果から原因の確率を求められるようになる"
tags: [math, probability]
stage: advanced
subject: 確率
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 応用編
    path: ../index.md
  - title: 条件付き確率とベイズの定理
    path: probability-conditional.md
requires:
  - title: 確率
    path: probability.md
---

## 条件付き確率

$B$ が起きたとわかった上での $A$ の確率：

$$P(A \mid B) = \frac{P(A \cap B)}{P(B)} \quad (P(B) > 0)$$

**例題**：赤玉3個・白玉2個の袋から2個取り出す。「1個目が赤のとき2個目も赤である確率」は、残りが赤2・白2の4個なので $P = \dfrac{2}{4} = \dfrac{1}{2}$。

---

## ベイズの定理

$$P(A \mid B) = \frac{P(B \mid A) P(A)}{P(B)}$$

「結果 $B$ が観測されたとき原因 $A$ の確率」を求めます。

**例題**：罹患率1%の病気で、感度99%・特異度95%の検査が陽性だったとき実際に罹患している確率は？

$$P(\text{陽性}) = 0.99 \times 0.01 + 0.05 \times 0.99 = 0.0594$$
$$P(\text{罹患} \mid \text{陽性}) = \frac{0.99 \times 0.01}{0.0594} \approx 0.167$$

「陽性 $=$ 罹患」ではないという直感に反する重要な結果です。

---

## まとめ

条件付き確率は、ある事象が起きたとわかった上での別の事象の確率です。ベイズの定理は、結果から原因の確率を逆算するときに使われます。

---

## 関連ページ

- [確率変数と確率分布（応用編）](random-variables.md)
