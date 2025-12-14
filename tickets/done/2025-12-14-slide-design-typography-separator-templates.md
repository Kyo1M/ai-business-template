---
title: slide-design.yaml の罫線・タイポ微調整と templates 方針の明文化
created: 2025-12-14
updated: 2025-12-14
status: done
---

## 背景
- トップメッセージ直下に「薄い灰色の罫線」を入れ、情報の区切りを明確にしたい。
- タイトル/トップメッセージのフォントサイズが大きすぎる可能性があるため、必要なら小さくしたい。
- `templates` は便利だが、内容に引きずられて自由度が下がる懸念があるため「任意（参考）」として方針を明文化したい。

## 目的（完了条件）
- トップメッセージ下に薄い灰色の罫線を引けるように、スタイルとして定義される。
- タイトル/トップメッセージのフォントサイズが過大にならないよう、基準値を調整する。
- `templates` は強制ではなく参考であることが明文化され、内容に合わせてレイアウトを選べる。

## 対象ファイル
- `prompts/design/slide-design.yaml`

## タスク（Step by Step）
- [x] (1) `top_message` の下線（罫線）スタイルを追加する（ファイル: `prompts/design/slide-design.yaml`）
- [x] (2) `slide_title` / `top_message` のサイズを微調整する（ファイル: `prompts/design/slide-design.yaml`）
- [x] (3) `templates` の利用方針（任意・参考）を明文化する（ファイル: `prompts/design/slide-design.yaml`）
- [x] (4) YAML として破綻がないことを確認する（ファイル: `prompts/design/slide-design.yaml`）

## 更新履歴
- 2025-12-14: チケット作成（todo）
- 2025-12-14: top_message の下罫線（divider_bottom）を追加、タイトル/トップメッセージのサイズを微調整、templates を参考（任意）として注記
- 2025-12-14: YAML パースで構文正常（ruby YAML.load_file）
