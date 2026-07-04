# Leadus Project

## 概要

## 構成

記事は学習順序を表す5段階（初級編・中級編・応用編・発展編・探求編）で構成されています。各段階が最上位のディレクトリになり、その下に科目・トピックが続きます。

```
math/
├── beginner/             # 初級編（小学校相当）
│   └── numbers/
│       ├── natural-numbers.md
│       ├── fractions.md
│       └── decimals.md
│
├── intermediate/         # 中級編（中学校相当）
│   ├── numbers/
│   │   ├── integers.md
│   │   └── arithmetic.md
│   ├── algebra/
│   │   ├── expressions.md
│   │   ├── equations.md
│   │   └── inequalities.md
│   └── geometry/
│       ├── quadrilaterals.md
│       └── polygons.md
│
├── advanced/             # 応用編（高校相当）
│   ├── numbers/          # complex-numbers.md
│   ├── algebra/          # polynomials.md
│   ├── foundations/      # sets.md, logic.md, proofs.md
│   ├── specific-functions/ # linear/quadratic/exponential/logarithmic/trigonometric.md
│   ├── geometry/         # point/line/triangles/circles.md
│   ├── analysis/         # functions/sequences/limits/derivatives/integrals.md
│   └── probability/      # counting.md, probability.md
│
├── bachelor/             # 発展編（大学相当）
│   ├── numbers/          # real-numbers.md
│   ├── algebra/          # abstract.md
│   ├── geometry/         # topology.md
│   ├── analysis/         # epsilon-delta/differentiability/riemann-integral/complex-analysis.md
│   ├── linear-algebra/   # vectors/matrices/linear-maps/eigenvalues.md
│   └── probability/      # distributions.md, statistics.md
│
└── master/               # 探求編（研究レベル相当、現時点では記事なし）
```

トピック本体は`<段階>/<科目>/<トピック>.md`というフラットファイルで、図版などの副次資材は記事と同名のディレクトリ（例：`<トピック>/images/`）に配置します。詳細は[CONTRIBUTING.md](/CONTRIBUTING.md)を参照してください。

## ライセンス

本サイトのコンテンツは [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) に準拠します。

[![CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-sa/4.0/)

## クレジット
連絡先はこちら

[support@leadus.info](mailto:support@leadus.info)


## コントリビュータへ
[こちら](/CONTRIBUTING.md)をお読みください。
