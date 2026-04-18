---
title: 分数
description: "有理数体の構成と性質"
goal: "同値類による有理数体の構成を説明でき、稠密性と可算性を証明できるようになる"
tags: [math,numbers,fractions]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 分数
    path: /math/numbers/fractions/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 分数（標準）
    path: /math/numbers/fractions/standard.md
  - title: 負数（専門）
    path: /math/numbers/integers/professional.md
  - title: 集合（入門）
    path: /math/foundations/sets/introduction.md
---

## 同値類による $\mathbb{Q}$ の構成

分数（標準）では $\frac{a}{b} = \frac{c}{d} \iff ad = bc$ を「等しさの条件」として使いました。ここではこれを厳密に構成します。

$\mathbb{Z} \times (\mathbb{Z} \setminus \{0\})$ 上の関係

$$(a, b) \sim (c, d) \iff ad = bc$$

が同値関係であることを確認します。

- 反射律：$ab = ba$（$\mathbb{Z}$ の乗法の交換法則）
- 対称律：$ad = bc \implies cb = da$
- 推移律：$(a,b) \sim (c,d)$ かつ $(c,d) \sim (e,f)$ のとき、$ad = bc$ かつ $cf = de$。$adf = bcf = bde$ であり $d \neq 0$ なので $af = be$、すなわち $(a,b) \sim (e,f)$。$\square$

$\mathbb{Q}$ をこの同値類全体の集合として定義し、$[(a,b)]$ を $\frac{a}{b}$ と書きます。

---

## 演算の定義とwell-defined性

$$[(a,b)] + [(c,d)] = [(ad+bc, bd)]$$
$$[(a,b)] \times [(c,d)] = [(ac, bd)]$$

これらが代表元の取り方によらないことを示す必要があります。

加法のwell-defined性：$(a,b) \sim (a',b')$ かつ $(c,d) \sim (c',d')$ とします。すなわち $ab' = a'b$ かつ $cd' = c'd$。$(ad+bc) \times b'd' = adb'd' + bcb'd'$ と $(a'd'+b'c') \times bd = a'd'bd + b'c'bd$。$adb'd' = a'b \cdot dd' = a'd' \cdot bd$ かつ $bcb'd' = b \cdot cd' \cdot b' = b \cdot c'd \cdot b' = b'c' \cdot bd$。よって等しい。$\square$

乗法も同様に確認できます。

---

## $\mathbb{Q}$ は体

$\mathbb{Q}$ は以下の性質を持ち、**体（field）**です。

- 加法について可換群：単位元 $\frac{0}{1}$、逆元 $-\frac{a}{b} = \frac{-a}{b}$
- 乗法について可換群（$0$ を除く）：単位元 $\frac{1}{1}$、逆元 $\left(\frac{a}{b}\right)^{-1} = \frac{b}{a}$（$a \neq 0$）
- 分配法則

$\mathbb{Z}$ は整域でしたが体ではありません（$2$ の乗法逆元 $\frac{1}{2}$ は $\mathbb{Z}$ に属しない）。$\mathbb{Q}$ は $\mathbb{Z}$ の**商体（field of fractions）**として得られます。これは整域から体を構成する一般的な方法です。

---

## 稠密性

**定理**：任意の $p, q \in \mathbb{Q}$（$p < q$）に対して、$p < r < q$ を満たす $r \in \mathbb{Q}$ が存在する。

証明：$r = \frac{p+q}{2}$ とおきます。$r \in \mathbb{Q}$（有理数は加法と $2$ による除法で閉じている）であり、$p < \frac{p+q}{2} < q$。$\square$

これを**稠密性**といいます。有理数はどこまでも「隙間なく」並んでいるように見えます。しかし、実数直線上には有理数では埋まらない「穴」が存在します（例：$\sqrt{2} \notin \mathbb{Q}$）。

---

## $\mathbb{Q}$ の可算性

**定理**：$\mathbb{Q}$ は可算集合である（$|\mathbb{Q}| = |\mathbb{N}|$）。

証明の概略：正の有理数 $\frac{a}{b}$（$a, b \in \mathbb{N}$、既約）を格子 $\mathbb{N} \times \mathbb{N}$ の点として表し、ジグザグに列挙します（カントールの対角線論法）。負の有理数と $0$ を交互に挟むと $\mathbb{Q}$ 全体の列挙が得られます。

一方、$\mathbb{R}$ はカントールの対角線論法により非可算です。よって $\mathbb{R} \setminus \mathbb{Q}$（無理数全体）も非可算です。有理数は稠密でありながら、実数直線の「ほとんど」を占めているのは無理数です。

---

## 関連ページ

- [分数（標準）](standard.md)
- [負数（専門）](../integers/professional.md)
- [集合（専門）](../../foundations/sets/professional.md)
- [数列（専門）](../../analysis/sequences/professional.md) — コーシー列による実数の構成