---
title: 線形写像
description: "ベクトルの構造を保つ変換"
goal: "線形写像が「足し算とスカラー倍を保つ変換」であることを理解し、行列との対応を説明できるようになる"
tags: [math,linear-algebra,linear-maps]
level: 入門
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 線形代数
    path: /math/linear-algebra/index.md
  - title: 線形写像
    path: /math/linear-algebra/linear-maps/introduction.md
levels:
  - level: 入門
  - level: 標準
    path: standard.md
  - level: 専門
    path: professional.md

requires:
  - title: 行列（入門）
    path: /math/linear-algebra/matrices/introduction.md
  - title: ベクトル（入門）
    path: /math/linear-algebra/vectors/introduction.md
---

## 「構造を保つ」変換

地図を拡大コピーするとき、距離は変わっても「直線は直線のまま」「平行な道は平行なまま」です。このように「足し算とスカラー倍の構造を壊さない変換」が**線形写像**です。

---

## 何が「線形」か

2つの条件を満たす変換 $f$ を線形といいます。

**足し算を保つ**：$f(\boldsymbol{u} + \boldsymbol{v}) = f(\boldsymbol{u}) + f(\boldsymbol{v})$「先に足してから変換」と「先に変換してから足す」が同じ結果になる。

**スカラー倍を保つ**：$f(c\boldsymbol{v}) = c f(\boldsymbol{v})$「先に $c$ 倍してから変換」と「先に変換してから $c$ 倍する」が同じ結果になる。

---

## 行列との関係

$\mathbb{R}^n$ から $\mathbb{R}^m$ への線形写像はすべて行列で表せます。

$2 \times 2$ 行列 $A$ を左から掛ける操作 $\boldsymbol{x} \mapsto A\boldsymbol{x}$ は線形写像です。逆に $\mathbb{R}^2 \to \mathbb{R}^2$ の線形写像はすべてある行列で表されます。

---

## 身近な線形写像の例

- **回転**：平面上の点を原点中心に $\theta$ 回転させる
- **拡大・縮小**：各座標を定数倍する
- **射影**：3次元ベクトルを平面に投影する

これらはすべて行列で書けます。

---

## 関連ページ

- [行列（入門）](../matrices/introduction.md)
- [ベクトル（入門）](../vectors/introduction.md)
