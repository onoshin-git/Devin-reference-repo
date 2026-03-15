# Devin Upload Definition

この文書は、将来 Devin に handoff パッケージを渡すときに含めるべき情報の基準をまとめた参考資料です。  
**この文書自体も reference であり、正本ではありません。**

## 基本原則
- 要約だけではなく、実装に使える contract を渡す
- `authoritative` と `reference` と `archive` を明確に分離する
- `dry-run` や `old` は正本扱いしない
- HTML 遷移、API、データ、handler、deploy を個別に定義する
- 曖昧な項目は質問させるのではなく、先に定義する

## Devin に渡すべき情報
### 1. 入口ルール
- `AGENTS.md`
- `START_HERE.md`
- 読む順序
- `authoritative` / `reference` / `archive` の区分

### 2. 画面契約
- 画面一覧
- 画面遷移
- 画面ごとの機能
- DOM id / class
- 画面と API / backend / data の対応

### 3. API 契約
- 全 endpoint の request / response / error
- nested schema
- level ごとの差分
- history / admin の exact shape

### 4. データ契約
- DynamoDB テーブル設計
- PK / SK ルール
- attribute 型
- update / preserve rule
- CSV exact contract

### 5. backend 契約
- handler 一覧
- handler ごとの責務
- 使用 table
- 使用 library
- Bedrock 呼び出し箇所

### 6. frontend 契約
- HTML ごとの責務
- JS ごとの責務
- sessionStorage key
- redirect / auth / unlock rule
- API call order

### 7. AWS / deploy 契約
- Lambda
- API Gateway
- DynamoDB
- Bedrock
- S3
- CloudFront
- deploy / seed / repair / verify の exact contract

### 8. テスト契約
- unit test 観点
- property test 観点
- frontend parity 観点
- acceptance criteria

### 9. 既知失敗パターン
- Codex / Gemini / Devin の失敗知見
- 認識ずれ
- 再発防止ルール

## Mermaid で定義したい図
- システム構成図
- 画面遷移図
- 画面項目と API / DB の対応図
- auth flow
- progression flow
- deploy flow
- repair flow

## 注意
この文書は、正本の contract を設計する際の参考用メモです。  
ここに書いてある内容をそのまま deploy 前提の仕様として使うのではなく、別途 authoritative な文書へ落とし込んでください。
