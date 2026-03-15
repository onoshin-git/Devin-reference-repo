# deploy 契約 Stub

これは参考用 stub です。正本ではありません。

## 分けて定義すべきもの

- backend deploy
- frontend publish
- seed users
- verify
- repair

## 最低限必要な観点

- Lambda / API Gateway / DynamoDB / Bedrock
- S3 / CloudFront
- stage
- rollback
- disposable 環境かどうか
