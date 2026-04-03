---
title: 分数（専門）
description: "有理数の代数的構造・稠密性・実数との対比"
difficulty: 4
tags: [math,numbers,fractions,professional]
hierarchy:
  - text: 数学
    href: /math/index.html
  - text: 数
    href: /math/numbers/index.html
  - text: 分数（専門）
    href: /math/numbers/fractions/professional.html
levels:
  - text: 基礎
    href: standard.html
  - text: 発展
    href: advanced.html
  - text: 専門
---








# 分数（発展）
有理数の代数的構造・稠密性・実数との距離について扱います。  
基礎は[分数（入門）](../fractions/standard.md)を参照してください。

## このページで扱うこと
- 同値類による $\mathbb{Q}$ の厳密な構成
- 有理数の稠密性と実数との差（$\mathbb{R} \setminus \mathbb{Q}$ の非可算性）
- $p$-進数への入口

## 前提知識
- [分数](../fractions/standard.md)
- [集合](../../math-language/sets/standard.md)
- [極限（専門）](../../functions/calculus/limits/professional.md)

---

## 同値類による $\mathbb{Q}$ の構成

整数の順序対 $(a, b)$（$b \neq 0$）に対して同値関係を定義します。

$$(a, b) \sim (c, d) \iff ad = bc$$

有理数 $\mathbb{Q}$ はこの同値類全体の集合であり、演算は

$$[(a,b)] + [(c,d)] = [(ad+bc, bd)], \quad [(a,b)] \cdot [(c,d)] = [(ac, bd)]$$

と定義されます。この構成により $\mathbb{Q}$ は**体（field）**となります。

---

## 稠密性

任意の二つの有理数 $p < q$ の間には別の有理数が存在します。

$$\frac{p + q}{2} \in \mathbb{Q}, \quad p < \frac{p+q}{2} < q$$

しかし実数直線上には有理数で埋まらない「隙間」があります。

---

## カントールの対角線論法と $|\mathbb{Q}| = |\mathbb{N}|$

$\mathbb{Q}$ は**可算**（$\mathbb{N}$ と1対1対応が存在）です。  
一方 $\mathbb{R}$ は非可算であるため $\mathbb{R} \setminus \mathbb{Q}$（無理数）は非可算。

**証明の概略**: $\mathbb{Q}$ を格子 $\mathbb{Z} \times \mathbb{N}$ の要素として表し、ジグザグに列挙します。

---

## $p$-進数への入口

素数 $p$ を法とする「近さ」を定義すると、通常とは異なる距離（$p$-進距離）が入ります。

$$|a - b|_p = p^{-v_p(a-b)}$$

この距離で完備化したものが**$p$-進数体** $\mathbb{Q}_p$ です。

---

## 関連ページ

- [分数](../fractions/standard.md)
- [集合（専門）](../../math-language/sets/professional.md)
- [数列（専門）](../../functions/sequences/professional.md) — コーシー列による実数の構成
