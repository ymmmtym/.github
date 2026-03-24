# .github

Template files.

- [README.md](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)
- [Issues](https://docs.github.com/en/issues)
- [Pull requests](https://docs.github.com/en/pull-requests)
- Contributing
- [pre-commit](https://pre-commit.com/)
- [Renovate](https://www.mend.io/free-developer-tools/renovate/)
    - `default.json`

## Claude Code

このリポジトリにはClaude Codeのプロジェクト設定テンプレートが含まれています。

### 使い方

新規プロジェクトで以下のコマンドを実行：

```bash
cd 新規プロジェクトディレクトリ
cp -r ~/.ghq/github.com/ymmmtym/.github/.claude .
```

または、`.claude/settings.json` のみ必要な場合：

```bash
mkdir -p .claude
cp ~/.ghq/github.com/ymmmtym/.github/.claude/settings.json .claude/
```

設定ファイルが有効になるのは、`.claude/` をプロジェクトルートに配置した後、`claude` コマンドを実行したときです。

### 現在のテンプレート状態（ひよこ → ムキムキ計画）

- ✅ `settings.json` - 基本権限設定
- ✅ `instructions.md` - 開発ルール（日本語対応）
- ✅ `memory/` - 共有知識（team-rules, api-reference, troubleshooting）
- ⏳ `hooks/` - 自動化フック（予定）
- ⏳ 環境別設定（dev/staging/prod）（予定）
- ⏳ MCPサーバー設定例（予定）

順次拡張予定。要望があればIssue起票 or PR投下！

## Renovate

### Usage

Add following values to `renovate.json` extends.

```json
{
    "extends": ["github>ymmmtym/.github"]
}
```
