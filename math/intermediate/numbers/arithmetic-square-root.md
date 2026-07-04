---
title: 平方根
description: "累乗の逆操作"
goal: "平方根の意味を理解し、根号を含む式の計算・有理化ができるようになる"
tags: [math, numbers, arithmetic]
stage: 中級編
subject: 数
hierarchy:
  - title: 数学
    path: ../../index.md
  - title: 中級編
    path: ../index.md
  - title: 平方根
    path: arithmetic-square-root.md
requires:
  - title: 累乗
    path: arithmetic.md
---

## 平方根——累乗の逆

「2乗すると9になる数は何か？」——答えは3です。$3^2 = 9$ だからです。

この「2乗すると $a$ になる数（$a \geq 0$）」を**平方根**といい、$\sqrt{a}$ と書きます。

$$\sqrt{9} = 3, \quad \sqrt{4} = 2, \quad \sqrt{25} = 5$$

$\sqrt{2}$ はどうでしょう。$1^2 = 1$、$2^2 = 4$ なので1と2の間のどこかにあります。電卓で計算すると $\sqrt{2} \approx 1.41421\ldots$ で、割り切れない小数が延々と続きます。これは整数でも分数でもない数（無理数）です。

---

## 根号を含む式の計算

平方根には次の性質があります。

$$\sqrt{ab} = \sqrt{a} \times \sqrt{b}, \qquad \sqrt{\frac{a}{b}} = \frac{\sqrt{a}}{\sqrt{b}}$$

これを使うと、根号の中を簡単にできます。

**例**：$\sqrt{12} = \sqrt{4 \times 3} = \sqrt{4} \times \sqrt{3} = 2\sqrt{3}$

分母に根号が残っていると計算しづらいので、分母と分子に同じ数を掛けて根号を分子に移します（**有理化**）。

$$\frac{1}{\sqrt{2}} = \frac{1 \times \sqrt{2}}{\sqrt{2} \times \sqrt{2}} = \frac{\sqrt{2}}{2}$$

**例題**：$\frac{\sqrt{18}}{\sqrt{2}}$ を計算する。

$$\frac{\sqrt{18}}{\sqrt{2}} = \sqrt{\frac{18}{2}} = \sqrt{9} = 3$$

---

## まとめ

平方根は2乗の逆操作です。$\sqrt{ab}=\sqrt{a}\sqrt{b}$ などの性質を使うと根号の中を簡単にでき、分母の根号は有理化して整理します。

---

## 関連ページ

- [無理数（中級編）](irrational-numbers.md)
- [誤差と近似値（中級編）](approximation.md)
