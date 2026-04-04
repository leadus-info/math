---
title: 多角形
description: "n 辺で囲まれた図形の一般論"
tags: [math,geometry,polygon]
hierarchy:
  - title: 数学
    url: /math/index.html
  - title: 幾何
    url: /math/geometry/index.html
  - title: 多角形
    url: /math/geometry/polygon/standard.html
levels:
  - level: introduction
    url: introduction.html
  - level: standard
  - level: professional
    url: professional.html
level: standard
requires:
  - title: 三角形
    url: professional.md
  - title: 四角形
    url: professional.md
  - title: 三角関数
    url: professional.md
---



3 辺以上の直線で囲まれた図形が**多角形**です。

## このページで扱うこと
- 内角・外角の和
- 対角線の本数
- 正多角形の面積

---

## 内角の和

$n$ 角形の内角の和：$(n-2) \times 180°$

| $n$ | 内角の和 |
|-----|---------|
| 3 | $180°$ |
| 4 | $360°$ |
| 5 | $540°$ |
| 6 | $720°$ |

---

## 外角の和

$$360°$$（$n$ の値によらず一定）

---

## 対角線の本数

$$\frac{n(n-3)}{2}$$

---

## 正多角形の 1 つの内角

$$\frac{(n-2) \times 180°}{n}$$

---

## 正多角形の面積

外接円の半径を $R$ とすると：

$$S = \frac{1}{2}nR^2\sin\frac{360°}{n}$$

$n \to \infty$ で $\pi R^2$（円の面積）に近づきます。

---

## 関連ページ

- [円](professional.md)
- [場合の数](professional.md)
- [多角形（専門）](professional.md)
