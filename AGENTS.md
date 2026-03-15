# Devin Reference AGENTS

このリポジトリは **参考用** です。  
**ここにある contract や stub は正本ではありません。**

## 最初に読む順序
1. `README.md`
2. `docs/START_HERE.md`
3. `docs/READ_ORDER.md`
4. `docs/REFERENCE_POLICY.md`
5. 必要に応じて `devin-upload-definition.md`
6. その後に `references/` と `diagrams/` を読む

## ルール
- `references/` は参考用 stub
- `old/` は archive
- `samples/` は exact header と sample row の参考
- 実装の正本は別管理にする
- `references/` や `old/` の内容をそのまま本番実装に使わない
- 仕様を確定するときは別途 `authoritative` な contract を作る

## 目的
- Devin に渡す情報の粒度を揃える
- 画面遷移、API、データ、deploy、テストの観点漏れを減らす
- `dry-run` や `archive` を正本扱いしないようにする
