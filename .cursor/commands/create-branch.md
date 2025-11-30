---
description: 作業内容から適切なブランチ名を生成し、ブランチを作成して移動
globs: 
alwaysApply: false
---

# Gitブランチ作成

作業内容を分析し、適切なブランチ名を提案してブランチを作成・移動します。

## 言語指定

- ブランチ名は **英語（ケバブケース）** で記述
- 説明や対話は日本語で行う

## ブランチ命名規則

### Prefix（必須）

| Prefix | 用途 |
|--------|------|
| feature/ | 新機能・新ドキュメントの追加 |
| fix/ | バグ修正・誤字修正 |
| docs/ | ドキュメント更新・追記 |
| experiment/ | 実験的な変更・検証 |
| refactor/ | リファクタリング |
| chore/ | 雑務・設定変更 |

### 命名フォーマット

```
<prefix>/<作業内容をケバブケースで表現>
```

### 命名ルール

1. **小文字英数字とハイフンのみ使用**
   - OK: `feature/add-user-auth`
   - NG: `feature/Add_User_Auth`

2. **簡潔で意味が伝わる名前**
   - OK: `feature/add-persona`
   - NG: `feature/add-new-persona-document-for-target-customer-analysis`

3. **動詞から始める**
   - OK: `fix/correct-typo-in-hypothesis`
   - NG: `fix/hypothesis-typo`

4. **Issue番号がある場合は末尾に付加（任意）**
   - 例: `feature/add-login-123`

## 生成例

### 例1: 新機能追加

作業内容: 「ユーザー認証機能を追加したい」

```
feature/add-user-authentication
```

### 例2: バグ修正

作業内容: 「仮説ドキュメントの誤字を修正」

```
fix/correct-typo-in-hypothesis
```

### 例3: ドキュメント更新

作業内容: 「ロードマップに2025年Q2の計画を追加」

```
docs/add-q2-2025-roadmap
```

### 例4: 実験的変更

作業内容: 「新しい価格モデルを検討」

```
experiment/explore-new-pricing-model
```

### 例5: リファクタリング

作業内容: 「共通コンポーネントを整理」

```
refactor/organize-common-components
```

## 禁止事項

- 日本語を含むブランチ名
- スペースやアンダースコアの使用
- 意味が伝わらない略語（`feature/upd` など）
- 長すぎるブランチ名（50文字以上）

---

## 実行手順

1. ユーザーから作業内容を聞く（または提供された内容を分析）
2. 適切なPrefixを選択
3. 作業内容をケバブケースに変換
4. ブランチ名を提案
5. ユーザーの承認を得る
6. 以下のコマンドを実行:
   ```bash
   git checkout main
   git pull origin main
   git checkout -b <ブランチ名>
   ```
7. 作成完了を報告

## 対話例

**ユーザー**: ペルソナのドキュメントを追加したい

**アシスタント**: 
以下のブランチ名を提案します：

```
feature/add-persona-document
```

または、ドキュメント専用として：

```
docs/add-persona
```

どちらがよろしいですか？または別の名前をご希望でしたらお知らせください。

