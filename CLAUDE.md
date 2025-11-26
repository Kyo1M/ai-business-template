# CLAUDE.md - AI開発アシスタント向けインストラクション

## このリポジトリについて

**AIツールとの対話を通じて事業開発を進める** ためのドキュメントテンプレートです。

Cursor、Claude Code、GitHub Copilot などのAIツールと連携しながら、曖昧なアイデアを構造化されたドキュメントに落とし込み、継続的に改善していきます。

## リポジトリ構造

```
docs/
├── 00_policy/      # 運用方針（まず読む）
├── 01_discovery/   # 発見・検証フェーズ
├── 02_strategy/    # 戦略フェーズ
├── 03_development/ # 開発フェーズ
├── 04_growth/      # 成長・運用フェーズ
└── 99_archive/     # アーカイブ

templates/          # 再利用可能なテンプレート
prompts/            # AIプロンプト集
checklists/         # チェックリスト
notes/              # メモ・議事録
├── meetings/       # 議事録
├── ideas/          # アイデアメモ
├── research/       # 調査メモ
└── misc/           # その他
```

## フェーズの流れ

```
Discovery（発見）→ Strategy（戦略）→ Development（開発）→ Growth（成長）
```

各フェーズで作成すべきドキュメントは `docs/` 配下の対応フォルダにあります。

## ドキュメント作成ルール

### ファイル命名規則
- 小文字英数字とハイフンを使用（例: `target-persona.md`）
- 日本語ファイル名は避ける

### Markdownフォーマット
- 見出しは `#` から始め、階層は3レベルまで
- 箇条書きは `-` を使用
- コードブロックは言語指定する

### メタ情報
各ドキュメントの冒頭に以下を含める：

```markdown
---
title: ドキュメントタイトル
created: YYYY-MM-DD
updated: YYYY-MM-DD
status: draft | review | approved
---
```

## 作業時の注意事項

### やるべきこと
- 変更前に関連ドキュメント（特に `00_policy/`）を確認
- 仮説を更新したら `docs/01_discovery/hypothesis.md` の更新ログに記録
- 大きな変更はIssueを立てて議論
- コミットメッセージは日本語で、何を変更したか明確に

### やってはいけないこと
- 機密情報（API Key、パスワード、個人情報等）をコミットしない
- 検証されていない仮説を「事実」として記載しない
- 古い情報を残さない（99_archive/ に移動する）

## よく行う作業

### 新しいドキュメントを追加する場合
1. 適切なフォルダを選択（フェーズに対応したフォルダ）
2. メタ情報テンプレートを含めて作成
3. README.mdの一覧に追加（重要なもののみ）

### メモ・議事録を追加する場合
1. `notes/` 配下の適切なフォルダを選択（meetings, ideas, research, misc）
2. `YYYY-MM-DD-タイトル.md` の形式でファイルを作成
3. 議事録は `templates/meeting-notes.md` を参照
4. 学びや気づきは `docs/04_growth/learnings.md` にも反映

### 仮説を更新する場合
1. `docs/01_discovery/hypothesis.md` を編集
2. 更新ログに変更理由を記載
3. 検証結果は該当する仮説の「結果」欄に記録

## プロンプト参照先

| 用途 | ファイル |
|------|----------|
| アイデア発想 | `prompts/ideation/` |
| 分析 | `prompts/analysis/` |
| 開発 | `prompts/development/` |

## 重要なドキュメント

プロジェクトを理解するために、以下の順で読むことを推奨：

1. `docs/01_discovery/hypothesis.md` - 現在の仮説
2. `docs/01_discovery/target-persona.md` - ターゲット顧客
3. `docs/02_strategy/mvp-definition.md` - MVP定義
4. `docs/02_strategy/roadmap.md` - ロードマップ



