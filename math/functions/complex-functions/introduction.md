---
title: 複素関数
description: "複素数を変数にとる関数"
goal: "複素関数の基本的なアイデアと必要性を日常的な例を使って説明できるようになる"
tags: [math,functions,calculus]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数の操作
    path: /math/functions/index.md
  - title: 複素関数
    path: /math/functions/complex-functions/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 複素数
    path: /math/numbers/complex-numbers/introduction.md
  - title: 微分
    path: /math/functions/derivatives/introduction.md
---

## 関数の「入力」を複素数にする

$f(x) = x^2$ では実数 $x$ を入れて実数が出ました。では、$x$ の代わりに複素数 $z = a + bi$ を入れたらどうなるでしょう？

$$f(z) = z^2 = (a + bi)^2 = a^2 - b^2 + 2abi$$

これも複素数になります。このように「複素数を入れて複素数が出る」関数を**複素関数**といいます。

---

## 実数の関数との違い

実数の関数は「数直線から数直線への対応」です。グラフを2次元の平面に描けます。

複素関数は「複素平面（2次元）から複素平面（2次元）への対応」なので、グラフを描こうとすると4次元が必要になります。そのため、複素関数は「ある領域の形が別の形にどう変換されるか」として視覚化することが多いです。

---

## 驚くほど良い性質

複素関数の中でも「どの方向から見ても微分できる（正則）」ものは、実数の関数にはない強力な性質を持ちます。

ある点の近くの様子だけで、関数全体の振る舞いが決まってしまう——「部分を知れば全体がわかる」という、実数では成り立たない性質が生まれます。

---

## 応用

- 流体力学（水や空気の流れ）
- 電気工学（交流回路の解析）
- 信号処理

複素関数は理論的な美しさだけでなく、工学の実践でも欠かせない道具です。

---

## まとめ

複素関数とは「複素数を入力・出力とする関数」です。実数の関数の自然な拡張ですが、「正則性」という条件を満たすとき、実数の世界では見られない驚くべき性質が現れます。

---

## 関連ページ

- [複素数（入門）](../../numbers/complex-numbers/introduction.md)
- [微分（入門）](../derivatives/introduction.md)
