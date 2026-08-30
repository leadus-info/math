---
title: 準同型・同型
description: "群の構造を保つ写像である準同型・同型を定義し、核・像を用いて準同型定理を証明し、その応用として巡回群が整数全体またはnを法とする剰余類全体と同型であることを証明する。ガロア理論・加群・テンソル積という代数学のさらに進んだ話題への見取り図も示す"
goal: "準同型・同型を理解し、準同型定理を証明し、巡回群の分類を証明できるようになる"
tags: [math, algebra, abstract]
stage: bachelor
subject: 代数
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 準同型・同型
    path: abstract-homomorphisms.md
requires:
  - title: 群
    path: abstract-groups.md
  - title: 環と体
    path: abstract-rings-fields.md
  - title: 多項式
    path: ../../advanced/algebra/polynomials.md
---

## 準同型・同型・巡回群

**群準同型** $\varphi: G \to H$ とは $\varphi(ab) = \varphi(a)\varphi(b)$ を満たす写像です。

- **核**：$\ker \varphi = \{g \in G : \varphi(g) = e_H\}$（正規部分群）
- **像**：$\mathrm{Im}\, \varphi = \{\varphi(g) : g \in G\}$（$H$ の部分群）

全単射な準同型を**同型**（$G \cong H$）といい、同型な群は代数的に区別できません。

**準同型定理（第一同型定理）**：$G / \ker \varphi \cong \mathrm{Im}\, \varphi$

**証明**：$K = \ker\varphi$（正規部分群）とし、写像 $\psi: G/K \to \mathrm{Im}\,\varphi$ を $\psi(gK) = \varphi(g)$ で定義します。

*well-defined性*：$gK = g'K$ ならば $g^{-1}g' \in K$、すなわち $\varphi(g^{-1}g') = e_H$。よって $\varphi(g)^{-1}\varphi(g') = e_H$ となり $\varphi(g) = \varphi(g')$。したがって $\psi$ は代表元の取り方によらず定まります。

*準同型であること*：$\psi((gK)(g'K)) = \psi(gg'K) = \varphi(gg') = \varphi(g)\varphi(g') = \psi(gK)\psi(g'K)$。

*単射性*：$\psi(gK) = e_H$ とすると $\varphi(g) = e_H$、すなわち $g \in K$。これは $gK = K$（$G/K$ の単位元）を意味するので、$\psi$ の核は自明、したがって単射です。

*全射性*：$\mathrm{Im}\,\varphi$ の任意の元は、ある $g \in G$ を用いて $\varphi(g)$ と書けるので、$\psi(gK) = \varphi(g)$ よりその元は $\psi$ の像に含まれます。

以上より $\psi$ は全単射な準同型、すなわち同型なので $G/K \cong \mathrm{Im}\,\varphi$。$\blacksquare$

---

## 巡回群の分類

1つの元 $g$ で生成される群 $\langle g \rangle = \{g^n \mid n \in \mathbb{Z}\}$ を**巡回群**といいます。

**命題**：位数 $n$ の有限巡回群は $\mathbb{Z}/n\mathbb{Z}$ と、無限巡回群は $\mathbb{Z}$ と同型である。

**証明**：$G = \langle g \rangle$ とし、写像 $\varphi: \mathbb{Z} \to G$ を $\varphi(k) = g^k$ で定めます。指数法則 $g^{k+l} = g^k g^l$ より $\varphi$ は準同型です。$G$ は $g$ で生成されるので $\varphi$ は全射（$\mathrm{Im}\,\varphi = G$）。

$\ker\varphi = \{k \in \mathbb{Z} \mid g^k = e\}$ は $\mathbb{Z}$ の部分群なので、ある $m \geq 0$ を用いて $m\mathbb{Z}$ の形になります（$\mathbb{Z}$ の部分群がすべてこの形であることは、割り算の原理から従います）。

- $m = 0$（$\ker\varphi = \{0\}$）のとき：上で証明した準同型定理より $\mathbb{Z}/\{0\} \cong G$、すなわち $\mathbb{Z} \cong G$。これは $g$ の位数が無限である場合に対応します。
- $m = n > 0$ のとき：準同型定理より $\mathbb{Z}/n\mathbb{Z} \cong G$。この $n$ が $g$ の位数（$g^n=e$ となる最小の正の整数）に一致します。

いずれの場合も、準同型定理を使うだけで巡回群の分類が直ちに従います。$\blacksquare$

---

## さらに進んだ話題

体 $F$ を含む体 $K$ を**拡大体**といい、$[K:F]$（$F$ ベクトル空間としての $K$ の次元）を拡大次数といいます。$K/F$ が有限次ガロア拡大のとき、$F$ を固定する $K$ の自己同型のなす**ガロア群** $\mathrm{Gal}(K/F)$ が定まり、次の対応が成り立ちます（**ガロア理論の基本定理**）。

$$\{K/F \text{ の中間体}\} \xleftrightarrow{1:1} \{\mathrm{Gal}(K/F) \text{ の部分群}\}$$

この理論の帰結として、5次以上の一般方程式は根号で解けないことが示されます（ガロア群が可解群でないため）。

環 $R$ 上の**加群**は、体上の加群がベクトル空間、$\mathbb{Z}$ 上の加群がアーベル群という形で線形代数の考え方を一般化したものです。2つの加群の**テンソル積**は、双線型写像を線形写像に変換する普遍性によって特徴づけられ、量子力学や微分幾何で使われます。

**参考文献**：Lang, S. (2002). *Algebra* (3rd ed.). Springer.

---

## まとめ

準同型は群の構造を保つ写像で、$G/\ker\varphi \cong \mathrm{Im}\,\varphi$ という準同型定理は、$\psi(gK)=\varphi(g)$ がwell-defined・準同型・全単射であることを順に確かめることで証明できます。この定理を $\varphi(k)=g^k$ という準同型に適用するだけで、巡回群がすべて $\mathbb{Z}$ か $\mathbb{Z}/n\mathbb{Z}$ と同型であることが直ちに従います。ガロア理論・加群・テンソル積は、この構造の考え方をさらに発展させた話題です。

---

## 関連ページ

- [抽象代数](abstract.md)
