# Marpスライド作成プロジェクト

このプロジェクトは、Marpを使用してスライドを作成し、GitHub Pagesで公開するためのものです。

## 環境要件

- Node.js (v14以上)
- npm (v6以上)

## セットアップ

1. リポジトリのクローン
```bash
git clone git@github:yuya4i/marp-study.git
cd marp-study
```

2. 依存パッケージのインストール
```bash
npm install
```

## 使用方法

### 開発モード（プレビュー）
```bash
npm start
```
ブラウザで自動的にプレビューが開きます。

### HTMLファイルの生成
```bash
npm run build
```
スライドのHTMLファイルが生成されます。

### PDFファイルの生成
```bash
npm run pdf
```
スライドのPDFファイルが生成されます。

### 監視モード
```bash
npm run watch
```
ファイルの変更を監視し、自動的にHTMLを生成します。

## スライドの構成

- 基本的な構成方法
- テキストの装飾
- 画像の挿入
- リンクの挿入
- コードの挿入
- テーブルの挿入
- リストの活用
- アニメーション効果
- カスタムCSSの活用
- 高度なレイアウト

## ブランチ戦略

- `main`: 公開用の安定版
- `feature/xxxx`: 各スライドまたは機能の作成用ブランチ

## GitHub Pages公開手順

1. リポジトリの`Settings`タブを開く
2. 左メニューから`Pages`を選択
3. `Source`を`main`ブランチに設定
4. 保存後、自動的にデプロイが開始されます

## 参考リンク

- [Marp公式サイト](https://marp.app/)
- [Marp CLI GitHubリポジトリ](https://github.com/marp-team/marp-cli)
- [GitHub Pages公式ドキュメント](https://pages.github.com/)
