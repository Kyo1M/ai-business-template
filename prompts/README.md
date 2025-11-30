# プロンプト集

## 概要

新規事業・MVP開発で使用する再利用可能なプロンプトを管理します。

## フォルダ構成

| フォルダ | 内容 | 用途 |
|----------|------|------|
| `ideation/` | アイデア発想 | ブレスト、アイデア整理 |
| `analysis/` | 分析 | データ分析、市場調査 |
| `development/` | 開発 | 仕様作成、コード生成 |
| `mindset/` | マインドセット | AI対話のスタンス設定 |

## プロンプト一覧

### ideation/（アイデア発想）

| プロンプト | 用途 |
|-----------|------|
| [business-idea-generator.md](ideation/business-idea-generator.md) | ビジネスアイデアの発想・整理 |
| [persona-generator.md](ideation/persona-generator.md) | ペルソナの作成 |

### analysis/（分析）

| プロンプト | 用途 |
|-----------|------|
| [competitive-research.md](analysis/competitive-research.md) | 競合調査 |
| [data-insight.md](analysis/data-insight.md) | データからインサイト抽出 |

### development/（開発）

| プロンプト | 用途 |
|-----------|------|
| [mvp-spec-generator.md](development/mvp-spec-generator.md) | MVP仕様書の作成 |
| [code-review.md](development/code-review.md) | コードレビュー |
| [commit-message-generator.md](development/commit-message-generator.md) | コミットメッセージ生成 |
| [branch-name-generator.md](development/branch-name-generator.md) | ブランチ名生成 |

### mindset/（マインドセット）

| プロンプト | 用途 |
|-----------|------|
| [no-sugarcoating.md](mindset/no-sugarcoating.md) | 忖度無しの正直なフィードバックを求める |

---

## プロンプトの使い方

### 1. 基本的な使い方

1. 適切なプロンプトファイルを開く
2. 「プロンプト本文」セクションをコピー
3. `{placeholder}` の部分を実際の情報で置き換える
4. AIツールに入力して実行

### 2. カスタマイズ

プロジェクトに合わせてプロンプトをカスタマイズする場合：

1. 元のプロンプトをコピー
2. プロジェクト固有の情報を追加
3. 必要に応じて出力形式を調整

---

## プロンプトテンプレート

新しいプロンプトを追加する際は以下の形式で：

```markdown
---
title: プロンプト名
purpose: 何のためのプロンプトか
input: 必要な入力情報
output: 期待する出力
---

# プロンプト名

## 使用方法

いつ、どのように使うか

## プロンプト本文

\`\`\`
（実際のプロンプト）
\`\`\`

## 使用例

### 入力例
\`\`\`
（入力の具体例）
\`\`\`

### 出力例
\`\`\`
（出力の具体例）
\`\`\`

## 改善履歴

| 日付 | 変更内容 | 理由 |
|------|----------|------|
| | | |
```

---

## 改善のサイクル

1. プロンプトを使用
2. 結果を評価
3. 改善点を特定
4. プロンプトを更新
5. 改善履歴に記録

継続的に改善することで、より良い結果が得られます。



