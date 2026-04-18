---
title: 証明法
description: "証明論・形式体系・計算可能性"
goal: "形式証明の概念を理解し、ヒルベルトの形式主義プログラムとその限界（ゲーデルの不完全性定理）を説明できるようになる"
tags: [math,foundations,proofs]
hierarchy:
  - title: 数学
    path: /math/index.md
  - title: 基礎
    path: /math/foundations/index.md
  - title: 証明法
    path: /math/foundations/proofs/professional.md
levels:
  - level: 入門
    path: introduction.md
  - level: 標準
    path: standard.md
  - level: 専門
level: 専門
requires:
  - title: 証明法（標準）
    path: /math/foundations/proofs/standard.md
  - title: 論理・必要十分条件（専門）
    path: /math/foundations/logic/professional.md
  - title: 集合（専門）
    path: /math/foundations/sets/professional.md
---

## 形式体系

数学的証明を完全に形式化する試みが**形式体系**です。

**定義**：形式体系 $\mathcal{F}$ は次の要素からなります。
- **記号の集合**：アルファベット
- **整式（well-formed formula）の定義**：記号列の文法規則
- **公理**：前提として認める整式の集合
- **推論規則**：既存の整式から新しい整式を導く規則

証明とは、公理から推論規則を有限回適用して得られる整式の列です。

---

## ヒルベルトのプログラム

20世紀初頭、ヒルベルトは「すべての数学を有限の公理と推論規則に基づく形式体系に還元し、その無矛盾性を有限の手段で証明する」という野心的なプログラムを提唱しました。

これは数学の完全な機械化——「問題を公理に入力すると証明が出力される機械」——の夢でもありました。

---

## ゲーデルの不完全性定理

**第一不完全性定理**（1931）：ペアノ算術を含む無矛盾な帰納的公理系 $T$ に対して、$T$ で証明も反証もできない命題が存在する。

**第二不完全性定理**：そのような $T$ は自身の無矛盾性を $T$ の中で証明できない。

これによりヒルベルトのプログラムは原理的に不可能であることが示されました。

証明の核心は**ゲーデル数**（命題を自然数にエンコードする技法）と自己言及的命題「この命題は証明できない」の構成にあります。

**参考文献**：Gödel, K. (1931). "Über formal unentscheidbare Sätze der Principia Mathematica und verwandter Systeme I." *Monatshefte für Mathematik und Physik*, 38, 173–198.

---

## 計算可能性との関係

**チャーチ＝チューリングのテーゼ**：直感的に計算可能な関数の全体はチューリング機械で計算可能な関数に一致する。

**停止問題**：「任意のプログラムが停止するかどうかを判定するプログラム」は存在しない（チューリング, 1936）。

停止問題の決定不可能性とゲーデルの不完全性定理は深く関連しており、どちらも「形式体系の能力の限界」を示しています。

**参考文献**：Turing, A. M. (1936). "On Computable Numbers, with an Application to the Entscheidungsproblem." *Proceedings of the London Mathematical Society*, 42, 230–265.

---

## カリー＝ハワード対応

証明と計算の間には深い対応があります。

| 論理 | プログラミング |
|------|--------------|
| 命題 | 型 |
| 証明 | プログラム |
| 含意 $A \Rightarrow B$ | 関数型 $A \to B$ |
| 連言 $A \wedge B$ | 積型 $(A, B)$ |
| 選言 $A \vee B$ | 和型 $A \mid B$ |

この対応により、数学的証明を型検査器で自動検証する**定理証明支援系**（Coq, Lean, Agdaなど）が開発されています。

**参考文献**：Sorensen, M. H. & Urzyczyn, P. (2006). *Lectures on the Curry-Howard Isomorphism*. Elsevier.

---

## 関連ページ

- [論理・必要十分条件（専門）](../logic/professional.md)
- [集合（専門）](../sets/professional.md)
- [自然数（専門）](../../numbers/natural-numbers/professional.md)
