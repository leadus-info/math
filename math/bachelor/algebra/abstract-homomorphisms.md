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

- **核**：$\ker \varphi = \{g \in G : \varphi(g) = e_H\}$（正規部分群。後述の補題(c)で証明）
- **像**：$\mathrm{Im}\, \varphi = \{\varphi(g) : g \in G\}$（$H$ の部分群。後述の補題(d)で証明）

全単射な準同型を**同型**（$G \cong H$）といい、同型な群は元の呼び方の違いを除いて全く同じ演算構造を持つため、代数的に区別できません。

**補題（準同型の基本性質）**：群準同型 $\varphi: G \to H$ について次が成り立ちます。

(a) $\varphi(e_G) = e_H$

(b) 任意の $g \in G$ に対し $\varphi(g^{-1}) = \varphi(g)^{-1}$

(c) $\ker\varphi$ は $G$ の正規部分群である

(d) $\mathrm{Im}\,\varphi$ は $H$ の部分群である

(e) $\ker\varphi = \{e_G\}$ ならば $\varphi$ は単射である

**証明**：(a) $\varphi(e_G) = \varphi(e_G e_G) = \varphi(e_G)\varphi(e_G)$ なので、両辺に左から $\varphi(e_G)^{-1}$ を掛けると $e_H = \varphi(e_G)$。

(b) (a)より $\varphi(g)\varphi(g^{-1}) = \varphi(gg^{-1}) = \varphi(e_G) = e_H$。よって $\varphi(g^{-1})$ は $\varphi(g)$ の逆元、すなわち $\varphi(g^{-1}) = \varphi(g)^{-1}$。

(c) (a)より $e_G \in \ker\varphi$。$k_1, k_2 \in \ker\varphi$ ならば $\varphi(k_1 k_2) = \varphi(k_1)\varphi(k_2) = e_H$ なので演算で閉じ、$k \in \ker\varphi$ ならば(b)より $\varphi(k^{-1}) = \varphi(k)^{-1} = e_H$ なので逆元も含みます。以上より $\ker\varphi$ は部分群です。

正規性については、任意の $g \in G$、$k \in \ker\varphi$ に対して $\varphi(gkg^{-1}) = \varphi(g)\varphi(k)\varphi(g)^{-1} = \varphi(g)\varphi(g)^{-1} = e_H$（補題(b)を使用）となるので $gkg^{-1} \in \ker\varphi$、すなわち $g(\ker\varphi)g^{-1} \subseteq \ker\varphi$ が任意の $g$ について成り立ちます。

逆の包含も示します。この包含関係は任意の $g$ について成り立つので、$g$ の代わりに $g^{-1}$ を代入すると $g^{-1}(\ker\varphi)g \subseteq \ker\varphi$ が得られます。この両辺に左から $g$ を、右から $g^{-1}$ を掛けると $g\bigl(g^{-1}(\ker\varphi)g\bigr)g^{-1} \subseteq g(\ker\varphi)g^{-1}$ となります。ここで左辺は、結合律による組み替えと $gg^{-1}=e$ を用いて $g\bigl(g^{-1}(\ker\varphi)g\bigr)g^{-1} = (gg^{-1})(\ker\varphi)(gg^{-1}) = e(\ker\varphi)e = \ker\varphi$ と簡単になるので、$\ker\varphi \subseteq g(\ker\varphi)g^{-1}$ が得られます。

この両方の包含 $g(\ker\varphi)g^{-1} \subseteq \ker\varphi$ と $\ker\varphi \subseteq g(\ker\varphi)g^{-1}$ から $g(\ker\varphi)g^{-1} = \ker\varphi$ となるので、$\ker\varphi$ は $G$ の正規部分群です。

(d) (a)より $e_H \in \mathrm{Im}\,\varphi$。$\varphi(g_1), \varphi(g_2) \in \mathrm{Im}\,\varphi$ ならば $\varphi(g_1)\varphi(g_2) = \varphi(g_1 g_2) \in \mathrm{Im}\,\varphi$ なので演算で閉じ、(b)より $\varphi(g)^{-1} = \varphi(g^{-1}) \in \mathrm{Im}\,\varphi$ なので逆元も含みます。以上より $\mathrm{Im}\,\varphi$ は $H$ の部分群です。

(e) $\varphi(a) = \varphi(b)$ とすると、(b)より $\varphi(ab^{-1}) = \varphi(a)\varphi(b)^{-1} = e_H$ なので $ab^{-1} \in \ker\varphi = \{e_G\}$、すなわち $a = b$。したがって $\varphi$ は単射です。$\blacksquare$

**準同型定理（第一同型定理）**：$G / \ker \varphi \cong \mathrm{Im}\, \varphi$

