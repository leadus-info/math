---
title: 代数
description: "抽象代数・環論・多項式環"
tags: [math,math-language,algebra]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数学の言語
    path: /math/math-language/index.md
  - title: 代数
    path: /math/math-language/algebra/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 代数
    path: /math/math-language/algebra/introduction.md
  - title: 四則演算（専門）
    path: ../../numbers/arithmetic/professional.md
  - title: 行列
    path: /math/linear-algebra/matrices/introduction.md
---

## 群・環・体

代数的構造の基本単位です。

**群 $(G, \cdot)$**：集合 $G$ と二項演算 $\cdot$ が結合律・単位元の存在・逆元の存在を満たす。

| 例 | 演算 | 群か |
|----|------|-----|
| $(\mathbb{Z}, +)$ | 加算 | ○（可換群） |
| $(\mathbb{Z}, \times)$ | 乗算 | ×（逆元なし） |
| $(\mathbb{Q}\setminus\{0\}, \times)$ | 乗算 | ○ |
| $(S_n, \circ)$ | 置換の合成 | ○（非可換） |

**環 $(R, +, \times)$**：$(R, +)$ が可換群で、$\times$ について結合律・分配律。

**体 $(F, +, \times)$**：$0$ 以外のすべての元が乗法逆元を持つ可換環。$\mathbb{Q}, \mathbb{R}, \mathbb{C}$ はすべて体。

---

## 多項式環

体 $F$ 上の多項式環 $F[x]$ は**主イデアル整域（PID）**です：\
すべてのイデアルが1つの元で生成されます。

$$F[x] \text{ の商体} = F(x) \text{（有理関数体）}$$

$F[x]/(f(x))$（$f$ が既約多項式のとき）は体の拡大になります。

**例**：$\mathbb{R}[x]/(x^2+1) \cong \mathbb{C}$\
実数の多項式環を $x^2+1$ で割ると複素数体が現れます。

---

## 準同型定理

群の準同型 $\varphi: G \to H$ に対して：

$$G / \ker(\varphi) \cong \text{Im}(\varphi)$$

**核（kernel）**：$\ker(\varphi) = \{g \in G : \varphi(g) = e_H\}$（正規部分群）

これはガロア理論・線形代数（核と像の定理）など広範に使われます。

---

## テンソル積

$R$-加群 $M, N$ のテンソル積 $M \otimes_R N$ は双線形写像の普遍対象：

$$\text{Hom}_R(M \otimes_R N, P) \cong \text{BiHom}_R(M \times N, P)$$

ベクトル空間では $\dim(V \otimes W) = \dim V \cdot \dim W$。

**参考文献**：Lang, S. (2002). *Algebra* (3rd ed.). Springer.

---

## 関連ページ

- [代数](standard.md)
- [行列（専門）](../../linear-algebra/matrices/professional.md)
- [等号・等式（専門）](../equations/professional.md)
