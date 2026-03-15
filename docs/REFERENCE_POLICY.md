---
title: 参照ポリシー
---

# 参照ポリシー

## 基本方針

- `authoritative`
  - 実際に構築や実装の正本として使う文書群
- `reference`
  - 今回の repo のような参考用資料、stub、図、サンプル
- `archive`
  - `old/` のような過去版、差分比較用、保存用の資料

## この repo における扱い

- `references/` は reference
- `samples/` は reference
- `old/` は archive
- この repo 自体は authoritative ではない

## 守るべきルール

1. `references/` や `old/` の内容をそのまま deploy 用仕様にしない
2. sample CSV を見たら exact header は authoritative 側へ移す
3. Mermaid 図は理解補助として使い、実装契約は別途明文化する
4. reference repo は「認識ずれを防ぐ」ための材料として使う
