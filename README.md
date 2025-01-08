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

### PowerPointファイルの生成
```bash
marp slides/index.md --pptx
```
スライドのPowerPointファイル（.pptx）が生成されます。
※ PowerPointで開く場合、一部のアニメーションやカスタムCSSが完全に再現されない場合があります。

### 監視モード
```bash
npm run watch
```
ファイルの変更を監視し、自動的にHTMLを生成します。

## テーマのカスタマイズ

### テーマファイルの作成
1. `themes`ディレクトリを作成
```bash
mkdir themes
```

2. カスタムテーマファイル（例：`custom.css`）を作成
```css
/* themes/custom.css */
@theme custom {
  /* ベーステーマの継承 */
  @import 'default';

  /* 全体のスタイル */
  section {
    background: #ffffff;
    color: #333333;
    font-family: 'Arial', sans-serif;
  }

  /* 見出しのスタイル */
  h1 {
    color: #2c3e50;
    font-size: 2.5em;
  }

  h2 {
    color: #34495e;
    font-size: 2em;
  }

  /* リストのスタイル */
  ul, ol {
    margin: 1em 0;
    line-height: 1.6;
  }

  /* コードブロックのスタイル */
  code {
    background: #f8f9fa;
    padding: 0.2em 0.4em;
    border-radius: 3px;
  }

  /* 特定のクラスのスタイル */
  section.lead {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
  }
}
```

### テーマの適用
1. スライドのYAMLフロントマターでテーマを指定
```markdown
---
marp: true
theme: custom
---
```

2. CLIでテーマを指定して実行
```bash
marp --theme-set ./themes/custom.css slides/index.md
```

### テーマの共有
1. テーマファイルをnpmパッケージとして公開
2. package.jsonに依存関係として追加
3. `@import`でテーマを継承して拡張可能

### テーマのベストプラクティス
- 変数を活用してカラーパレットを定義
- メディアクエリでレスポンシブ対応
- スコープ付きスタイルで部分的な適用
- コメントで各スタイルの目的を明記

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