**証明**：$K = \ker\varphi$ とします。上の補題(c)より $K$ は $G$ の正規部分群なので、商群 $G/K$ が矛盾なく定義されます。写像 $\psi: G/K \to \mathrm{Im}\,\varphi$ を $\psi(gK) = \varphi(g)$ で定義します。

*well-defined性*：$gK = g'K$ ならば $g^{-1}g' \in K$、すなわち $\varphi(g^{-1}g') = e_H$。上の補題(b)より $\varphi(g^{-1}) = \varphi(g)^{-1}$ なので $\varphi(g)^{-1}\varphi(g') = e_H$ となり $\varphi(g) = \varphi(g')$。したがって $\psi$ は代表元の取り方によらず定まります。

*準同型であること*：$\psi((gK)(g'K)) = \psi(gg'K) = \varphi(gg') = \varphi(g)\varphi(g') = \psi(gK)\psi(g'K)$。

*単射性*：$\psi(gK) = e_H$ とすると $\varphi(g) = e_H$、すなわち $g \in K$。これは $gK = K$（$G/K$ の単位元）を意味するので、$\ker\psi = \{K\}$（$G/K$ の単位元のみ）です。$\psi$ が準同型であることは既に示した通りなので、上の補題(e)を $\psi$ に適用すると $\psi$ は単射です。

*全射性*：$\mathrm{Im}\,\varphi$ の任意の元は、ある $g \in G$ を用いて $\varphi(g)$ と書けるので、$\psi(gK) = \varphi(g)$ よりその元は $\psi$ の像に含まれます。

以上より $\psi$ は全単射な準同型、すなわち同型なので $G/K \cong \mathrm{Im}\,\varphi$。$\blacksquare$

---

## 巡回群の分類

1つの元 $g$ で生成される群 $\langle g \rangle = \{g^n \mid n \in \mathbb{Z}\}$ を**巡回群**といいます。

元 $g \in G$ の**位数**とは、$g^n = e$ となる最小の正の整数 $n$ のことをいいます（そのような $n$ が存在しない場合、$g$ の位数は無限であるといいます）。有限群 $G$ に対しては、その要素数 $|G|$ のことも**位数**（$G$ の位数）といいます。次の命題における「位数 $n$ の巡回群」は、この群の位数の意味です。

**命題**：位数 $n$ の有限巡回群は $\mathbb{Z}/n\mathbb{Z}$ と、無限巡回群は $\mathbb{Z}$ と同型である。

**証明**：$G = \langle g \rangle$ とし、写像 $\varphi: \mathbb{Z} \to G$ を $\varphi(k) = g^k$ で定めます。指数法則 $g^{k+l} = g^k g^l$ より $\varphi$ は準同型です。$G$ は $g$ で生成されるので $\varphi$ は全射（$\mathrm{Im}\,\varphi = G$）。

$\ker\varphi = \{k \in \mathbb{Z} \mid g^k = e\}$ は（上の補題(c)より）$\mathbb{Z}$ の部分群なので、ある $m \geq 0$ を用いて $m\mathbb{Z}$ の形になります（$\mathbb{Z}$ の部分群がすべてこの形であることは、割り算の原理から従います）。

- $m = 0$（$\ker\varphi = \{0\}$）のとき：上で証明した準同型定理より $\mathbb{Z}/\{0\} \cong G$、すなわち $\mathbb{Z} \cong G$。これは $g$ の位数が無限である場合に対応します。
- $m = n > 0$ のとき：準同型定理より $\mathbb{Z}/n\mathbb{Z} \cong G$。同型な群同士は要素数が等しいので $|G| = |\mathbb{Z}/n\mathbb{Z}| = n$、すなわち $G$ の位数（群の位数）は $n$ です。また、$\ker\varphi = n\mathbb{Z} = \{\ldots, -2n, -n, 0, n, 2n, \ldots\}$ の正の元のうち最小のものは $n$ 自身です。$\ker\varphi = \{k \in \mathbb{Z} \mid g^k = e\}$ であったことを思い出すと、これは「$g^k=e$ となる正の整数 $k$ のうち最小のものが $n$」であること、すなわち $n$ が $g$ の位数（元の位数）に一致することを意味します。

いずれの場合も、準同型定理を使うだけで巡回群の分類が直ちに従います。$\blacksquare$

---

## さらに進んだ話題

体 $F$ を含む体 $K$ を**拡大体**といいます。$K$ を $F$ 上のベクトル空間とみなしたときの次元を $[K:F]$ と書き、**拡大次数**といいます。$K/F$ が有限次ガロア拡大のとき、$F$ を固定する $K$ の自己同型のなす**ガロア群** $\mathrm{Gal}(K/F)$ が定まり、次の対応が成り立ちます（**ガロア理論の基本定理**）。

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
