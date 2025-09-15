---
term: "knowledge cutoff"
ja: "知識カットオフ"
aliases: ["model cutoff date", "training data cutoff"]
related: ["longitudinal-evaluation", "benchmark-contamination", "temporal-stratification"]
refs: [2509.00072]
---

# 用語の説明
- 定義: モデルの学習データが原則として含む情報の最終日付。以降の知識は未学習と仮定される。
- 背景: 前後で性能を比較することで汚染の兆候（ポストカットオフ低下など）を検出。
- 例/注意: カットオフ前後6カ月を含む月次バケットで縦断評価。

