---
title: コミットメッセージ生成
purpose: Gitの変更差分からConventional Commits形式のコミットメッセージを生成
input: git diff または ステージングされた変更内容
output: Conventional Commits形式のコミットメッセージ（日本語）
---

# コミットメッセージ生成

## 使用方法

コードやドキュメントを変更した後、コミット前に使用します。
`git diff` や `git diff --cached` の出力を入力として渡し、適切なコミットメッセージを生成します。

### Cursorでの使い方

1. ファイルを変更後、ステージング（`git add`）
2. Cursorのチャットで `/generate-commit-message` を呼び出す
3. 生成されたメッセージでコミット

または、このプロンプト本文をコピーして使用することも可能です。

## プロンプト本文

```
あなたはGitコミットメッセージを生成するアシスタントです。
提供された変更差分を分析し、Conventional Commits形式でコミットメッセージを作成してください。

## ルール

### 言語
- コミットメッセージは日本語で記述
- 技術用語・固有名詞は英語のまま使用可

### フォーマット

<Prefix>: <サマリ（50文字以内）>

- 変更内容1
- 変更内容2

Refs: #Issue番号（該当する場合）
BREAKING CHANGE: 内容（後方互換を壊す場合）

### Prefix一覧
- feat: 新機能
- fix: バグ修正
- refactor: リファクタリング
- perf: パフォーマンス改善
- test: テスト
- docs: ドキュメント
- build: ビルド/依存関係
- ci: CI関連
- chore: 雑務
- style: スタイル変更
- revert: 取り消し

スコープを指定する場合: <Prefix>(scope): <サマリ>

### 生成の原則
- 必ず未コミットの差分を確認してから生成
- issueタイトルやブランチ名だけから推測しない
- 実際の差分に含まれる変更内容を要約・列挙

### 禁止事項
- 曖昧なサマリ（例: "update", "修正", "fix bug"）
- 差分を見ずに推測で作成
- 箇条書きのない長文

## 変更内容

{変更差分をここに貼り付け}
```

## 使用例

### 入力例

```diff
diff --git a/docs/01_discovery/target-persona.md b/docs/01_discovery/target-persona.md
index abc1234..def5678 100644
--- a/docs/01_discovery/target-persona.md
+++ b/docs/01_discovery/target-persona.md
@@ -10,6 +10,15 @@ status: review
 ## ペルソナA: 新規事業担当者
 
 ### 基本情報
+- 年齢: 30-40代
+- 役職: 事業開発部 マネージャー
+- 企業規模: 中堅〜大企業
+
+### 課題
+- アイデアを形にする方法がわからない
+- 社内説得用の資料作成に時間がかかる
+- 仮説検証の進め方が不明確
```

### 出力例

```
docs: ターゲットペルソナAの詳細情報を追加

- 基本属性（年齢、役職、企業規模）を定義
- 主要な課題を3点追加
- ペルソナの解像度を向上
```

### 破壊的変更の例

```
feat!: API認証方式をJWTに変更

- Bearer Token認証からJWT認証に移行
- 認証ミドルウェアを全面的に書き換え
- レスポンス形式を統一

BREAKING CHANGE: 既存のAPIキー認証は廃止。クライアントはJWTトークンを使用する必要あり
```

## 関連ドキュメント

- [Git運用フロー](../../docs/00_policy/git-workflow.md)
- [Conventional Commits](https://www.conventionalcommits.org/)
- Cursor Rule: `.cursor/rules/generate-commit-message.mdc`

## 改善履歴

| 日付 | 変更内容 | 理由 |
|------|----------|------|
| 2025-11-30 | 初版作成 | Conventional Commits形式でのコミットメッセージ生成を自動化 |

