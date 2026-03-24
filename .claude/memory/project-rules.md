# チーム共有ルール（memory）

## コーディング規約
- 言語: プロジェクトごと（JavaScript/TypeScript/Python/Go etc.）
- フォーマッター: Prettier + ESLint（JS/TS）、black（Python）、gofmt（Go）
-  max-line-length: 100

## 環境設定
- 開発環境: Docker / asdf / direnv
- 環境変数ファイル: `.env.example` を必ずcommit
- シークレット: 絶対にcommitしない、`.gitignore` に追加

## ワークフロー
- Git: GitHub Flow（mainは保護ブランチ）
- PR: 最低1名のapprove必須
- CI: 全テスト・リンターチェック必須

## ドキュメント
- README.md: プロジェクト概要、セットアップ手順、環境変数一覧
- CHANGELOG.md: 変更履歴
- API仕様: OpenAPI/Swagger（ある場合）
