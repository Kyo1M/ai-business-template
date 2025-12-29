---
title: Assets フォルダ
created: YYYY-MM-DD
updated: YYYY-MM-DD
status: approved
---

# Assets フォルダ

## 概要

このフォルダには、プロジェクトで使用するファイル（PDF、PowerPoint、画像など）を格納します。

---

## フォルダ構成

```
assets/
├── competitors/    # 競合調査で収集した資料
├── sales/          # 営業資料（PowerPoint等）
└── README.md
```

---

## competitors/ - 競合資料

競合調査で収集したPDF、スクリーンショット、資料等を保存

**ファイル命名規則**:
- `{競合名}-{資料種類}-{日付}.{拡張子}`
- 例: `techstar-pricing-2025-12.pdf`
- 例: `innovate-inc-lp-screenshot-2025-12.png`

**関連ドキュメント**:
- 競合サマリー: `docs/01_discovery/competitive-analysis.md`
- 個別競合プロファイル: `docs/01_discovery/competitors/`

---

## sales/ - 営業資料

営業・提案で使用するPowerPoint、PDFなどを保存

**ファイル例**:
- `sales-deck.pptx` - メイン営業資料
- `sales-deck.pdf` - PDF版（送付用）
- `one-pager.pdf` - 1枚サマリー

**関連ドキュメント**:
- スライド構成: `docs/02_strategy/sales-deck.md`
- 提案書テンプレート: `templates/proposal.md`

---

## 注意事項

- **機密情報**: 顧客固有の情報が含まれるファイルは`.gitignore`に追加を検討
- **ファイルサイズ**: 大きなファイルはGit LFSの使用を検討
- **命名規則**: 日本語ファイル名は避け、小文字英数字とハイフンを使用

---

## 更新ログ

| 日付 | 更新内容 |
|------|----------|
| YYYY-MM-DD | 初版作成 |

