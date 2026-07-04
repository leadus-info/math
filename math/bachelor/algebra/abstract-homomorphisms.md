---
title: 準同型・同型
description: "群の構造を保つ写像と、より進んだ話題"
goal: "準同型・同型・巡回群を理解し、ガロア理論や加群など、より進んだ話題の見取り図を説明できるようになる"
tags: [math, algebra, abstract]
stage: 発展編
subject: 代数
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 準同型・同型
    path: abstract-homomorphisms.md
requires:
  - title: 環と体
    path: abstract-rings-fields.md
  - title: 多項式
    path: ../../advanced/algebra/polynomials.md
---

## 準同型・同型・巡回群

**群準同型** $\varphi: G \to H$ とは $\varphi(ab) = \varphi(a)\varphi(b)$ を満たす写像です。

- **核**：$\ker \varphi = \{g \in G : \varphi(g) = e_H\}$（正規部分群）
- **像**：$\mathrm{Im}\, \varphi = \{\varphi(g) : g \in G\}$（$H$ の部分群）

**準同型定理**：$G / \ker \varphi \cong \mathrm{Im}\, \varphi$

全単射な準同型を**同型**（$G \cong H$）といい、同型な群は代数的に区別できません。1つの元 $g$ で生成される群 $\langle g \rangle$ を**巡回群**といい、位数 $n$ の有限巡回群は $\mathbb{Z}/n\mathbb{Z}$ と、無限巡回群は $\mathbb{Z}$ と同型です。

---

## さらに進んだ話題

体 $F$ を含む体 $K$ を**拡大体**といい、$[K:F]$（$F$ ベクトル空間としての $K$ の次元）を拡大次数といいます。$K/F$ が有限次ガロア拡大のとき、$F$ を固定する $K$ の自己同型のなす**ガロア群** $\mathrm{Gal}(K/F)$ が定まり、次の対応が成り立ちます（**ガロア理論の基本定理**）。

$$\{K/F \text{ の中間体}\} \xleftrightarrow{1:1} \{\mathrm{Gal}(K/F) \text{ の部分群}\}$$

この理論の帰結として、5次以上の一般方程式は根号で解けないことが示されます（ガロア群が可解群でないため）。

環 $R$ 上の**加群**は、体上の加群がベクトル空間、$\mathbb{Z}$ 上の加群がアーベル群という形で線形代数の考え方を一般化したものです。2つの加群の**テンソル積**は、双線型写像を線形写像に変換する普遍性によって特徴づけられ、量子力学や微分幾何で使われます。

**参考文献**：Lang, S. (2002). *Algebra* (3rd ed.). Springer.

---

## まとめ

準同型は群の構造を保つ写像で、準同型定理により核と像の関係が明らかになります。巡回群はすべて $\mathbb{Z}$ か $\mathbb{Z}/n\mathbb{Z}$ と同型です。ガロア理論・加群・テンソル積は、この構造の考え方をさらに発展させた話題です。

---

## 関連ページ

- [抽象代数（発展編）](abstract.md)
