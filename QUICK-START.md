# ⚡ クイックスタートガイド

**10分でプロジェクトを始める** ためのガイドです。

---

## Step 1: リポジトリをセットアップ（2分）

```bash
# テンプレートからプロジェクトを作成
git clone https://github.com/YOUR_USERNAME/mvp-business-template.git my-project
cd my-project
rm -rf .git
git init
git add .
git commit -m "Initial commit from template"
```

---

## Step 2: 最初に埋める3つのファイル（5分）

### 1️⃣ 仮説を書く

📄 `docs/01_discovery/hypothesis.md`

```markdown
### H1: ターゲット仮説
| **仮説** | 〇〇な人がターゲットである |
| **根拠** | △△だから |
| **状態** | 🔴 未検証 |

### H2: 課題仮説
| **仮説** | ターゲットは「□□」という課題を持っている |
| **根拠** | △△だから |
| **状態** | 🔴 未検証 |
```

### 2️⃣ ターゲットを定義する

📄 `docs/01_discovery/target-persona.md`

最低限これだけ埋める：
- **誰？**: 年齢、職業、状況
- **何に困っている？**: 課題・ペイン
- **なぜ既存の解決策ではダメ？**

### 3️⃣ このREADMEを書き換える

📄 `README.md`

```markdown
# プロジェクト名

## 何を作るか
一言で説明

## 誰のために
ターゲット顧客

## 解決する課題
どんな課題を解決するか
```

---

## Step 3: 開発を始める前に（3分）

### チェックリストを確認

📄 `checklists/project-kickoff.md` を開いて、最低限これをチェック：

- [ ] 仮説を書いた
- [ ] ターゲットを定義した
- [ ] 課題を言語化した

---

## 🎯 これだけでOK！

上記3ステップが完了すれば、プロジェクトを開始できます。

その後は、プロジェクトの進行に合わせて各ドキュメントを埋めていってください。

---

## 次のステップ

### Discovery フェーズ

1. ターゲット顧客5人以上と話す
2. 仮説を検証して `hypothesis.md` を更新
3. 課題の優先順位をつける

### Strategy フェーズ

1. `mvp-definition.md` でMVPを定義
2. `roadmap.md` でスケジュールを決める
3. `business-model.md` で収益モデルを設計

### Development フェーズ

1. `requirements.md` で要件を整理
2. `tech-stack.md` で技術を選定
3. 開発開始 🚀

---

## 困ったときは

| やりたいこと | 参照先 |
|--------------|--------|
| AI（Claude/Cursor）の使い方 | `docs/00_policy/ai-usage-guide.md` |
| ドキュメントのルール | `docs/00_policy/document-rules.md` |
| フェーズ移行の判断 | `checklists/phase-transition.md` |
| ピボットの判断 | `checklists/pivot-decision.md` |
| プロンプト集 | `prompts/README.md` |

---

## テンプレート構造（参考）

```
docs/
├── 00_policy/        ← ルール（最初に読む）
├── 01_discovery/     ← 仮説・ターゲット・課題
├── 02_strategy/      ← 戦略・MVP定義
├── 03_development/   ← 要件・設計・技術
├── 04_growth/        ← 指標・実験・学び
└── 99_archive/       ← 古いドキュメント

notes/                ← メモ・議事録
templates/            ← 再利用テンプレート
prompts/              ← AIプロンプト集
checklists/           ← チェックリスト
```

---

**さあ、始めましょう！** 🚀

