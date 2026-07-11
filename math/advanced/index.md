---
title: 応用編
description: "中級編を踏まえ、複素数・整数の性質、多項式や集合・証明法、二次関数や指数対数三角関数、図形とベクトル、数列・極限・微分積分、場合の数・確率・統計的な推測まで体系的に扱う"
tags: [math, advanced]
hierarchy:
  - title: 数学
    path: ../index.md
  - title: 応用編
    path: index.md
---

中級編の内容を前提に、関数・図形・微積分の初歩など、体系的に数学を扱います。

## 数

### 複素数
実数では解けない方程式から生まれた数。虚数単位・四則演算・複素平面・極形式を扱います。

- [複素数](numbers/complex-numbers.md)

### 整数の性質・n進法
ユークリッドの互除法・1次不定方程式と、10以外を底とする位取り記数法を扱います。

- [ユークリッドの互除法](numbers/euclidean-algorithm.md)
- [n進法](numbers/number-systems.md)

## 代数

### 多項式
べき乗の和で表される関数。根・因数定理・代数学の基本定理を扱います。

- [多項式](algebra/polynomials.md)
- [整式の除法と剰余の定理](algebra/polynomial-division.md)

### 三次の乗法公式・等式不等式の証明
2次の乗法公式を3次に拡張し、恒等式・相加相乗平均を用いた証明を扱います。

- [三次の乗法公式](algebra/cubic-expansion.md)
- [等式・不等式の証明](algebra/inequality-proofs.md)

## 基礎

### 集合
ものの集まりを数学的に扱う言語。和集合・共通部分・補集合・部分集合を扱います。

- [集合](foundations/sets.md)

### 必要・十分条件
「ならば」の向きと強さ。必要条件・十分条件・対偶・背理法を扱います。

- [必要・十分条件](foundations/logic.md)

### 証明法
数学的命題を正しく示す方法。直接証明・対偶証明・背理法・数学的帰納法を扱います。

- [証明法とは](foundations/proofs.md)
- [直接証明](foundations/proofs-direct.md)
- [対偶証明](foundations/proofs-contrapositive.md)
- [背理法](foundations/proofs-contradiction.md)
- [数学的帰納法](foundations/proofs-induction.md)

## 具体的な関数

### 二次関数
グラフが放物線になる関数。頂点・判別式・二次不等式を扱います。

- [二次関数](specific-functions/quadratic.md)

### 指数関数
倍々で増える変化を表す関数。指数法則と指数方程式を扱います。

- [指数関数](specific-functions/exponential.md)

### 対数関数
「何乗すれば？」という問いに答える関数。指数関数の逆です。

- [対数関数](specific-functions/logarithmic.md)

### 三角関数
単位円から生まれる周期関数。波・振動・回転のモデルです。

- [三角関数](specific-functions/trigonometric.md)

### 分数関数・無理関数
反比例・平方根のグラフを平行移動した関数。漸近線と定義域を扱います。

- [分数関数・無理関数](specific-functions/rational-irrational-functions.md)

## 幾何

### 点
位置だけを持つ最も基本的な要素。座標・距離・中点を扱います。

- [点](geometry/point.md)

### 直線
2点を結んで伸ばした線。方程式・平行・垂直・距離を扱います。

- [直線](geometry/line.md)

### 三角比・三角形
直角三角形の辺の比から始まる三角比と、正弦定理・余弦定理・五心を扱います。

- [三角比](geometry/trigonometry.md)
- [三角形](geometry/triangles.md)
- [三角形の性質の応用](geometry/triangle-theorems.md)

### 円
中心から等距離にある点の集合。方程式・接線・弧長を扱います。

- [円](geometry/circles.md)
- [円の性質の応用](geometry/circle-theorems.md)

### 軌跡と領域
条件を満たす点の集まりを方程式で表し、不等式が表す領域を図示します。

- [軌跡と領域](geometry/locus-and-regions.md)

### 二次曲線
放物線・楕円・双曲線と、媒介変数表示・極座標を扱います。

- [二次曲線](geometry/conic-sections.md)

### 空間図形の性質
直線と平面の垂直条件・三垂線の定理と、正多面体が5種類しかない理由を扱います。

- [空間図形の性質](geometry/solid-geometry.md)

### ベクトル
向きと大きさを持つ量。平面・空間のベクトルと内積、図形への応用を扱います。

- [ベクトル](geometry/vectors.md)
- [空間座標とベクトル](geometry/space-vectors.md)

## 解析

### 関数とは
入力に対して出力が一意に定まる対応関係。定義域・値域・合成関数・逆関数を扱います。

- [関数とは](analysis/functions.md)

### 数列
自然数を引数にとる離散的な関数。等差・等比・漸化式・無限級数を扱います。

- [数列](analysis/sequences.md)

### 極限
「限りなく近づく」という概念。微積分の土台です。

- [極限](analysis/limits.md)

### 微分
瞬間の変化率を求める操作。

- [微分](analysis/derivatives.md)
- [微分の応用](analysis/derivatives-applications.md)

### 積分
面積・累積を求める操作。微分の逆操作です。

- [積分](analysis/integrals.md)

## 確率

### 場合の数
順列・組み合わせ——「何通りあるか」を数えます。

- [場合の数とは](probability/counting.md)
- [順列](probability/counting-permutations.md)
- [組み合わせ](probability/counting-combinations.md)
- [二項定理](probability/counting-binomial-theorem.md)

### 確率
起こりやすさを0から1の数値で表す理論。条件付き確率・ベイズの定理を扱います。

- [確率とは](probability/probability.md)
- [条件付き確率とベイズの定理](probability/probability-conditional.md)

### データの分析
分散・標準偏差・相関係数でデータの特徴を数値化し、仮説検定の考え方を扱います。

- [データの分析](probability/data-analysis.md)

### 統計的な推測
確率変数と確率分布、二項分布・正規分布、標本平均の分布を使った区間推定・仮説検定を扱います。

- [確率変数と確率分布](probability/random-variables.md)
- [二項分布](probability/binomial-distribution.md)
- [正規分布](probability/normal-distribution.md)
- [統計的な推測](probability/statistical-inference.md)
