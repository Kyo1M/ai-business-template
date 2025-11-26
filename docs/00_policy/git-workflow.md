---
title: Git運用フロー
created: 2025-01-01
updated: 2025-01-01
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
git commit -m "[docs] ペルソナを追加"

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
git commit -m "[fix] typo修正"
git push origin main
```

### 3. 重要な変更（レビューが必要）

```bash
# 1. Issueを作成（GitHub上で）

# 2. ブランチを作成
git checkout -b feature/pivot-strategy

# 3. 作業・コミット
git add .
git commit -m "[strategy] ピボット案を追加"

# 4. プッシュ
git push origin feature/pivot-strategy

# 5. GitHub上でPull Requestを作成

# 6. レビュー後にマージ
```

## コミットの粒度

### 良いコミット
```
[docs] ペルソナAを追加
[hypothesis] H1を検証済みに更新、結果を記載
[strategy] MVP定義v2を作成
```

### 悪いコミット
```
更新
いろいろ修正
WIP
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



