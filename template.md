---
# 必須メタデータ（編集して使用）
title_en: ""            # 英語タイトル（原題）
title_ja: ""            # タイトルの日本語訳（自然な訳で）
arxiv: ""               # 例: 2509.12345（バージョンは本文側で管理）
version: "v1"           # 例: v1, v2（PDFファイル名に反映）
aliases: []              # 例: ["短縮名", "略称"]
tags: [paper]            # 分野タグを追加: [paper, LLM, RL, ...]
status: note             # note | draft | reviewed
venue: arXiv
year: 20xx
authors:
  -
links:
  - abs: https://arxiv.org/abs/<arxiv>
  - pdf: https://arxiv.org/pdf/<arxiv><version>.pdf
created: {{date}}
---

# {{title_en}} / {{title_ja}}

## 概要（3行で）
- 目的:
- アプローチ:
- 結果:

## 主な貢献
-
-
-

## 手法 / 設計
- 問題設定:
- 提案手法:
- 実装要点:

## 実験・評価（要約）
- セットアップ:
- 比較条件:
- 指標:

## 主要結果
-
-
-

## 考察・限界
- 位置づけ:
- 限界:
- 将来課題:

## 再現性メモ
- 依存/コード:
- データ/環境:
- ログ/設定:

## 応用・拡張アイデア
-
-

## キークォート
> ""

## 用語メモ（words/ を使う）
- [[words/TERM]]: 一言メモ（詳細は words の用語ページへ）

## 関連研究
-

## BibTeX
```bibtex
@misc{<key>,
  title         = {<title_en>},
  author        = {<authors>},
  year          = {<year>},
  eprint        = {<arxiv>},
  archivePrefix = {arXiv},
  primaryClass  = {cs.AI},
  url           = {https://arxiv.org/abs/<arxiv>}
}
```

## リンク
- arXiv: https://arxiv.org/abs/<arxiv>
- PDF: https://arxiv.org/pdf/<arxiv><version>.pdf

<!-- 作成手順メモ（削除可）
1) ファイル名は <arxiv>.md（例: 2509.12345.md）で作成。
2) 上部メタデータの arxiv, version, title_en, title_ja, authors を埋める。
3) PDF は保存しない。links.pdf は arXiv の URL（https://arxiv.org/pdf/<arxiv><version>.pdf）を使用。
4) 用語は words/ フォルダに用語ごとのノートを作り、ここから [[words/<term>]] でリンク。
-->
