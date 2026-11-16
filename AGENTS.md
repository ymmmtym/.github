# AGENTS.md

`ymmmtym/.github` で作業する AI エージェント向けの指示です。

## このリポジトリの役割

`ymmmtym` のリポジトリ共通デフォルト設定です。他のリポジトリが継承・検証で
利用する設定を置きます。コピーして使うテンプレート集ではありません。

## レイアウト

- `default.json` — Renovate shared preset。`github>ymmmtym/.github` として継承される。
- `renovate.json` — このリポジトリ自身の Renovate 設定。
- `.github/workflows/actions.lock` — ワークフロー依存の機械生成 lockfile。
- `.github/workflows/verify-actions-lock.yml` — PR と `main` への push で lockfile を検証。
- `.github/ACTIONS_LOCK.md` — lockfile の更新・検証手順。
- `.github/ISSUE_TEMPLATE/` — Issue テンプレート。
- `README.md` — リポジトリ概要。

## ルール

### Actions lockfile

- `.github/workflows/actions.lock` を手で編集しない。
- ワークフローの `uses:` を変更したら、同じコミットで lockfile を再生成する。

  ```sh
  gh extension install github/gh-actions-lock --pin v0.4.1
  gh actions-lock --no-narrow
  gh actions-lock --verify
  ```

  lockfile を更新せずに `uses:` を編集すると `Verify Actions lockfile` が失敗する。
- 拡張のバージョンは CI と同じ `v0.4.1` に固定する。

### コミットと PR

- コミットメッセージは英語・命令形（例: `Add feature`、`Fix bug`）。
- ベースブランチは `main`。
- PR 説明は日本語でよい。変更点を明確に書く。
- ブランチ名は `feature/`、`fix/`、`docs/`、`chore/` プレフィックスを使う。

### 言語

- ドキュメントと PR 説明は日本語でよい。技術用語は英語のままにする。

### ローカルの作業メモ

- `.openhands/memory/` などのエージェント作業メモはこのリポジトリの一部ではない。
  コミットしない（`.gitignore` で除外済み）。
