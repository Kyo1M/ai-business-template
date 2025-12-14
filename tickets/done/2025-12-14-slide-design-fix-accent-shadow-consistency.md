---
title: slide-design.yaml のアクセント色ルール矛盾と影の不一致を解消
created: 2025-12-14
updated: 2025-12-14
status: done
---

## 背景
- `prompts/design/slide-design.yaml` 内で、アクセント色（信号色）に関するルールが矛盾しており、実装時に解釈が分かれる。
- 影（shadow）を「常に同じ」としながら、定義値が複数存在し一貫性が崩れている。

## 目的（完了条件）
- アクセント色（growth/alert/highlight）の「定義の数」と「運用上の同時使用制限」が明確になり、矛盾がない。
- 影（shadow）が 1 種類の値に統一され、「常に同じ」ルールを満たす。
- YAML として破綻しない。

## 対象ファイル
- `prompts/design/slide-design.yaml`

## タスク（Step by Step）
- [x] (1) 現状の矛盾点（アクセント/信号色）を該当行で確認し、ルールとして整合する方針へ統一（ファイル: `prompts/design/slide-design.yaml`）
- [x] (2) consistency_checklist の文言を、統一した運用ルールに合わせて修正（ファイル: `prompts/design/slide-design.yaml`）
- [x] (3) shadow 定義を 1 種類に統一（ファイル: `prompts/design/slide-design.yaml`）
- [x] (4) YAML パースで構文が正常であることを確認（ファイル: `prompts/design/slide-design.yaml`）

## 更新履歴
- 2025-12-14: チケット作成（todo）
- 2025-12-14: 作業開始（doing）
- 2025-12-14: 信号色（growth/alert/highlight）の「定義は3種・同時使用最大2種（通常1）」へルール文言を統一
- 2025-12-14: consistency_checklist の強調色チェック文言をトークン名ベースへ統一
- 2025-12-14: shadow を 1 種類（rgba 0.08）へ統一
- 2025-12-14: YAML パースで構文正常（ruby YAML.load_file）
