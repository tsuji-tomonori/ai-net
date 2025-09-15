---
term: "benchmark contamination"
ja: "ベンチマーク汚染"
aliases: ["data contamination in evaluation", "contaminated benchmarks"]
related: ["reasoning-driven-synthesis", "longitudinal-evaluation", "knowledge-cutoff"]
refs: [2509.00072]
---

# 用語の説明
- 定義: 学習データと評価データが重複・漏洩し、丸暗記によってスコアが不当に高くなる現象。推論能力の測定を歪める。
- 背景: 大規模事前学習の拡大により公開ベンチマークやWeb由来の問題の混入が常態化。
- 例/注意: カットオフ後の性能低下の有無で兆候を検出。推論駆動の合成問題で浅い記憶効果を低減。

