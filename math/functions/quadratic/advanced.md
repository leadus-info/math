---
title: 二次関数（発展）
description: "放物線を描く関数（発展）"
difficulty: 2
tags: [math,functions,quadratic,advanced]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 関数
    href: /math/functions/index.html
  - text: 二次関数（発展）
    href: /math/functions/quadratic/advanced.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
  - text: 専門
    href: professional.html
---







# 二次関数
$x^2$ を含む関数で、グラフは**放物線**になります。
ボールの軌跡や橋のアーチがこの形です。

## このページで扱うこと
- 二次関数の標準形と頂点形式
- 放物線のグラフの特徴
- 二次方程式との対応

## 前提知識
- [一次関数](professional.md)
- [代数](professional.md)

---

## 定義

$$f(x) = ax^2 + bx + c \quad (a \neq 0)$$

- $a > 0$：下に開く（$\cup$ 形）
- $a < 0$：上に開く（$\cap$ 形）

---

## 頂点形式（平方完成）

$$f(x) = a(x - p)^2 + q$$

- **頂点**：$(p,\ q)$（最大値または最小値の点）
- **軸**：$x = p$

**平方完成の例**：

$$x^2 + 4x + 1 = (x + 2)^2 - 3 \implies \text{頂点 }(-2,\ -3)$$

---

## 頂点の座標

$$p = -\frac{b}{2a}, \qquad q = f(p)$$

---

## $x$ 軸との交点（判別式）

$$D = b^2 - 4ac$$

| $D$ | $x$ 軸との関係 |
|-----|--------------|
| $D > 0$ | 2 点で交わる |
| $D = 0$ | 1 点で接する |
| $D < 0$ | 交わらない |

---

## 二次不等式

$a > 0$、$D > 0$（解を $\alpha < \beta$）のとき：

$$f(x) < 0 \iff \alpha < x < \beta$$
$$f(x) > 0 \iff x < \alpha \text{ または } x > \beta$$

---

## 関連ページ

- [多項式](professional.md)
- [微分](professional.md) — 頂点は $f'(x) = 0$ の点
- [二次関数（専門）](professional.md) — 二次形式・円錐曲線
