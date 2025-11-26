---
title: Notes - メモ・議事録管理
created: 2025-11-26
updated: 2025-11-26
status: approved
---

# 📝 Notes - メモ・議事録管理

プロジェクトに関するメモ、議事録、アイデアなどを管理するフォルダです。

## 📁 フォルダ構成

```
notes/
├── meetings/     # 議事録・ミーティングメモ
├── ideas/        # アイデアメモ・ブレスト記録
├── research/     # 調査・リサーチメモ
└── misc/         # その他のメモ
```

## 📋 各フォルダの用途

### meetings/ - 議事録

定例会議、ステークホルダーとのミーティング、顧客ヒアリングなどの記録

**ファイル命名例**:
- `2025-11-26-kickoff-meeting.md`
- `2025-11-26-weekly-sync.md`
- `2025-11-26-customer-interview-tanaka.md`

### ideas/ - アイデアメモ

新機能のアイデア、ブレインストーミングの記録、改善案など

**ファイル命名例**:
- `2025-11-26-new-feature-idea.md`
- `2025-11-26-brainstorm-ux-improvement.md`

### research/ - 調査メモ

市場調査、技術調査、ユーザーリサーチの結果など

**ファイル命名例**:
- `2025-11-26-market-research-saas.md`
- `2025-11-26-tech-comparison-auth.md`

### misc/ - その他

上記に分類されないメモ、一時的なメモなど

## ✍️ ファイル作成ルール

### 命名規則

```
YYYY-MM-DD-タイトル.md
```

- 日付を先頭に（時系列で並ぶように）
- 小文字英数字とハイフンを使用
- 内容がわかる簡潔なタイトル

### テンプレート

議事録のテンプレートは `templates/meeting-notes.md` を使用してください。

### メタ情報

各ファイルの冒頭に以下を含めることを推奨：

```markdown
---
title: タイトル
date: YYYY-MM-DD
participants: 参加者（議事録の場合）
tags: タグ（任意）
---
```

## 🔗 関連ドキュメントへの反映

メモから得られた重要な学びや気づきは、以下のドキュメントにも反映してください：

| 内容 | 反映先 |
|------|--------|
| 検証結果・学び | `docs/04_growth/learnings.md` |
| 仮説の更新 | `docs/01_discovery/hypothesis.md` |
| 実験結果 | `docs/04_growth/experiment-log.md` |
| 意思決定 | `templates/decision-log.md` を使用 |

