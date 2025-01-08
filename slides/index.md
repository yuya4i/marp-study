---
marp: true
theme: uncover
paginate: true
header: "Marpスライド作成ガイド"
footer: "© 2024 Marp Study"
size: 16:9
style: |
  section {
    background-color: #ffffff;
    font-size: 1.5em;
    padding: 40px;
    width: 100%;
    height: 100%;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  /* アニメーション定義 */
  @keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
  }

  @keyframes slideIn {
    from { transform: translateX(-100%); opacity: 0; }
    to { transform: translateX(0); opacity: 1; }
  }

  @keyframes zoomIn {
    from { transform: scale(0); opacity: 0; }
    to { transform: scale(1); opacity: 1; }
  }

  @keyframes rotateIn {
    from { transform: rotate(-360deg); opacity: 0; }
    to { transform: rotate(0); opacity: 1; }
  }

  @keyframes bounce {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-30px); }
  }

  /* アニメーションクラス */
  section.animate-fade * {
    animation: fadeIn 2s ease-in;
  }

  section.animate-slide * {
    animation: slideIn 1.5s ease-out;
  }

  section.animate-zoom * {
    animation: zoomIn 1s cubic-bezier(0.4, 0, 0.2, 1);
  }

  section.animate-rotate * {
    animation: rotateIn 1.5s ease-in-out;
  }

  section.animate-bounce * {
    animation: bounce 1s cubic-bezier(0.36, 0, 0.66, -0.56) 3;
  }

  /* 組み合わせアニメーション */
  section.animate-combined * {
    animation: 
      fadeIn 1s ease-in,
      slideIn 1.5s ease-out,
      bounce 2s cubic-bezier(0.36, 0, 0.66, -0.56) 2;
  }
  h1 {
    color: #2c3e50;
    font-size: 2.5em;
  }
  h2 {
    color: #34495e;
    font-size: 2em;
  }
  h3 {
    font-size: 1.8em;
  }
  ul, ol {
    margin: 1em 0;
    line-height: 1.6;
  }
  code {
    font-size: 0.9em;
  }
  table {
    font-size: 0.9em;
  }
  .grid-container {
    display: grid;
    gap: 1em;
    margin: 1em 0;
  }
  .card {
    padding: 1em;
    border-radius: 8px;
    background: #f8f9fa;
  }
---

# Marpスライド作成ガイド <!-- fit -->

基本から応用まで <!-- fit -->

<!-- _footer: "スライド 1 / 20" -->

---

<!-- _class: lead -->
## 目次

1. 基本構成
2. テキスト装飾
3. メディア挿入
4. レイアウト
5. アニメーション

---

<!-- _class: lead -->
## 1. 基本構成

- 見出し（h1, h2, h3）の使用方法
- 本文とフッターの配置
- テーマ設定（`theme: uncover`）

---

## 2. テキストの装飾

- **太字** と *斜体*
- ~~打消し線~~ と <u>下線</u>
- `コードインライン`
- <span style="color: red;">色付きテキスト</span>

---

## 3. メディアの挿入

### 画像

