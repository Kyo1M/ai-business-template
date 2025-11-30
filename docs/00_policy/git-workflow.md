---
title: Git運用フロー
created: 2025-01-01
updated: 2025-11-30
status: approved
---

# Git運用フロー

## ブランチ戦略

### メインブランチ
- `main`: 本番環境・確定版

### 作業ブランチ
```
feature/   # 新機能・新ドキュメント
fix/       # 修正
docs/      # ドキュメント更新
experiment/# 実験的な変更
```

### 命名例
```
feature/add-persona
fix/typo-in-hypothesis
docs/update-roadmap
experiment/new-pricing-model
```

## 基本ワークフロー

### 1. 通常の作業フロー

```bash
# 1. mainから最新を取得
git checkout main
git pull origin main

# 2. 作業ブランチを作成
git checkout -b feature/add-persona

# 3. 作業・コミット
git add .
git commit -m "docs: ペルソナを追加

- ペルソナAの基本情報を定義
- 課題と目標を記載"

# 4. mainにマージ
git checkout main
git merge feature/add-persona

# 5. プッシュ
git push origin main

# 6. 作業ブランチを削除
git branch -d feature/add-persona
```

### 2. 軽微な修正

```bash
# mainで直接作業（typo修正など）
git checkout main
git add .
git commit -m "fix: typo修正

- hypothesis.mdの誤字を修正"
git push origin main
```

### 3. 重要な変更（レビューが必要）

```bash
# 1. Issueを作成（GitHub上で）

# 2. ブランチを作成
git checkout -b feature/pivot-strategy

# 3. 作業・コミット
git add .
git commit -m "feat: ピボット案を追加

- 新しい戦略案を3パターン記載
- 各案のメリット・デメリットを比較

Refs: #45"

# 4. プッシュ
git push origin feature/pivot-strategy

# 5. GitHub上でPull Requestを作成

# 6. レビュー後にマージ
```

## コミットメッセージ規約

### 基本フォーマット

Conventional Commits形式を採用します。

```
<Prefix>: <サマリ（日本語、50文字以内）>

- 変更内容1（箇条書き）
- 変更内容2（箇条書き）

Refs: #<Issue番号>（任意）
BREAKING CHANGE: <内容>（任意）
```

### Prefix一覧

| Prefix | 用途 |
|--------|------|
| feat | 新機能の追加 |
| fix | バグ修正 |
| refactor | リファクタリング（挙動変更なし） |
| perf | パフォーマンス改善 |
| test | テスト追加/修正 |
| docs | ドキュメント更新 |
| build | ビルド/依存関係の変更 |
| ci | CI関連の変更 |
| chore | 雑務（ツール設定/スクリプト等） |
| style | スタイルのみの変更 |
| revert | 取り消し |

スコープを指定する場合: `<Prefix>(scope): <サマリ>`

### 良いコミットメッセージ

```
docs: ペルソナAを追加

- 基本情報（年齢、役職、企業規模）を定義
- 主要な課題を3点追加
```

```
feat(hypothesis): H1を検証済みに更新

- 検証結果を記載
- 次のアクションを追加

Refs: #12
```

```
refactor: MVP定義v2を作成

- 機能を優先度別に再整理
- スコープ外の機能を明確化
- 挙動の変更なし
```

### 悪いコミットメッセージ

```
更新
いろいろ修正
WIP
fix bug
```

### 破壊的変更がある場合

Prefixに `!` を付けるか、フッターに `BREAKING CHANGE:` を記載します。

```
feat!: API認証方式をJWTに変更

- 認証ミドルウェアを全面的に書き換え

BREAKING CHANGE: 既存のAPIキー認証は廃止
```

## コンフリクト解決

```bash
# 1. mainを最新化
git checkout main
git pull origin main

# 2. 作業ブランチでリベース
git checkout feature/xxx
git rebase main

# 3. コンフリクトを解決
# （エディタでコンフリクト箇所を修正）
git add .
git rebase --continue

# 4. マージ
git checkout main
git merge feature/xxx
```

## よく使うコマンド

```bash
# 状態確認
git status
git log --oneline -10

# 差分確認
git diff
git diff --cached

# 直前のコミットを修正
git commit --amend

# 変更を一時退避
git stash
git stash pop

# ブランチ一覧
git branch -a

# リモートの変更を取得（マージなし）
git fetch origin
```

## GitHub連携

### Issue
- 大きな変更・検討事項はIssueで議論
- ラベルを活用: `hypothesis`, `strategy`, `bug`, `enhancement`

### Pull Request
- 重要な変更はPRを作成
- レビュワーをアサイン
- マージ前にコンフリクトを解決

### テンプレート
- `.github/ISSUE_TEMPLATE/` にIssueテンプレートあり
- `.github/PULL_REQUEST_TEMPLATE.md` にPRテンプレートあり

## 参考

- [Conventional Commits](https://www.conventionalcommits.org/)

### Cursorカスタムコマンド

| コマンド | 用途 |
|----------|------|
| `/create-branch` | ブランチ名を生成して作成・移動 |
| `/generate-commit-message` | コミットメッセージを生成 |
| `/no-sugarcoating` | 忖度無しの正直なフィードバックを求める |
