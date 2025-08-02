
# Simple Commit and Push Action

リポジトリ内の変更を自動でコミット＆プッシュするシンプルな GitHub Action です。

## 使い方（例）

以下の内容をワークフローに追加してください。

```yaml
jobs:
  your-job:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4

      - name: Commit and Push
        uses: satt-dots/simple-commit-and-push@v1
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
```

### パラメータ

| 名前            | 必須   | デフォルト値          | 説明                                      |
|-----------------|--------|-----------------------|-------------------------------------------|
| `github-token`    | 必須   | なし                  | GitHub のトークン。 |
| `commit-message`  | 任意   | Auto commit           | コミットメッセージ |
| `user-email`      | 任意   | <action@github.com>     | コミット Author の email |
| `user-name`       | 任意   | GitHub Action         | コミット Author 名 |
