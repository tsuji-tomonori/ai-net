# 論文ノート運用ルール（Obsidian）

目的: arXiv 論文の要点を素早く一貫して記録し、用語を横断参照できるようにする。

## ファイル命名・配置
- 論文ノートのファイル名は `arxiv-id.md` とする。
  - 例: `2509.08785.md`, `2509.09677.md`
  - 既存ノートは無理にリネームしないが、今後新規はこの形式に統一。
- PDF はリポジトリにコミットしない（必要ならローカル保持のみ）。
  - リンクは arXiv の PDF を使用: `https://arxiv.org/pdf/<arxiv-id><version>.pdf`
- 用語メモは `words/` フォルダ直下に、用語ごとに1ファイルを作成。
  - 例: `words/agent.md`, `words/self-conditioning.md`

## メタデータ（YAMLフロントマター）
- 必須項目
  - `title_en`: 英語原題
  - `title_ja`: 日本語訳（自然な訳）
  - `arxiv`: 数字のみの arXiv ID（例: `2509.12345`）
  - `version`: `v1` のように明記（PDFファイル名に使用）
  - `authors`: 著者の配列
  - `venue`: 基本は `arXiv`
  - `year`: 公開年
  - `tags`: 最低 `[paper]` を含める
  - `links`: `abs` と `pdf` を記載（pdf は arXiv の URL）
- 任意項目
  - `aliases`, `status`（`note|draft|reviewed`）
- 例は `template.md` を参照。

## タイトル表記
- ノート内の最初の見出しは `英題 / 和題` の併記とする。
  - 例: `# The Illusion of Diminishing Returns / 逓減の錯覚`
- `aliases` に英題の省略形や和題の別案を入れて検索性を上げる。

## セクション構成（推奨）
- 概要（3行で）: 目的 / アプローチ / 結果
- 主な貢献: 箇条書きで3±2項目
- 手法 / 設計: 問題設定・提案の核・実装要点
- 実験・評価（要約）: セットアップ / 比較条件 / 指標
- 主要結果: 要点の箇条書き
- 考察・限界: 位置づけ / 限界 / 将来課題
- 再現性メモ: 依存・データ・ログ
- 応用・拡張アイデア
- キークォート
- 用語メモ（words/ 参照）
- 関連研究
- BibTeX

## 用語集（words/）
- 目的: 用語の定義と背景を独立ノートとして体系化し、論文ノートから参照。
- ファイル作成規則
  - ファイル名は原則小文字・ハイフン区切り（英語が望ましい）。
    - 例: `self-conditioning.md`, `long-horizon.md`
  - 日本語用語を主に扱う場合はローマ字/英訳併記を推奨。
- 推奨テンプレート（コピペで使用）
  ```md
  ---
  term: ""          # 英語の見出し語
  ja: ""            # 日本語名（必要なら）
  aliases: []        # 同義・バリアント
  related: []        # 関連用語（words/<term> を想定）
  refs: []           # 参照論文（arXiv ID の配列: [2509.08785, ...]）
  ---

  # 用語の説明
  - 定義:
  - 背景:
  - 例/注意:
  ```
- 論文ノートからは `[[words/<file-name>]]` でリンクする。

## 作成フロー（新規論文）
1. `template.md` を複製し、ファイル名を `<arxiv-id>.md` に変更。
2. フロントマターに `title_en`, `title_ja`, `arxiv`, `version`, `authors`, `year` を入力。
3. `links` の `abs` と `pdf` を arXiv の URL で設定（例: `abs`: https://arxiv.org/abs/<arxiv>、`pdf`: https://arxiv.org/pdf/<arxiv><version>.pdf）。
4. 本文の各セクションを埋める。用語は必要に応じて `words/` に作成してリンク。

## 記載スタイル
- 箇条書きで短く、比較や数字は明示。
- 和訳は意訳しすぎず、専門用語は `words/` に切り出して定義。
- 図表やログの要点はテキストで要約（画像は任意）。
