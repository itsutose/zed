# Zed Settings

Zed エディタの設定ファイル。

## セットアップ

```bash
# シンボリックリンクを作成
ln -s ~/dotfiles/zed/settings.json ~/.config/zed/settings.json
```

## 設定内容

### Python LSP

- **Language Server**: basedpyright (Zed v0.204.0+ built-in)
- **Python Path**: `.venv/bin/python` (プロジェクトの venv を自動検出)
- **診断モード**: デフォルト（openFilesOnly）

### その他

- **Base Keymap**: Cursor
- **Theme**: Ayu Dark / Ayu Light (system mode)
- **Autosave**: 1秒後に自動保存
- **Terminal**: バーカーソル、選択時自動コピー

## 注意事項

### ワークツリーの信頼

新しいプロジェクトを開く際は、Zed がセキュリティ上ワークツリーの信頼を求めます。
LSP を起動するには、必ず「Trust this folder」を選択してください。

### Python バージョン検出

`.venv/bin/python` を指定することで、basedpyright が自動的に Python バージョンを検出します。
`pyrightconfig.json` に `pythonVersion` を明示的に書く必要はありません。
