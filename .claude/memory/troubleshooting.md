# トラブルシューティング集

## Claude Code関連

### 権限エラー
- **This directory is not in your allowed_directories**
  - 解決: `~/.claude/settings.json` またはプロジェクトの `.claude/settings.json` にディレクトリを追加

### ファイルが見つからない
- `Glob` が `.gitignore` を尊重する
  - 解決: `.gitignore` から除外するか、`respectGitignore: false` を設定

## 開発全般

### Node.js
- `nvm` でバージョン切り替え
- `node_modules` が巨大的: `npm ci` でクリーンインストール

### Docker
- ビルドキャッシュ: `docker build --no-cache`
- ボリュームパーミッション: `chmod 777`（開発時のみ）

## その他
- このファイルはプロジェクトごとにカスタマイズ可能
