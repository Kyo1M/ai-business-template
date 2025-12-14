---
title: top_message 下罫線をテキスト幅に合わせる
created: 2025-12-14
updated: 2025-12-14
status: done
---

## 背景
- トップメッセージ直下の罫線は、本文領域いっぱいではなく「トップメッセージのテキスト幅」に合わせたい。

## 目的（完了条件）
- `typography.styles.top_message.divider_bottom` に、罫線幅がテキスト幅に追従する指定が追加されている。

## 対象ファイル
- `prompts/design/slide-design.yaml`

## タスク（Step by Step）
- [x] (1) divider_bottom に「テキスト幅に合わせる」指定を追加（ファイル: `prompts/design/slide-design.yaml`）
- [x] (2) YAML として破綻がないことを確認（ファイル: `prompts/design/slide-design.yaml`）

## 更新履歴
- 2025-12-14: チケット作成（todo）
- 2025-12-14: divider_bottom に width_mode=fit_text / align=text_left を追加
- 2025-12-14: YAML パースで構文正常（ruby YAML.load_file）
