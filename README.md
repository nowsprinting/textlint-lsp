# textlint-lsp

[textlint](https://textlint.github.io/) を LSP（Language Server Protocol）で使えるようにするサーバーです。Zed、Neovim など LSP 対応エディタで日本語文章校正ができます。

## インストール

```bash
npm install -g textlint-lsp
```

## 使い方

プロジェクトに textlint とルールをセットアップしてください。

```bash
npm install --save-dev textlint @textlint/markdown
npm install --save-dev @textlint-ja/no-synonyms prh
```

`.textlintrc.json` を作成：

```json
{
  "plugins": { "@textlint/markdown": true },
  "rules": {
    "@textlint-ja/no-synonyms": true,
    "prh": { "rulePaths": ["prh.yml"] }
  }
}
```

### Zed

[zed-textlint.zip](https://yasutakeyohei.com/zed-textlint.zip) をダウンロードし、Dev Extension としてインストールしてください。

1. ダウンロードして展開
2. `Ctrl+Shift+P` → `zed: install dev extension` → 展開したフォルダを指定

## できること

- 文字入力のたびに自動校正
- 波線で問題箇所を表示
- `Ctrl+.` で修正候補を表示・適用
- ルール単位の無効化

## ライセンス

MIT
