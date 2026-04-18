---
title: 対数関数
description: "「何乗すれば？」という問いへの答え"
goal: "対数関数の基本的なアイデアと必要性を日常的な例を使って説明できるようになる"
tags: [math,functions,logarithmic]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数
    path: /math/analysis/index.md
  - title: 対数関数
    path: /math/specific-functions/logarithmic/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 指数関数
    path: /math/specific-functions/exponential/introduction.md
---

## 「何乗すると…になるか」を求める

$2^3 = 8$ はわかります。では逆に「2を何乗すると8になるか？」——答えは3です。

このように「何乗すると指定の数になるか」を求める操作が**対数**です。指数関数の逆の操作にあたります。

$$\log_2 8 = 3 \quad \text{「$2$ を底とする $8$ の対数は $3$」}$$

---

## 掛け算を足し算に変える

対数の一番強力な性質は「掛け算を足し算に変換できる」ことです。

$$\log_2 (8 \times 4) = \log_2 8 + \log_2 4 = 3 + 2 = 5$$

電卓がなかった時代、天文学者たちは惑星の軌道を計算するために何十桁もの数を掛け合わせる必要がありました。対数を使えば、それが足し算に変換できる——対数表はそのための道具でした。

---

## 大きな範囲をコンパクトに表す

地震のマグニチュードは対数スケールです。マグニチュードが1増えると、エネルギーは約32倍になります。もし「エネルギーをそのまま」グラフに描いたら、小さな地震と大きな地震を同じ図に収めることはできません。対数を使うことで、非常に広い範囲を扱いやすい尺度に収められます。

---

## まとめ

対数は指数関数の逆操作です。「掛け算を足し算に変換する」という強力な性質があり、歴史的には計算を劇的に簡単にするための道具として使われました。現代でも、非常に広い範囲の量（音の強さ、地震のエネルギー、酸性度など）を表すスケールとして使われます。

---

## 関連ページ

- [指数関数（入門）](../exponential/introduction.md)
