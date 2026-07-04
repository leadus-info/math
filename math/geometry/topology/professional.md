---
title: 位相幾何学
description: "基本群・被覆空間・ホモロジー"
goal: "基本群の定義と計算方法を述べ、ホモロジー群の直感的な意味とオイラー標数との関係を説明できるようになる"
tags: [math,geometry,topology]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 幾何
    path: /math/geometry/index.md
  - title: 位相幾何学
    path: /math/geometry/topology/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 位相幾何学（標準）
    path: /math/geometry/topology/standard.md
  - title: 抽象代数（標準）
    path: /math/algebra/abstract/standard.md
  - title: 集合（専門）
    path: /math/foundations/sets/professional.md
---

## 基本群

基点付き位相空間 $(X, x_0)$ において、$x_0$ を基点とするループ（始点・終点が $x_0$ の連続曲線）のホモトピー類（連続変形で移り合うクラス）の全体が群をなします。これを**基本群** $\pi_1(X, x_0)$ といいます。

**群構造**：ループの連結（先に一方を走り、次に他方を走る）が積。

**例**：
- $\pi_1(\mathbb{R}^n, 0) = \{e\}$（自明群）——$\mathbb{R}^n$ はすべてのループが収縮可能
- $\pi_1(S^1, 1) \cong \mathbb{Z}$——円上のループは「何回巻くか」で分類
- $\pi_1(T^2) \cong \mathbb{Z} \times \mathbb{Z}$——トーラスは2方向への巻きつき
- $\pi_1(\mathbb{R}P^2) \cong \mathbb{Z}/2\mathbb{Z}$——射影平面

基本群は空間の「穴の形」（1次元的な穴）を検出します。

---

## 被覆空間

$p: \tilde{X} \to X$ が**被覆写像**であるとは：任意の点 $x \in X$ が開近傍 $U$ を持ち、$p^{-1}(U)$ が互いに素な開集合の合併で各成分が $U$ と同相なこと。

**例**：$p: \mathbb{R} \to S^1$、$p(t) = e^{2\pi it}$——実数直線は円の被覆空間。

**ガロア対応**（被覆空間論）：連結被覆空間は基本群の部分群と1対1に対応します（普遍被覆の場合 $\pi_1$ 全体に対応）。これは代数のガロア理論と平行した構造です。

---

## ホモロジー

基本群は1次元的な穴を検出しますが、高次元の穴（球面の「囲み」など）は検出できません。これを体系的に扱うのが**ホモロジー**です。

**特異ホモロジー群** $H_n(X)$（$n = 0, 1, 2, \ldots$）：$n$ 次元的な「サイクル（境界を持たないもの）」を「バウンダリ（何かの境界になるもの）」で割った群。

| 群 | 意味 |
|----|------|
| $H_0(X)$ | 連結成分の情報 |
| $H_1(X)$ | 1次元的な穴（基本群のアーベル化） |
| $H_2(X)$ | 2次元的な穴（囲まれた空洞） |

**例**：$H_n(S^k)$：$n = 0$ または $n = k$ のとき $\mathbb{Z}$、それ以外は $0$。

---

## オイラー標数とホモロジー

$$\chi(X) = \sum_{n=0}^{\infty} (-1)^n \mathrm{rank}(H_n(X))$$

ベッチ数 $b_n = \mathrm{rank}(H_n(X))$ による表示です。コンパクト曲面については：

$$\chi(\text{閉曲面}) = 2 - 2g \quad (g: \text{種数})$$

これがガウス＝ボネの定理 $\int_M K\,dA = 2\pi\chi(M)$ と結びつき、微分幾何・代数幾何・数論への深い接続をもたらします。

**参考文献**：Hatcher, A. (2002). *Algebraic Topology*. Cambridge University Press. (無料公開あり)

---

## 関連ページ

- [位相幾何学（標準）](standard.md)
- [集合（専門）](../../foundations/sets/professional.md)
- [抽象代数（専門）](../../algebra/abstract/professional.md)
