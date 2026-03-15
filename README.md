# Devin Reference Repository

このリポジトリは **Devin に渡す handoff 一式を設計・整理するための参考用リポジトリ** です。  
**このリポジトリ自体は正本ではなく、参考資料・stub・テンプレートを置くための場所** です。

## 目的
- Devin に渡すべき情報の粒度を整理する
- `authoritative` と `reference` と `archive` の分離方針を共有する
- 画面、API、データ、deploy、テストの各観点で最低限必要な情報を残す
- 今後の handoff、RAG、レビュー観点の参考にする

## この repo の前提
- `references/` は参考用 stub です
- `old/` は archive です
- `samples/` は exact header や sample row の参考です
- 実案件で使う正本は別 repo または別フォルダで管理してください

## 推奨構成

```text
Devin-reference-repo/
  AGENTS.md
  README.md
  CONTRIBUTING.md
  LICENSE
  .gitignore
  devin-upload-definition.md
  docs/
    index.md
    START_HERE.md
    READ_ORDER.md
    REFERENCE_POLICY.md
  diagrams/
    system_context.mmd
    screen_flow.mmd
    deploy_flow.mmd
  templates/
    README.md
    backend/
    frontend/
    tests/
  samples/
    users.csv
    pass_status.csv
  references/
    contracts/
      screen_contract_stub.md
      api_contract_stub.json
      data_contract_stub.json
      backend_contract_stub.md
      frontend_contract_stub.md
    screens/
      screen_to_api_db_mapping_stub.md
    deploy/
      deploy_contract_stub.md
      repair_contract_stub.md
    tests/
      test_contract_stub.json
  .github/
    ISSUE_TEMPLATE/
      bug_report.md
      improvement_request.md
      config.yml
    pull_request_template.md
  old/
```

## 使い方
1. `AGENTS.md` と `docs/START_HERE.md` を読む
2. `docs/READ_ORDER.md` に従って必要な参考ファイルだけ読む
3. `references/` の stub を参考にして正本用の contract を別管理で作る
4. `diagrams/` と `samples/` を参考に不足観点を補う
5. 実際の構築では `authoritative` と `reference` を必ず分離する

## GitHub Pages での公開

この repo は `docs/` を入口にした GitHub Pages 用の構成も持っています。

### 公開方法
1. GitHub に push する
2. Repository Settings を開く
3. Pages の Source を `Deploy from a branch` にする
4. Branch を `main`、Folder を `/docs` にする
5. 保存後、`docs/index.md` を入口にしたドキュメントサイトとして公開する

### Pages の入口
- `docs/index.md`
- `docs/START_HERE.md`
- `docs/READ_ORDER.md`
- `docs/REFERENCE_POLICY.md`

### 補足
- Mermaid は Pages 用レイアウトで表示する想定です
- `devin-upload-definition.md` もナビゲーションから辿れるようにしています

## 注意
この repo は「どういう情報を Devin に渡すべきか」を整理するための参考資料です。  
ここにある stub や sample をそのまま本番 deploy して使うことは想定していません。
