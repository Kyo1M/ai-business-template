---
title: slide-design.yaml のスタイル一貫性強化
created: 2025-12-14
updated: 2025-12-14
status: done
---

## 背景
- スライド生成時に、背景色・文字色・見出しスタイルなどが微妙にブレることがある。
- `prompts/design/slide-design.yaml` に「必ず守るスタイル規約（Must/Must Not）」と「生成後の自己検証」を追加し、一貫した見た目を厳守させる。

## 目的（完了条件）
- 背景は常に白（#FFFFFF）で統一される。
- タイトル/トップメッセージ/本文/補足/ページ番号のスタイルが固定され、スライド間でブレない。
- 使用色はパレットのトークン参照に限定され、任意の色追加を禁止できる。
- 生成後に、ルール違反がないかチェックできる（チェックリストがある）。

## 対象ファイル
- `prompts/design/slide-design.yaml`

## タスク（Step by Step）
- [x] (1) 現状のスタイル定義の揺れ要因（曖昧さ）を特定する（ファイル: `prompts/design/slide-design.yaml`）
- [x] (2) グローバル固定ルール（背景/配色/文字/余白/整列/禁止事項）を追記する（ファイル: `prompts/design/slide-design.yaml`）
- [x] (3) UIコンポーネント規約（カード/図形/線/アイコン/強調）を追記する（ファイル: `prompts/design/slide-design.yaml`）
- [x] (4) 自己検証チェックリスト（生成後に必ず確認）を追記する（ファイル: `prompts/design/slide-design.yaml`）
- [x] (5) YAML として破綻がないことを確認する（ファイル: `prompts/design/slide-design.yaml`）

## 更新履歴
- 2025-12-14: チケット作成、作業開始（doing）
- 2025-12-14: style一貫性のための絶対ルール/コンポーネント規約/チェックリストを `prompts/design/slide-design.yaml` に追加
- 2025-12-14: YAML パースで構文正常（ruby YAML.load_file）
