---
title: 不等号・不等式
description: "大小関係を記号で表す"
goal: "不等号の意味を理解し、不等式が「範囲」を表すことと、負の数を掛けると向きが逆転する理由を説明できるようになる"
tags: [math,algebra,inequalities]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 代数
    path: /math/algebra/index.md
  - title: 不等号・不等式
    path: /math/algebra/inequalities/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 等号・等式（入門）
    path: /math/algebra/equations/introduction.md
  - title: 負数（入門）
    path: /math/numbers/integers/introduction.md
---

## 「大きい」「小さい」を記号で表す

りんごが5個、みかんが3個——りんごの方が多いです。この大小関係を記号で表したのが**不等号**です。

$$5 > 3 \quad \text{（5は3より大きい）}$$
$$3 < 5 \quad \text{（3は5より小さい）}$$

「以上」「以下」は「等しい場合も含む」という意味です。

$$5 \geq 5 \quad \text{（5は5以上——等しいので成り立つ）}$$
$$3 \leq 4 \quad \text{（3は4以下）}$$

---

## 不等式の解は「範囲」

方程式 $x + 2 = 5$ の解は $x = 3$ という1つの値でした。

不等式 $x + 2 > 5$ を考えましょう。$x = 3$ のとき $3 + 2 = 5$ で $>5$ は満たしません。$x = 4$ のとき $4 + 2 = 6 > 5$ で満たします。$x = 100$ でも $100 + 2 = 102 > 5$ で満たします。

両辺から2を引くと $x > 3$——3より大きいすべての数が解です。

---

## 変形のルール

等式と同じように、両辺に同じ数を足したり引いたりしても不等号の向きは変わりません。

$$3 < 5 \implies 3 + 10 < 5 + 10 \quad (13 < 15)$$

正の数を掛けても変わりません。

$$3 < 5 \implies 3 \times 2 < 5 \times 2 \quad (6 < 10)$$

しかし**負の数を掛けると向きが逆転します**。

$$3 < 5 \implies 3 \times (-2) > 5 \times (-2) \quad (-6 > -10)$$

なぜか？数直線で $-1$ 倍すると左右が入れ替わるためです。$3$ は $-3$ に、$5$ は $-5$ に移ると、$-3$ は $-5$ より右（大きい）になります。

---

## まとめ

不等号は大小関係を表す記号で、不等式の解は1つの値でなく範囲になります。変形のとき、負の数を掛けると向きが逆転する点が等式と異なります。

---

## 関連ページ

- [等号・等式（入門）](../equations/introduction.md)
- [必要・十分条件（入門）](../../foundations/logic/introduction.md)
