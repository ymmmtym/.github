# .github

`ymmmtym` のリポジトリ共通デフォルト設定です。

コピーして使うテンプレート集ではありません。各リポジトリが「継承」または
「機械検証」で利用する設定だけを置いています。

## 内容

### Renovate shared preset

`default.json` を各リポジトリの `renovate.json` から継承させます。

```json
{
    "extends": ["github>ymmmtym/.github"]
}
```

### GitHub Actions dependency lockfile

`.github/workflows/actions.lock` がワークフローの `uses:` を検証済みコミットに固定します。
`Verify Actions lockfile` ワークフローが PR と `main` への push で検証を実行します。
更新・検証の手順は [.github/ACTIONS_LOCK.md](.github/ACTIONS_LOCK.md) を参照してください。

### デフォルトコミュニティヘルスファイル

`.github` リポジトリ（public）に置くと、独自ファイルを持たない全リポジトリへ継承されます。

- `.github/ISSUE_TEMPLATE/` — bug report / feature request / custom と `config.yml`
- `SECURITY.md` — 脆弱性報告ポリシー

<!-- coderabbit-ai-generated:v1 -->

<!-- coderabbit-ai-generated-section:v1:7a76c16ca74d4d7976a643ea6cefeccbbf6a1c1e8fa046de50e31f6d7f48dd2e -->

脆弱性の報告は対象リポジトリの **Security タブ → Security policy** を確認してください。
独自のポリシーが優先されるため、共通の `config.yml` に固定のポリシーリンクは置きません。

<!-- /coderabbit-ai-generated:v1 -->

継承されたファイルは各リポジトリのファイル一覧・Git 履歴・clone には含まれません。

### 再利用可能ワークフロー

`.github/workflows/reusable-verify-actions-lock.yml` は他リポジトリから呼び出せます。

<!-- coderabbit-ai-generated:v1 -->

<!-- coderabbit-ai-generated-section:v1:b8fef1e960e841951f563b2be3e0c69f78609504731c04bd1edc62076c4fe172 -->

```yaml
jobs:
  verify:
    uses: ymmmtym/.github/.github/workflows/reusable-verify-actions-lock.yml@main
```

<!-- /coderabbit-ai-generated:v1 -->

## 参考

- [README](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)
- [Issues](https://docs.github.com/en/issues)
- [Pull requests](https://docs.github.com/en/pull-requests)
- [Renovate](https://www.mend.io/free-developer-tools/renovate/)
- [gh-actions-lock](https://github.com/github/gh-actions-lock)

## エージェント向け

このリポジトリで作業する AI エージェントは [AGENTS.md](AGENTS.md) を参照してください。
