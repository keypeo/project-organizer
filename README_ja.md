# 🗂️ プロジェクトオーガナイザー Skill

[English](README.md) | [中文](README_zh.md) | [한국어](README_ko.md)

> すべてのプロジェクトでAIアシスタントが自動的に構造化されたファイル管理を実行するSkillです。

## 機能

インストールすると、AIアシスタントがすべてのプロジェクトで**積極的にファイルを整理**します。長時間の作業セッション後にフォルダが散らかることはもうありません。

| トリガー | 動作 |
|---------|------|
| 新しいプロジェクトの開始 | 標準化されたフォルダ構成を提案・作成 |
| タスク中にファイルを作成 | 各ファイルを正しいフォルダに自動配置 |
| 「整理して」「片付けて」と指示 | プロジェクトフォルダ全体をスキャンして再編成 |
| 3〜5回のファイル操作ごと | クリーンアップチェックポイントを実行 |

## 基本ルール

### 📁 標準プロジェクト構成

```
project-name/
├── README.md        — プロジェクト説明、ステータス、規約
├── drafts/          — 作業中の草稿、反復バージョン
├── figures/         — 画像、チャート、図表
├── scripts/         — 出力を生成するコード
├── references/      — 参考資料、テンプレート
├── output/          — 最終成果物のみ
└── archive/         — 置き換えられた旧バージョン（削除ではなく移動）
```

### 📝 命名規則

| ✅ 正しい | ❌ 間違い |
|----------|----------|
| `report_v1.docx` | `report_final.docx` |
| `report_v2.docx` | `report_new.docx` |
| `submission_20260226.docx` | `report_final_FINAL.docx` |

### 🏗️ ドメイン別テンプレート

以下のテンプレートが組み込まれています：
- **学術論文** — drafts / figures / scripts / references / output / archive
- **Webアプリケーション** — src / public / scripts / docs / dist
- **データ分析** — data / notebooks / scripts / figures / output

## インストール

`project-organizer/` フォルダをskillsディレクトリに配置してください：

```
~/.gemini/antigravity/skills/project-organizer/
```

すべての新しい会話で自動的に有効になります。

## ライセンス

MIT
