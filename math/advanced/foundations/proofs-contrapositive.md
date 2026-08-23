---
title: 対偶証明
description: "命題「PならばQ」と同値な対偶「QでないならPでない」を示す対偶証明の考え方を、xyが無理数ならばxまたはyが無理数であることの証明を例に扱う"
goal: "対偶証明の考え方を理解し、対偶を使った証明を書けるようになる"
tags: [math, foundations, proofs]
stage: advanced
subject: 基礎
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 応用編
    path: ../index.md
  - title: 対偶証明
    path: proofs-contrapositive.md
requires:
  - title: 証明法
    path: proofs.md
---

## 同値な対偶を示す

[必要・十分条件](logic.md)で見た通り、「$P$ ならば $Q$」と対偶「$\neg Q$（$Q$ でない）ならば $\neg P$（$P$ でない）」は同値です。$Q$ が「でない」という形で書きやすいときに使います。

**例題**：「実数 $x, y$ について、$xy$ が無理数ならば、$x$ または $y$ は無理数である」ことを証明する。

直接示そうとすると「$xy$ が無理数」という情報から $x, y$ 個別の性質を引き出しにくいので、対偶を考えます。「$x$ または $y$ は無理数である」の否定は「$x, y$ はともに（かつ）有理数である」なので、対偶は「$x, y$ がともに有理数ならば、$xy$ は有理数である」となり、こちらなら簡単です。

$x=\dfrac{p}{q}$、$y=\dfrac{r}{s}$（$p,q,r,s$ は整数、$q,s\neq0$）とおくと、$xy=\dfrac{pr}{qs}$ で有理数です。$\square$

---

## まとめ

対偶証明は、示したい命題の対偶（同値な命題）を代わりに示す方法です。結論を否定した形が扱いやすいときに有効です。

---

## 関連ページ

- [背理法](proofs-contradiction.md)
