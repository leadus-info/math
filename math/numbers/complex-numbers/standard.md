---
title: 複素数
description: "複素数の演算・複素平面・極形式"
goal: "複素共役・除法・複素平面・絶対値・極形式を理解し、複素数の計算と幾何的な意味を説明できるようになる"
tags: [math,numbers,complex-numbers]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 数
    path: /math/numbers/index.md
  - title: 複素数
    path: /math/numbers/complex-numbers/standard.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
  - level: 専門
    path: professional.md
level: 標準
requires:
  - title: 複素数（入門）
    path: /math/numbers/complex-numbers/introduction.md
  - title: 三角関数（入門）
    path: /math/geometry/trigonometry/introduction.md
---

## 複素数の定義

複素数（入門）で見た内容を正確に述べます。

**定義**：$i^2 = -1$ を満たす数 $i$ を**虚数単位**といいます。実数 $a, b$ を用いて $z = a + bi$ と表せる数を**複素数**といいます。複素数全体の集合を $\mathbb{C}$ と書きます。

- $a = \text{Re}(z)$：**実部**
- $b = \text{Im}(z)$：**虚部**
- $b = 0$ のとき実数、$a = 0$ かつ $b \neq 0$ のとき純虚数

$\mathbb{R} \subset \mathbb{C}$ です（実数は $b = 0$ の複素数）。

---

## 複素共役

$z = a + bi$ に対して、虚部の符号を反転した $\bar{z} = a - bi$ を**複素共役**といいます。

**性質**：
- $z + \bar{z} = 2a$（実部の2倍）
- $z \times \bar{z} = a^2 + b^2$（常に0以上の実数）

$z \times \bar{z}$ が実数になるという性質は、割り算で重要な役割を果たします。

---

## 割り算

複素数の割り算は、分母の複素共役を分母・分子に掛けて、分母を実数にします。

$$\frac{1 + 2i}{3 + i} = \frac{(1+2i)(3-i)}{(3+i)(3-i)}$$

分母：$(3+i)(3-i) = 9 - i^2 = 9 + 1 = 10$

分子：$(1+2i)(3-i) = 3 - i + 6i - 2i^2 = 3 + 5i + 2 = 5 + 5i$

$$\frac{5 + 5i}{10} = \frac{1}{2} + \frac{1}{2}i$$

---

## 複素平面

複素数 $a + bi$ を平面上の点 $(a, b)$ として表します。横軸を**実軸**、縦軸を**虚軸**とした平面を**複素平面**（ガウス平面）と呼びます。

複素数の足し算は、ベクトルの足し算と同じく平行四辺形の対角線に対応します。

---

## 絶対値

複素数 $z = a + bi$ の**絶対値**は、複素平面上の原点からの距離です。

$$|z| = \sqrt{a^2 + b^2}$$

**性質**：
- $|z| \geq 0$（等号は $z = 0$ のとき）
- $|z_1 \times z_2| = |z_1| \times |z_2|$
- $|z|^2 = z \times \bar{z}$

---

## 極形式

複素平面上の点は、原点からの距離 $r = |z|$ と実軸からの角度 $\theta$（**偏角**）で表すこともできます。

$$z = r(\cos\theta + i\sin\theta)$$

これを**極形式**といいます。

極形式では、掛け算の意味が明確になります。

$$r_1(\cos\theta_1 + i\sin\theta_1) \times r_2(\cos\theta_2 + i\sin\theta_2) = r_1 r_2(\cos(\theta_1 + \theta_2) + i\sin(\theta_1 + \theta_2))$$

つまり、複素数の掛け算は「絶対値を掛け合わせ、偏角を足し合わせる」操作です。幾何的には**回転と拡大の合成**に対応します。

**例**：$i$ を掛けることは、偏角を $90°$ 足すこと、つまり反時計回りに $90°$ 回転させることです。

---

## 関連ページ

- [三角関数（入門）](../../geometry/trigonometry/introduction.md)
- [複素関数（入門）](../../analysis/complex-analysis/introduction.md)