---
title: 積分
description: "細かく分けて足し合わせる操作"
goal: "積分の基本的なアイデアと必要性を日常的な例を使って説明できるようになる"
tags: [math,functions,calculus]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 関数の操作
    path: /math/functions/index.md
  - title: 積分
    path: /math/functions/integrals/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 微分
    path: /math/functions/derivatives/introduction.md
  - title: 極限
    path: /math/functions/limits/introduction.md
---

## 曲線で囲まれた面積

長方形の面積は縦×横で求められます。では、こんな問題はどうでしょう。

> なめらかな曲線と $x$ 軸の間の面積は？

定規では測れません。でも、アイデアがあります。

---

## 細い長方形で近似する

曲線の下の領域を、細い長方形で埋めてみましょう。長方形が粗ければ近似は大ざっぱです。でも、長方形を細くすればするほど、近似は正確になります。

長方形を「無限に細くした極限」——それが**積分**です。

$$\text{積分} = \text{面積} = \text{無限に細かくした長方形の和の極限}$$

---

## 「累積した量」を求める

速さが変化しながら走るとき、走った距離はどうなるでしょう？

「速さ×時間 = 距離」ですが、速さが変わり続けるなら一口には言えません。でも、細かい時間ごとに「速さ×短い時間」を足し合わせていけば、走った距離に近づきます。これも積分の考え方です。積分は「変化し続ける量を積み重ねた総量」を求める操作です。

---

## 微分と積分の関係

「速さを積み重ねると距離」「距離を微分すると速さに戻る」——微分と積分は逆の操作です。

曲線の傾き（微分）と面積（積分）が逆関係にあるという事実は、数学史上最大の発見のひとつです。これを**微積分学の基本定理**といいます。

---

## まとめ

積分は「細い長方形を無限に足し合わせた極限」として面積を求める操作です。「変化し続ける量の累積」も同じ仕組みで計算できます。微分の逆操作でもあり、この関係が微積分学の核心です。

---

## 関連ページ

- [微分（入門）](../derivatives/introduction.md)
- [極限（入門）](../limits/introduction.md)
