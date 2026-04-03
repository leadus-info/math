---
title: 二次関数
description: "グラフが放物線になる関数"
difficulty: 1
tags: [math,functions,quadratic]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 二次関数
    href: /math/functions/quadratic/standard.html
levels:
  - text: 基礎
  - text: 発展
    href: advanced.html
  - text: 専門
    href: professional.html
---






# 二次関数
ボールを投げたときの軌跡、橋のアーチ——これらは**放物線**という曲線です。
$x^2$ を含む関数のグラフがこの形になります。

## このページで扱うこと
- 二次関数の基本形と頂点形式
- グラフの特徴（開く向き・頂点・軸）
- 判別式と $x$ 軸との交点

## 前提知識
- [一次関数](../linear/standard.md)
- [代数](../../math-language/algebra/standard.md)

---

## 二次関数とは？

$$f(x) = ax^2 + bx + c \quad (a \neq 0)$$

- $a > 0$：下に開く放物線（$\cup$ の形）
- $a < 0$：上に開く放物線（$\cap$ の形）
- $|a|$ が大きいほど細い放物線

---

## 頂点形式（平方完成）

$$f(x) = a(x - p)^2 + q$$

- **頂点**：$(p,\ q)$（山の頂上 or 谷の底）
- **軸**：$x = p$（放物線の左右対称の直線）

**平方完成の例**：

$$x^2 + 4x + 1 = (x + 2)^2 - 4 + 1 = (x+2)^2 - 3$$

→ 頂点は $(-2,\ -3)$

**頂点を公式で求めると**：$p = -\dfrac{b}{2a}$

---

## $x$ 軸との交点（判別式）

$ax^2 + bx + c = 0$ の解の個数は**判別式** $D = b^2 - 4ac$ で決まります。

| $D$ | 意味 | グラフ |
|-----|------|--------|
| $D > 0$ | 実数解が $2$ 個 | $x$ 軸と $2$ 点で交わる |
| $D = 0$ | 実数解が $1$ 個（重解） | $x$ 軸にちょうど接する |
| $D < 0$ | 実数解なし | $x$ 軸と交わらない |

---

## 解の公式

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

---

## 関連ページ

- [一次関数](../linear/standard.md)
- [多項式](../polynomials/standard.md)
- [二次関数（発展）](../quadratic/advanced.md) — より詳しく学ぶ
