---
title: 極限の厳密な定義
description: "関数や数列の極限をε-δ論法・ε-N論法で厳密に定義し、収束の証明の書き方、点収束と一様収束の違い、コーシー列による収束判定を解説する"
goal: "極限をε-δ論法で厳密に定義し、収束の証明を書けるようになり、一様収束とコーシー列による収束判定を説明できるようになる"
tags: [math, analysis, limits]
stage: bachelor
subject: 解析
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 発展編
    path: ../index.md
  - title: 極限の厳密な定義
    path: epsilon-delta.md
requires:
  - title: 極限
    path: ../../advanced/analysis/limits.md
  - title: 実数
    path: ../numbers/real-numbers.md
---

## 「近づく」を数式にする

応用編の「極限」では、$x$ を $a$ に近づけたときの $f(x)$ の行き先を直感的に扱いました。しかし「近づく」という言葉のままでは、証明の道具として使うには曖昧です。ここでは、この直感を不等式だけで表現する**ε-δ論法**を導入します。

---

## 関数の極限の厳密な定義

**定義**：$\displaystyle\lim_{x\to a} f(x) = L$ とは、

$$\forall \varepsilon > 0,\ \exists \delta > 0 \text{ s.t. } 0 < |x - a| < \delta \Rightarrow |f(x) - L| < \varepsilon$$

が成り立つことです。ここで s.t. は "such that" の略で、「〜を満たす」という意味です。「$f(x)$ を $L$ にどれだけ近づけたいか（$\varepsilon$）」を先に指定させ、それに応じて「$x$ を $a$ にどれだけ近づければよいか（$\delta$）」を答えられれば、極限が存在するとみなします。

**証明例**：$\displaystyle\lim_{x\to 3}(2x - 1) = 5$ を示す。$|2x-1-5| = 2|x-3| < \varepsilon$ としたいので、$|x-3| < \varepsilon/2$ ととればよい。よって $\delta = \varepsilon/2$ とおく。実際、$0 < |x-3| < \delta$ ならば $|(2x-1)-5| = 2|x-3| < 2\delta = \varepsilon$ となり、定義が満たされる。$\square$

---

## 数列の極限の厳密な定義

**定義**：$\displaystyle\lim_{n\to\infty} a_n = L$ とは、

$$\forall \varepsilon > 0,\ \exists N \in \mathbb{N} \text{ s.t. } n > N \Rightarrow |a_n - L| < \varepsilon$$

が成り立つことです。「どんな精度 $\varepsilon$ を要求されても、十分先の項からはその精度で $L$ に収まる」という意味です。

---

## 点収束と一様収束

関数列 $\{f_n\}$ の収束には2種類あります。

**点収束**：各 $x$ で $\lim_{n\to\infty} f_n(x) = f(x)$

**一様収束**：$\sup_x |f_n(x) - f(x)| \to 0$

一様収束は「収束のスピードが全点で均一」であることを意味し、一様収束のもとでは連続性・積分・微分と極限の交換が正当化されます。

**例（点収束だが一様収束しない）**：$f_n(x) = x^n$ を $[0,1]$ で考えると、各点では $0$ か $1$ に収束しますが、$x=1$ 付近での収束が遅くなるため一様には収束しません。

---

## コーシーの収束判定

数列がどんな値に収束するかを知らなくても、収束するかどうかだけを判定する方法があります。

**定義**：$\{a_n\}$ が**コーシー列**であるとは、$\forall \varepsilon > 0,\ \exists N,\ m,n > N \Rightarrow |a_m - a_n| < \varepsilon$ が成り立つことです。

**定理（実数の完備性）**：実数列 $\{a_n\}$ が収束する $\iff$ $\{a_n\}$ がコーシー列である。

**証明（⟹方向）**：$\{a_n\}$ が $L$ に収束すると仮定します。任意の $\varepsilon>0$ に対し、収束の定義よりある $N$ が存在して $n>N \Rightarrow |a_n-L|<\varepsilon/2$。$m,n>N$ のとき、三角不等式より

$$|a_m-a_n| \leq |a_m-L|+|L-a_n| < \frac\varepsilon2+\frac\varepsilon2=\varepsilon$$

よって $\{a_n\}$ はコーシー列です。$\blacksquare$（逆方向「コーシー列ならば収束する」は実数の完備性公理そのものに相当し、実数の構成方法に依存する証明が必要になるため、実数に譲ります。）

この定理は実数で見た完備性の公理と表裏一体です。

**参考文献**：Rudin, W. (1976). *Principles of Mathematical Analysis* (3rd ed.). McGraw-Hill.

---

## まとめ

ε-δ論法は「限りなく近づく」という直感を、不等式だけを使った厳密な言葉に置き換えたものです。関数の極限・数列の極限がこの枠組みで定義され、点収束と一様収束の違い、コーシー列による収束判定が、極限の議論をより精密にします。

---

## 関連ページ

- [微分の厳密な定義](differentiability.md)
