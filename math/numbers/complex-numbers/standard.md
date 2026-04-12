---
title: 複素数
description: "実数を超えた数の体系"
tags: [math,complex-numbers,complex-numbers]
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
  - title: 負数
    path: /math/numbers/negative-numbers/introduction.md
  - title: 三角関数
    path: /math/functions/trigonometric/introduction.md
  - title: 指数関数
    path: /math/functions/exponential/introduction.md
---

## 虚数単位と複素数の定義

**定義**：$i^2 = -1$ を満たす数 $i$ を**虚数単位**といいます。

**定義**：実数 $a, b$ を用いて $z = a + bi$ と表せる数を**複素数**といいます。

- $a = \text{Re}(z)$：**実部**
- $b = \text{Im}(z)$：**虚部**
- $b = 0$ のとき実数、$a = 0$ かつ $b \neq 0$ のとき純虚数

---

## 四則演算

複素数は実数と同じルールで計算し、$i^2 = -1$ を適用します。

**加法**：

$$(3 + 2i) + (1 - i) = 4 + i$$

**乗法**（分配法則を使い $i^2 = -1$ を代入）：

$$(1 + 2i)(3 + i) = 3 + i + 6i + 2i^2 = 3 + 7i - 2 = 1 + 7i$$

**複素共役**：$\overline{a + bi} = a - bi$（虚部の符号を変える）

**除法**（分母の共役を掛けて実数化）：

$$\frac{1 + 2i}{3 + i} = \frac{(1+2i)(3-i)}{(3+i)(3-i)} = \frac{3 - i + 6i - 2i^2}{9 + 1} = \frac{5 + 5i}{10} = \frac{1+i}{2}$$

---

## 複素平面

複素数 $a + bi$ を平面上の点 $(a, b)$ として表します。\
横軸が実軸、縦軸が虚軸です。

**絶対値**（原点からの距離）：

$$|z| = \sqrt{a^2 + b^2}$$

**性質**：$|z_1 z_2| = |z_1||z_2|$（絶対値の乗法性）

---

## 極形式とオイラーの公式

絶対値 $r = |z|$ と偏角 $\theta$（実軸からの角度）を使って：

$$z = r(\cos\theta + i\sin\theta) = re^{i\theta}$$

**オイラーの公式**（微積分から導かれる）：

$$e^{i\theta} = \cos\theta + i\sin\theta$$

$\theta = \pi$ を代入すると：

$$e^{i\pi} + 1 = 0$$

$e$、$i$、$\pi$、$1$、$0$ という5つの重要定数が一つの式に現れます。

**極形式の乗法**：$r_1 e^{i\theta_1} \times r_2 e^{i\theta_2} = r_1 r_2 e^{i(\theta_1 + \theta_2)}$

つまり複素数の乗法は「絶対値を掛け合わせ、偏角を足し合わせる」操作です——**回転と拡大の合成**です。

---

## 関連ページ

- [三角関数](../../functions/trigonometric/introduction.md)
- [複素関数](../../functions/complex-functions/introduction.md)
