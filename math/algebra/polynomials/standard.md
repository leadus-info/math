---
title: 多項式
description: "べき乗の和で表される関数"
goal: "多項式の定義・主要な定理・代表的な計算を理解し、後続のトピックに進める基礎を身につける"
tags: [math,algebra,polynomials]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/analysis/index.md
  - title: 多項式
    path: /math/algebra/polynomials/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 二次関数
    path: /math/specific-functions/quadratic/introduction.md
  - title: 代数
    path: /math/algebra/expressions/introduction.md
  - title: 微分
    path: /math/analysis/derivatives/introduction.md
---

## 多項式の定義

**定義**：$a_n x^n + a_{n-1} x^{n-1} + \cdots + a_1 x + a_0$（$a_n \neq 0$）を**$n$ 次多項式**といいます。$n$ を**次数**、$a_k$ を**係数**、$a_n$ を**最高次係数**といいます。

---

## 根と因数定理

$f(\alpha) = 0$ となる $\alpha$ を $f$ の**根**（零点）といいます。

**定理（因数定理）**：$f(\alpha) = 0 \iff f(x) = (x - \alpha) \cdot g(x)$ となる多項式 $g(x)$ が存在する。

**例**：$f(x) = x^2 - 5x + 6$ において $f(2) = 4-10+6 = 0$、$f(3) = 9-15+6 = 0$。

よって $f(x) = (x-2)(x-3)$。

---

## 代数学の基本定理

**定理**：複素数係数の $n$ 次多項式（$n \geq 1$）は、$\mathbb{C}$ 内に重複を込めてちょうど $n$ 個の根を持つ。

実係数多項式の実数根は「$n$ 個以下」ですが、複素数まで含めると必ず $n$ 個あります。これが「根は複素数の世界で完結する」理由です。

---

## 微分・積分

$$\frac{d}{dx}x^n = nx^{n-1}, \qquad \int x^n\,dx = \frac{x^{n+1}}{n+1} + C \quad (n \neq -1)$$

---

## グラフの概形

- 次数 $n$ が偶数・最高次係数が正 → 両端が上（$\cup$ 形）
- 次数 $n$ が奇数・最高次係数が正 → 左下から右上へ
- 根の場所でグラフが $x$ 軸と交わる（奇数重根）または接する（偶数重根）

---

## 関連ページ

- [多項式（入門）](introduction.md)
- [代数（標準）](../expressions/standard.md)
- [複素数（標準）](../../numbers/complex-numbers/standard.md)
