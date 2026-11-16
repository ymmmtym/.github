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

### Issue templates

`.github/ISSUE_TEMPLATE/` に bug report / feature request / custom を配置しています。

## 参考

- [README](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)
- [Issues](https://docs.github.com/en/issues)
- [Pull requests](https://docs.github.com/en/pull-requests)
- [Renovate](https://www.mend.io/free-developer-tools/renovate/)
- [gh-actions-lock](https://github.com/github/gh-actions-lock)

## エージェント向け

このリポジトリで作業する AI エージェントは [AGENTS.md](AGENTS.md) を参照してください。
