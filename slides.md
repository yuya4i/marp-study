---
marp: true
theme: uncover
paginate: true
header: "Marpスライド作成ガイド"
footer: "© 2024 Marp Study"
style: |
  section {
    background-color: #ffffff;
  }
  h1 {
    color: #2c3e50;
  }
  h2 {
    color: #34495e;
  }
---

# Marpスライド作成ガイド
基本から応用まで

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

<!-- _class: lead -->
## 10. 高度なレイアウト

<div style="
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
">
<div>

### 左カラム
- 項目1
- 項目2

</div>
<div>

### 右カラム
- 項目A
- 項目B

</div>
</div>