![width:500px](https://raw.githubusercontent.com/marp-team/marp/master/marp.png)

画像のサイズと位置を調整可能

---

## リンクの挿入

[Marp公式サイト](https://marp.app/)

<a href="https://github.com/marp-team/marp" style="
  display: inline-block;
  padding: 10px 20px;
  background: #0366d6;
  color: white;
  text-decoration: none;
  border-radius: 5px;
">GitHubリポジトリ</a>

---

## コードの挿入

```python
def hello_world():
    print("Hello, Marp!")
```

```javascript
console.log('Hello from JavaScript!');
```

---

## テーブルの挿入

| 機能 | 説明 | 難易度 |
|:-----|:-----|:------:|
| 基本構成 | スライドの基本設定 | ★ |
| テーマ設定 | デザインのカスタマイズ | ★★ |
| アニメーション | 動的な表現 | ★★★ |

---

## リストの活用

1. 番号付きリスト
   1. サブリスト1
   2. サブリスト2
2. 次の項目

- 箇条書きリスト
  - ネストされたリスト
    - さらにネスト

---

<!-- _class: lead -->
## アニメーション効果集

5つの基本アニメーション

---

<!-- _class: animate-fade -->

## 1. フェードイン効果

テキストがゆっくりと浮かび上がります

---

<!-- _class: animate-slide -->

## 2. スライドイン効果

- 左から右へスライドイン
- アニメーション時間: 1.5秒
- イージング: ease-out

---

<!-- _class: animate-zoom -->

<div class="zoom-container">

## 3. ズーム効果

要素が中心から拡大表示されます

</div>

---

<!-- _class: animate-rotate -->

<div class="rotate-element">

## 4. 回転効果

要素が回転しながら表示されます

</div>

---

<!-- _class: animate-bounce -->

<div class="bounce-element">

## 5. バウンス効果

要素が上下にバウンドします

</div>

---

<!-- _class: lead -->
## アニメーション組み合わせ例

<!-- _class: animate-combined -->

<div class="combined-animation">

### 複数のアニメーションを組み合わせることも可能です

- フェードイン
- スライドイン
- バウンス

</div>

---

# 高度なレイアウト集

---

### レイアウト1: 2カラムグリッド

<div style="
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
  margin: 1rem auto;
  max-width: 95%;
  padding-top: 0;
">
<div style="
  background: #f8f9fa;
  padding: 1.5rem;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  font-size: 0.8em;
  height: 150px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
">

#### 基本機能
- シンプルな操作性
- 直感的なインターフェース

</div>
<div style="
  background: #f8f9fa;
  padding: 1.5rem;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  font-size: 0.8em;
  height: 150px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
">

#### 拡張機能
- カスタマイズ可能
- プラグイン対応

</div>
</div>

---

### レイアウト2: ヒーローセクション

<div style="
  height: 60vh;
  background: linear-gradient(45deg, #4a90e2, #50e3c2);
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 15px;
  padding: 20px;
">
<div style="text-align: center;">

### 大見出し
#### サブタイトル
詳細な説明文をここに記載します

</div>
</div>

---

### レイアウト3: タイムライン表示

<div style="display: flex; flex-direction: column; gap: 20px;">
<div style="
  position: relative;
  padding-left: 30px;
  border-left: 2px solid #4a90e2;
">

### 2024年
主要な出来事1

</div>
<div style="
  position: relative;
  padding-left: 30px;
  border-left: 2px solid #4a90e2;
">

### 2025年
主要な出来事2

</div>
</div>

---

### レイアウト4: カード型レイアウト

<div style="
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 15px;
  margin: 20px 0;
">
<div style="background: white; padding: 15px; border-radius: 8px; box-shadow: 0 2px 5px rgba(0,0,0,0.1);">

#### カード1
コンテンツ説明

</div>
<div style="background: white; padding: 15px; border-radius: 8px; box-shadow: 0 2px 5px rgba(0,0,0,0.1);">

#### カード2
コンテンツ説明

</div>
<div style="background: white; padding: 15px; border-radius: 8px; box-shadow: 0 2px 5px rgba(0,0,0,0.1);">

#### カード3
コンテンツ説明

</div>
</div>

---

### レイアウト5: 比較表示

<div style="
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  gap: 30px;
  align-items: center;
">
<div style="text-align: right;">

#### Before
- 課題1
- 課題2
- 課題3

</div>
<div style="font-size: 2em; color: #4a90e2;">→</div>
<div>

#### After
- 解決1
- 解決2
- 解決3

</div>
</div>

---

### レイアウト6: ダッシュボード

<div style="
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(2, 1fr);
  gap: 15px;
  height: 60vh;
">
<div style="background: #f8f9fa; padding: 15px; border-radius: 8px;">

#### グラフ1
データ可視化エリア

</div>
<div style="background: #f8f9fa; padding: 15px; border-radius: 8px;">

#### グラフ2
データ可視化エリア

</div>
<div style="background: #f8f9fa; padding: 15px; border-radius: 8px;">

#### グラフ3
データ可視化エリア

</div>
<div style="background: #f8f9fa; padding: 15px; border-radius: 8px;">

#### グラフ4
データ可視化エリア

</div>
</div>

---

### レイアウト7: 特徴説明

<div style="
  display: grid;
  grid-template-columns: auto 1fr;
  gap: 30px;
  align-items: center;
">
<div style="font-size: 3em; color: #4a90e2;">
🎯
</div>
<div>

#### 主要な特徴
詳細な説明文をここに記載します。
複数行に渡る説明も可能です。

</div>
</div>

---

### レイアウト8: ステップ表示

<div style="
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 40px 0;
">
<div style="text-align: center;">
<div style="
  width: 40px;
  height: 40px;
  background: #4a90e2;
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 10px;
">1</div>
ステップ1
</div>
<div style="flex-grow: 1; height: 2px; background: #4a90e2; margin: 0 10px;"></div>
<div style="text-align: center;">
<div style="
  width: 40px;
  height: 40px;
  background: #4a90e2;
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 10px;
">2</div>
ステップ2
</div>
<div style="flex-grow: 1; height: 2px; background: #4a90e2; margin: 0 10px;"></div>
<div style="text-align: center;">
<div style="
  width: 40px;
  height: 40px;
  background: #4a90e2;
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 10px;
">3</div>
ステップ3
</div>
</div>

---

### レイアウト9: 引用デザイン

<div style="
  position: relative;
  padding: 30px;
  background: #f8f9fa;
  border-left: 5px solid #4a90e2;
  margin: 40px 0;
">
<div style="
  position: absolute;
  top: -20px;
  left: 20px;
  background: white;
  padding: 5px 15px;
  color: #4a90e2;
  font-weight: bold;
">引用元</div>

引用文をここに記載します。
複数行に渡る引用も美しく表示されます。

<div style="
  text-align: right;
  margin-top: 20px;
  font-style: italic;
">- 著者名</div>
</div>

---

### レイアウト10: 機能比較表

<div style="
  display: grid;
  grid-template-columns: auto repeat(3, 1fr);
  gap: 10px;
  text-align: center;
">
<div style="background: #4a90e2; color: white; padding: 10px;">機能</div>
<div style="background: #4a90e2; color: white; padding: 10px;">Basic</div>
<div style="background: #4a90e2; color: white; padding: 10px;">Pro</div>
<div style="background: #4a90e2; color: white; padding: 10px;">Enterprise</div>

<div style="background: #f8f9fa; padding: 10px;">機能1</div>
<div style="background: #f8f9fa; padding: 10px;">✓</div>
<div style="background: #f8f9fa; padding: 10px;">✓</div>
<div style="background: #f8f9fa; padding: 10px;">✓</div>

<div style="background: #f8f9fa; padding: 10px;">機能2</div>
<div style="background: #f8f9fa; padding: 10px;">-</div>
<div style="background: #f8f9fa; padding: 10px;">✓</div>
<div style="background: #f8f9fa; padding: 10px;">✓</div>

<div style="background: #f8f9fa; padding: 10px;">機能3</div>
<div style="background: #f8f9fa; padding: 10px;">-</div>
<div style="background: #f8f9fa; padding: 10px;">-</div>
<div style="background: #f8f9fa; padding: 10px;">✓</div>
</div>

---

## まとめ

1. Marpの基本機能を習得
   - テキスト装飾
   - メディア挿入
   - コードブロック
2. アニメーションとスタイルの活用
   - 5種類の基本アニメーション
   - カスタムCSSの適用
3. 高度なレイアウト実装
   - グリッドレイアウト
   - カード型デザイン
   - タイムライン表示
4. 実践的なスライド作成
   - レスポンシブ対応
   - 視覚的な階層構造
   - インタラクティブ要素

---

<!-- _class: lead -->
# ご清聴ありがとうございました
