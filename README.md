# 🚀 MVP Business Template

新規事業・MVP開発プロジェクトのためのドキュメントテンプレート集です。

## 📋 このテンプレートについて

アイデア検証からMVPリリース、グロースまでの各フェーズで必要なドキュメントを構造化して管理できます。

### 特徴

- **フェーズ別に整理**: Discovery → Strategy → Development → Growth
- **AI連携対応**: Claude Code / Cursor等のAIツールと連携しやすい設計
- **すぐに使える**: 空のテンプレートではなく、記入例・ガイド付き
- **チェックリスト完備**: 重要な意思決定ポイントを見逃さない

## 🏁 クイックスタート

### 1. テンプレートから新規リポジトリを作成

```bash
# GitHubの「Use this template」ボタンを使用するか、
# 手動でクローンして使用
git clone https://github.com/YOUR_USERNAME/mvp-business-template.git my-new-project
cd my-new-project
rm -rf .git
git init
```

### 2. プロジェクト情報を設定

1. この `README.md` をプロジェクト用に書き換える
2. `docs/01_discovery/hypothesis.md` に最初の仮説を記入
3. `docs/01_discovery/target-persona.md` にターゲットを定義

### 3. 各フェーズのドキュメントを埋めていく

進捗に応じて各ドキュメントを更新していきます。

## 📁 リポジトリ構成

```
mvp-business-template/
├── docs/
│   ├── 00_policy/        # プロジェクト運用ルール
│   ├── 01_discovery/     # 発見・検証フェーズ
│   ├── 02_strategy/      # 戦略フェーズ
│   ├── 03_development/   # 開発フェーズ
│   ├── 04_growth/        # 成長・運用フェーズ
│   └── 99_archive/       # アーカイブ
│
├── templates/            # 再利用可能なテンプレート
├── prompts/              # AIプロンプト集
├── notes/                # メモ・議事録
│   ├── meetings/         # 議事録
│   ├── ideas/            # アイデアメモ
│   ├── research/         # 調査メモ
│   └── misc/             # その他
└── checklists/           # チェックリスト
```

## 📚 ドキュメント一覧

### 00_policy/ - 運用ルール
| ファイル | 内容 |
|----------|------|
| [document-rules.md](docs/00_policy/document-rules.md) | ドキュメント管理ルール |
| [git-workflow.md](docs/00_policy/git-workflow.md) | Git運用フロー |
| [ai-usage-guide.md](docs/00_policy/ai-usage-guide.md) | AI活用ガイド |

### 01_discovery/ - 発見・検証フェーズ
| ファイル | 内容 |
|----------|------|
| [hypothesis.md](docs/01_discovery/hypothesis.md) | 仮説管理 |
| [target-persona.md](docs/01_discovery/target-persona.md) | ターゲット・ペルソナ |
| [problem-statement.md](docs/01_discovery/problem-statement.md) | 課題定義 |
| [competitive-analysis.md](docs/01_discovery/competitive-analysis.md) | 競合分析 |

### 02_strategy/ - 戦略フェーズ
| ファイル | 内容 |
|----------|------|
| [value-proposition.md](docs/02_strategy/value-proposition.md) | バリュープロポジション |
| [business-model.md](docs/02_strategy/business-model.md) | ビジネスモデル |
| [mvp-definition.md](docs/02_strategy/mvp-definition.md) | MVP定義 |
| [roadmap.md](docs/02_strategy/roadmap.md) | ロードマップ |

### 03_development/ - 開発フェーズ
| ファイル | 内容 |
|----------|------|
| [requirements.md](docs/03_development/requirements.md) | 要件定義 |
| [design-spec.md](docs/03_development/design-spec.md) | 設計仕様 |
| [tech-stack.md](docs/03_development/tech-stack.md) | 技術選定 |

### 04_growth/ - 成長・運用フェーズ
| ファイル | 内容 |
|----------|------|
| [metrics.md](docs/04_growth/metrics.md) | 計測指標（KPI） |
| [experiment-log.md](docs/04_growth/experiment-log.md) | 実験・A/Bテスト記録 |
| [learnings.md](docs/04_growth/learnings.md) | 学び・気づき |

## ✅ チェックリスト

| ファイル | タイミング |
|----------|------------|
| [project-kickoff.md](checklists/project-kickoff.md) | プロジェクト開始時 |
| [mvp-launch.md](checklists/mvp-launch.md) | MVPリリース前 |
| [pivot-decision.md](checklists/pivot-decision.md) | ピボット検討時 |

## 🤖 AI連携

このテンプレートはAIツール（Claude Code、Cursor等）との連携を前提に設計されています。

- `CLAUDE.md`: AI向けのプロジェクト説明・ルール
- `prompts/`: 各フェーズで使えるプロンプト集

詳細は [AI活用ガイド](docs/00_policy/ai-usage-guide.md) を参照してください。

## 📝 テンプレートファイル

| ファイル | 用途 |
|----------|------|
| [hearing-sheet.md](templates/hearing-sheet.md) | 顧客ヒアリング |
| [weekly-report.md](templates/weekly-report.md) | 週次進捗レポート |
| [decision-log.md](templates/decision-log.md) | 意思決定の記録 |
| [retrospective.md](templates/retrospective.md) | 振り返り |
| [meeting-notes.md](templates/meeting-notes.md) | 議事録 |

## 📂 メモ・議事録

`notes/` フォルダでメモや議事録を管理します。詳細は [notes/README.md](notes/README.md) を参照。

| フォルダ | 内容 |
|----------|------|
| [meetings/](notes/meetings/) | 議事録・ミーティングメモ |
| [ideas/](notes/ideas/) | アイデアメモ・ブレスト記録 |
| [research/](notes/research/) | 調査・リサーチメモ |
| [misc/](notes/misc/) | その他のメモ |

## 🔄 推奨ワークフロー

```
Week 1-2: Discovery
├── 仮説を立てる (hypothesis.md)
├── ターゲットを定義 (target-persona.md)
└── 課題を明確化 (problem-statement.md)

Week 3-4: Strategy
├── バリュープロポジション (value-proposition.md)
├── ビジネスモデル (business-model.md)
└── MVP定義 (mvp-definition.md)

Week 5-8: Development
├── 要件定義 (requirements.md)
├── 設計・実装
└── MVPリリース

Week 9+: Growth
├── データ計測 (metrics.md)
├── 実験・改善 (experiment-log.md)
└── 学びの蓄積 (learnings.md)
```

## 📄 ライセンス

MIT License - 自由にご利用ください。

---

**Made with ❤️ for startup builders**



