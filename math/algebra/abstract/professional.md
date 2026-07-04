---
title: 抽象代数
description: "ガロア理論・加群・テンソル積"
goal: "ガロア対応の内容を述べ、加群とテンソル積の普遍性を説明できるようになる"
tags: [math,algebra,abstract]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 代数
    path: /math/algebra/index.md
  - title: 抽象代数
    path: /math/algebra/abstract/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 抽象代数（標準）
    path: /math/algebra/abstract/standard.md
  - title: 多項式（専門）
    path: /math/algebra/polynomials/professional.md
  - title: 集合（専門）
    path: /math/foundations/sets/professional.md
---

## 体の拡大

体 $F$ を含む体 $K$ を $F$ の**拡大体**、組 $K/F$ を**体の拡大**といいます。

$[K:F] = \dim_F K$（$F$ ベクトル空間としての次元）を**拡大次数**といいます。

**例**：$\mathbb{C}/\mathbb{R}$ は次数2の拡大。$\mathbb{Q}(\sqrt{2})/\mathbb{Q}$ も次数2。

**代数的元**：$F$ 係数多項式の根になる $K$ の元。すべての元が代数的な拡大を**代数拡大**といいます。

---

## ガロア理論

$K/F$ を有限次ガロア拡大（分離的かつ正規）とします。

**ガロア群** $\mathrm{Gal}(K/F)$：$F$ を固定する $K$ の自己同型の群。$|\mathrm{Gal}(K/F)| = [K:F]$。

**ガロア対応**（基本定理）：

$$\left\{K/F \text{ の中間体 } L\right\} \xleftrightarrow{1:1} \left\{\mathrm{Gal}(K/F) \text{ の部分群 } H\right\}$$

$L \mapsto \mathrm{Gal}(K/L)$、$H \mapsto K^H$（$H$ の固定体）が互いに逆の対応。

**応用**：$n$ 次方程式が根号で解けるための条件——ガロア群が可解群であること（アーベル＝ルフィニの定理の精密化）。5次以上の一般方程式は根号で解けない。

**参考文献**：Lang, S. (2002). *Algebra* (3rd ed.). Springer.

---

## 加群

環 $R$ 上の**左加群** $M$：アーベル群 $(M, +)$ に $R$ が左から作用する構造。

$$r(m + n) = rm + rn,\quad (r+s)m = rm + sm,\quad (rs)m = r(sm),\quad 1m = m$$

体 $F$ 上の加群 $=$ $F$ 上のベクトル空間。整数環 $\mathbb{Z}$ 上の加群 $=$ アーベル群。

**自由加群**：$\mathbb{Z}^n$ のように基底を持つ加群。

**有限生成アーベル群の分類定理**：任意の有限生成アーベル群は $\mathbb{Z}^r \oplus \mathbb{Z}/n_1\mathbb{Z} \oplus \cdots \oplus \mathbb{Z}/n_k\mathbb{Z}$（$n_1 \mid n_2 \mid \cdots \mid n_k$）と同型。

---

## テンソル積

$R$-加群 $M, N$ の**テンソル積** $M \otimes_R N$ は次の普遍性で特徴づけられます：

任意の $R$-双線形写像 $\phi: M \times N \to P$ は $M \otimes_R N \to P$ を経由する一意の線形写像に分解されます。

$$\mathrm{Hom}_R(M \otimes_R N, P) \cong \mathrm{BiHom}_R(M \times N, P)$$

ベクトル空間では $\dim(V \otimes W) = \dim V \cdot \dim W$。

テンソル積は多重線形代数・微分幾何（テンソル場）・量子力学（複合系の状態空間）の基礎です。

**参考文献**：Atiyah, M. F. & Macdonald, I. G. (1969). *Introduction to Commutative Algebra*. Addison-Wesley.

---

## 関連ページ

- [抽象代数（標準）](standard.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
- [多項式（専門）](../polynomials/professional.md)
