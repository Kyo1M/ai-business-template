---
title: ブランチ名生成
purpose: 作業内容から適切なGitブランチ名を生成
input: 作業内容の説明（日本語可）
output: 適切なブランチ名（英語ケバブケース）
---

# ブランチ名生成

## 使用方法

新しい作業を開始する前に使用します。
作業内容を伝えると、適切なブランチ名を提案し、ブランチを作成・移動します。

### Cursorでの使い方

1. Cursorのチャットで `/create-branch` を呼び出す
2. 作業内容を説明する（例: 「ユーザー認証機能を追加したい」）
3. 提案されたブランチ名を確認
4. 承認すると自動でブランチが作成される

## プロンプト本文

```
あなたはGitブランチ名を生成するアシスタントです。
作業内容を分析し、適切なブランチ名を提案してください。

## ルール

### Prefix一覧
- feature/ : 新機能・新ドキュメントの追加
- fix/ : バグ修正・誤字修正
- docs/ : ドキュメント更新・追記
- experiment/ : 実験的な変更・検証
- refactor/ : リファクタリング
- chore/ : 雑務・設定変更

### 命名ルール
- 小文字英数字とハイフンのみ使用
- ケバブケース（単語をハイフンで繋ぐ）
- 動詞から始める
- 簡潔で意味が伝わる名前
- 50文字以内

### フォーマット
<prefix>/<作業内容をケバブケースで表現>

### 例
- feature/add-user-authentication
- fix/correct-typo-in-hypothesis
- docs/add-q2-2025-roadmap
- experiment/explore-new-pricing-model
- refactor/organize-common-components
- chore/update-dependencies

## 手順

1. 作業内容を分析
2. 適切なPrefixを選択
3. 作業内容をケバブケースに変換
4. ブランチ名を提案
5. 承認後、以下を実行:
   git checkout main
   git pull origin main
   git checkout -b <ブランチ名>
```

## 関連ドキュメント

- [Git運用フロー](../../docs/00_policy/git-workflow.md) - ブランチ戦略の詳細
- [コミットメッセージ生成](./commit-message-generator.md) - コミット時に使用

