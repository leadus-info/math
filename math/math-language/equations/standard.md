---
title: 等号・等式
description: "「等しい」を記号で表す"
tags: [math,math-language,equations]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数学の言語
    path: /math/math-language/index.md
  - title: 等号・等式
    path: /math/math-language/equations/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 乗法・べき乗
    path: /math/numbers/arithmetic/introduction.md
---



## このページで扱うこと

「左と右が同じ量である」ことを $=$ という記号で表します。
これが**等号**、$=$ を含む式が**等式**です。

- 等号の意味と性質
- 恒等式と方程式の違い
- 一次・二次方程式の解き方

---

## 等号とは

$$3 + 4 = 7$$

左辺と右辺が等しいことを表します。

| 性質 | 意味 | 例 |
|------|------|----|
| 反射律 | 自分自身と等しい | $a = a$ |
| 対称律 | 左右を入れ替えてよい | $a = b \Rightarrow b = a$ |
| 推移律 | 間をはしごできる | $a=b,\ b=c \Rightarrow a=c$ |

---

## 等式の変形ルール

両辺に同じ操作をしても等号は保たれます。

$$a = b \Rightarrow a + c = b + c$$
$$a = b \Rightarrow a \times c = b \times c$$

---

## 恒等式と方程式

**恒等式**：どんな値でも成り立つ

$$(x + 1)^2 = x^2 + 2x + 1$$

**方程式**：特定の値のときだけ成り立つ

$$x^2 = 4 \implies x = 2 \text{ または } x = -2$$

---

## 一次方程式

$$2x + 3 = 7 \implies 2x = 4 \implies x = 2$$

---

## 二次方程式の解の公式

$$ax^2 + bx + c = 0 \implies x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

| 判別式 $b^2 - 4ac$ | 解の個数 |
|-------------------|---------|
| 正 | 2 個 |
| 0 | 1 個（重解） |
| 負 | 実数解なし |

---

## 関連ページ

- [不等号・不等式](professional.md)
- [代数](professional.md)
- [等号・等式（専門）](professional.md)
