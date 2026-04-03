---
title: 不等号・不等式
description: "「大きい・小さい」を記号で表す"
difficulty: 1
tags: [math,math-language,inequalities]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数学の言語
    href: /math/math-language/index.html
  - text: 不等号・不等式
    href: /math/math-language/inequalities/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---




# 不等号・不等式
「$a$ は $b$ より大きい」——この大小関係を表す記号が**不等号**です。

## このページで扱うこと
- 不等号の種類と意味
- 不等式を変形するときの注意点
- 一次不等式の解き方

## 前提知識
- [等号・等式](../equations/standard.md)
- [負数](../../numbers/negative-numbers/standard.md)

---

## 不等号の種類

| 記号 | 読み方 | 例 |
|------|--------|----|
| $a < b$ | $a$ は $b$ より小さい | $3 < 5$ |
| $a > b$ | $a$ は $b$ より大きい | $7 > 4$ |
| $a \leq b$ | $a$ は $b$ 以下 | $3 \leq 5$、$5 \leq 5$ |
| $a \geq b$ | $a$ は $b$ 以上 | $7 \geq 4$、$4 \geq 4$ |

$\leq$ は「$<$ または $=$」、$\geq$ は「$>$ または $=$」です。

---

## 不等式の変形ルール

**足す・引く**：両辺に同じ数を足しても引いても、不等号の向きは変わりません。

$$3 < 7 \implies 3 + 2 < 7 + 2 \quad (5 < 9)$$

**正の数で掛ける・割る**：向きは変わりません。

$$3 < 7 \implies 3 \times 2 < 7 \times 2 \quad (6 < 14)$$

**負の数で掛ける・割るときは向きが逆！**

$$3 < 7 \implies 3 \times (-2) > 7 \times (-2) \quad (-6 > -14)$$

これが不等式で最も大切な注意点です。

---

## 一次不等式の解き方

$$2x - 3 > 5$$

両辺に $3$ を足す：

$$2x > 8$$

両辺を $2$ で割る（正なので向き不変）：

$$x > 4$$

答えは「$x$ は $4$ より大きい数」——無限に多くの数が解になります。

---

## 解を数直線で表す

$$x > 4 \implies \text{数直線上の } 4 \text{ より右の部分}$$

```
----------------o==========>
         3   4   5   6   7
```

$\circ$（白丸）は「$4$ を含まない」を意味します。
$\leq$ の場合は $\bullet$（黒丸）で「$4$ を含む」を表します。

---

## 関連ページ

- [等号・等式](../equations/standard.md)
- [必要・十分条件](../conditions/standard.md)
- [不等号・不等式（発展）](../inequalities/advanced.md) — より詳しく学ぶ
