# Marp Study Project

このリポジトリは、AI（Claude）によって作成された Marp を使用したスライド作成プロジェクトです。

## プロジェクトについて

このプロジェクトは、Marpを使用してスライドを作成し、GitHub Pagesで公開することを目的としています。
すべてのコード、設定、およびドキュメントはAIによって生成されています。

## 導入方法

1. リポジトリのクローン
```bash
git clone git@github:yuya4i/marp-study.git
cd marp-study
```

2. 依存関係のインストール
```bash
npm install
```

## 使い方

### スライドの作成・編集

1. プレビューモード起動
```bash
npm run start
```

2. HTMLファイルの生成
```bash
npm run build
```

3. PDFファイルの生成
```bash
npm run pdf
```

4. ファイル変更の監視
```bash
npm run watch
```

### テーマの使用

1. テーマのプレビュー
```bash
npm run theme-example:server
```

2. テーマを適用したHTMLの生成
```bash
npm run theme-example
```

3. テーマを適用したPDFの生成
```bash
npm run theme-example:pdf
```

4. テーマを適用したPPTXの生成
```bash
npm run theme-example:pptx
```

## 機能一覧

### 基本機能
- スライドの基本的な構成
- テキストの装飾（太字、斜体、下線、打消し線）
- 画像の挿入とサイズ調整
- リンクの挿入
- コードブロックの挿入
- テーブルの作成
- リストの作成

### 高度な機能
- アニメーション効果
  - フェードイン
  - スライドイン
  - ズーム
  - 回転
  - バウンス
- カスタムCSSによるスタイリング
- レスポンシブデザイン
- 様々なレイアウトパターン

## プロジェクト構成

```
marp/
├── config.ini        # プロジェクト設定
├── package.json      # 依存関係と実行スクリプト
├── slides/          # スライドファイル
│   └── index.md     # メインスライド
└── themes/          # テーマファイル
    ├── modern.css   # カスタムテーマ
    └── example.md   # テーマ使用例
```

## 技術スタック

- Marp CLI v4.0.4
- Node.js
- カスタムCSS
- Markdown

## 参照元

- [Marp公式サイト](https://marp.app/)
- [Marp CLI GitHubリポジトリ](https://github.com/marp-team/marp-cli)
- [GitHub Pagesの公式ドキュメント](https://pages.github.com/)

## 注意事項

このプロジェクトはAI（Claude）によって自動生成されたものです。コードやドキュメントの品質は人間の確認とレビューを推奨します。

## ライセンス

ISC License
