---
marp: true
theme: uncover
paginate: true
header: "Marpスライド作成ガイド"
footer: "© 2024 Marp Study"
style: |
  section {
    background-color: #ffffff;
    font-size: 1.5em;
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

---

<!-- _class: lead -->
## 1. スライドの基本構成

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

## 3. 画像の挿入

![width:500px](https://raw.githubusercontent.com/marp-team/marp/master/marp.png)

画像のサイズと位置を調整可能

---

## 4. リンクの挿入

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

## 5. コードの挿入

```python
def hello_world():
    print("Hello, Marp!")
```

```javascript
console.log('Hello from JavaScript!');
```

---

## 6. テーブルの挿入

| 機能 | 説明 | 難易度 |
|:-----|:-----|:------:|
| 基本構成 | スライドの基本設定 | ★ |
| テーマ設定 | デザインのカスタマイズ | ★★ |
| アニメーション | 動的な表現 | ★★★ |

---

## 7. リストの活用

1. 番号付きリスト
   1. サブリスト1
   2. サブリスト2
2. 次の項目

- 箇条書きリスト
  - ネストされたリスト
    - さらにネスト

---

<!-- _class: lead invert -->
## 8. アニメーション効果

このスライドは反転テーマを使用

---

<!-- _class: anime -->
<style scoped>
h2 {
  animation: fadeIn 1s;
}
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}
</style>

## 9. カスタムCSSの活用

アニメーションとスタイルのカスタマイズ

---

## 10. 高度なレイアウト集

---

<!-- _class: lead -->
### レイアウト1: 3カラムグリッド

<div style="
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 20px;
  text-align: center;
">
<div style="background: #f0f0f0; padding: 20px; border-radius: 8px;">

#### セクション1
- 特徴1
- 特徴2

</div>
<div style="background: #e0e0e0; padding: 20px; border-radius: 8px;">

#### セクション2
- 機能1
- 機能2

</div>
<div style="background: #d0d0d0; padding: 20px; border-radius: 8px;">

#### セクション3
- ポイント1
- ポイント2

</div>
</div>

---

### レイアウト2: ヒーローセクション

<div style="
  position: relative;
  height: 70vh;
  background: linear-gradient(45deg, #4a90e2, #50e3c2);
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 15px;
">
<div style="text-align: center;">

# 大見出し
## サブタイトル
詳細な説明文をここに記載します

</div>
</div>

---

### レイアウト3: カード型レイアウト

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

### レイアウト4: タイムライン

<div style="display: flex; flex-direction: column; gap: 20px;">
<div style="
  position: relative;
  padding-left: 30px;
  border-left: 2px solid #4a90e2;
">

#### 2024年
主要な出来事1

</div>
<div style="
  position: relative;
  padding-left: 30px;
  border-left: 2px solid #4a90e2;
">

#### 2025年
主要な出来事2

</div>
<div style="
  position: relative;
  padding-left: 30px;
  border-left: 2px solid #4a90e2;
">

#### 2026年
主要な出来事3

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
