---
title: 抽象代数
description: "演算の構造を公理から分析する"
goal: "群・環・体を公理から定義し、部分群・準同型・商群の基本定理を理解して、ガロア理論などのより進んだ話題の見取り図を説明できるようになる"
tags: [math, algebra, abstract]
stage: 発展編
subject: 代数
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 発展編
    path: /math/bachelor/index.md
  - title: 抽象代数
    path: /math/bachelor/algebra/abstract.md
requires:
  - title: 多項式
    path: /math/advanced/algebra/polynomials.md
  - title: 集合
    path: /math/advanced/foundations/sets.md
---

## 演算の「共通する性質」を探す

整数の足し算と、時計の数字の足し算（12時の1時間後は1時）——これらは見た目が違いますが、「演算の結果がまた同じ集合に属する」「単位元がある」という共通の性質を持っています。抽象代数は「どんな対象かに関わらず、演算の性質だけを取り出して研究する」学問です。「体であれば成り立つ定理」を1回証明すれば、$\mathbb{Q}, \mathbb{R}, \mathbb{C}$ などすべての体に自動的に適用できます。

---

## 群の定義

集合 $G$ と二項演算 $\cdot: G \times G \to G$ の組 $(G, \cdot)$ が**群**であるとは、次の3条件を満たすことです。

1. **結合律**：$(a \cdot b) \cdot c = a \cdot (b \cdot c)$
2. **単位元**：$e \cdot a = a \cdot e = a$ を満たす $e \in G$ が存在する
3. **逆元**：各 $a$ に対し $a \cdot a^{-1} = a^{-1} \cdot a = e$ を満たす $a^{-1}$ が存在する

$a \cdot b = b \cdot a$ が成り立つとき**可換群**（アーベル群）といいます。

| 群 | 演算 | 単位元 |
|----|------|--------|
| $(\mathbb{Z}, +)$ | 足し算 | $0$ |
| $(\mathbb{Q}\setminus\{0\}, \times)$ | 掛け算 | $1$ |
| $(\mathbb{Z}/n\mathbb{Z}, +)$ | 剰余の足し算 | $[0]$ |

---

## 部分群と剰余類

$H \subset G$ が $G$ の**部分群**であるとは、$H$ 自身が $G$ の演算のもとで群をなすことです。

**ラグランジュの定理**：有限群 $G$ の部分群 $H$ について、$|H|$ は $|G|$ を割り切る。

$a \in G$ に対する $H$ の**左剰余類**を $aH = \{ah \mid h \in H\}$ で定義します。$H$ が $G$ の**正規部分群**（$gHg^{-1} = H$、$\forall g$）のとき、剰余類全体 $G/H$ が自然に群をなします（**商群**）。

---

## 環と体

群に2つ目の演算（掛け算）を加えた構造が**環**、さらに $0$ 以外の全要素に乗法逆元がある可換環が**体**です。

**環** $(R, +, \cdot)$：$(R, +)$ が可換群、$\cdot$ について結合律・分配律が成立。

**整域**：零因子を持たない可換単位環（$ab=0 \Rightarrow a=0$ または $b=0$）。

$$\text{体} \subset \text{整域} \subset \text{可換環} \subset \text{環}$$

整数 $\mathbb{Z}$ は環（割り算はできないことがある）、有理数 $\mathbb{Q}$・実数 $\mathbb{R}$・複素数 $\mathbb{C}$ は体（自由に四則演算できる）です。

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

抽象代数は、集合と演算の組が満たす公理（結合律・単位元・逆元など）だけに注目することで、整数・有理数・多項式・行列など見た目の異なる対象を統一的に扱います。群・環・体という段階的な構造の中で、部分群・商群・準同型といった道具立てが共通して使われます。

---

## 関連ページ

- [多項式（応用編）](/math/advanced/algebra/polynomials.md)
- [位相幾何学（発展編）](/math/bachelor/geometry/topology.md)
