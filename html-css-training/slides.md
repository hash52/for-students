---
marp: true
theme: default
size: 16:9
paginate: true
header: ""
footer: ""
style: |
  section {
    background-color: #ffffff;
    color: #333333;
    font-family: 'Segoe UI', -apple-system, BlinkMacSystemFont, sans-serif;
    padding: 50px 70px;
  }
  h1 {
    color: #2563eb;
    font-size: 1.8rem;
    font-weight: 700;
    margin-bottom: 0.5rem;
  }
  h2 {
    color: #1e40af;
    font-size: 1.5rem;
    font-weight: 600;
    border-bottom: 3px solid #3b82f6;
    padding-bottom: 0.25rem;
    margin-bottom: 0.6rem;
  }
  h3 {
    color: #1e3a8a;
    font-size: 1.1rem;
    margin-bottom: 0.3rem;
  }
  h4 {
    color: #1e40af;
    font-size: 0.95rem;
    margin-bottom: 0.25rem;
  }
  strong {
    color: #dc2626;
  }
  section.title {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
  }
  section.title h1 {
    color: white;
    font-size: 2.4rem;
    margin-bottom: 2rem;
  }
  section.title strong {
    color: white;
  }
  p {
    font-size: 0.95rem;
    line-height: 1.4;
    margin-bottom: 0.35rem;
  }
  ul {
    font-size: 0.95rem;
    line-height: 1.4;
    margin-left: 1.1rem;
  }
  li {
    margin-bottom: 0.2rem;
  }
  .highlight {
    background-color: #fef3c7;
    padding: 0.6rem 0.8rem;
    border-left: 4px solid #f59e0b;
    margin: 0.6rem 0;
    font-size: 0.95rem;
  }
  .warning {
    background-color: #fee2e2;
    padding: 0.6rem 0.8rem;
    border-left: 4px solid #dc2626;
    margin: 0.6rem 0;
    font-size: 0.95rem;
  }
  .two-columns {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
  }
  .three-columns {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
  }
  .schedule-grid {
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 0.3rem 0.8rem;
    margin-top: 0.4rem;
  }
  .schedule-time {
    font-weight: 600;
    color: #2563eb;
    font-size: 0.9rem;
  }
  code {
    background-color: #f3f4f6;
    padding: 0.1rem 0.3rem;
    border-radius: 0.2rem;
    font-size: 0.9rem;
  }
  pre {
    background-color: #1e293b;
    color: #e2e8f0;
    padding: 0.8rem;
    border-radius: 0.4rem;
    font-size: 0.85rem;
    overflow-x: auto;
  }
  pre code {
    background-color: transparent;
    color: #e2e8f0;
    padding: 0;
  }
---

<!-- _class: title -->

# HTML/CSS/Bootstrap 入門<br>体験ワークショップ

**〜すぐに作れるWeb制作研修〜**

---

## 自己紹介

### 👤 吐師 昊冴（はし ひろき）

<div class="two-columns">

<div>

**職業**

- プログラマ / 研修講師

**直近の技術スタック**

- Java, Spring
- TypeScript, React
- PostgreSQL, Elasticsearch, RabbitMQ

</div>

<div>

**開発しているもの**

- toB 向けファイル管理アプリ
- 画像・動画などのメディアファイルを扱うシステム

**趣味**

- 映画鑑賞, 読書, 料理, 釣り
  プログラミング

</div>

</div>

---

## 今日の目標 🎯

### この研修のゴール

**「細かいことを知らなくても、雑な知識でそれっぽいWebサイトが作れる」**

- 学校の授業とは違う：基礎から積み上げる「地味で退屈」ではなく
- **すぐに実践できる楽しさ**を体験
- 今日学んだことを明日から使える

<div class="highlight">

**重要**: 細かい文法は覚えなくてOK！でも**概念は必要** → なぜなら、概念を知らないとAIに聞けないから

</div>

---

## 本日の流れ

<div class="schedule-grid">
<span class="schedule-time">13:00-13:15</span><span>オープニング・環境確認</span>
<span class="schedule-time">13:15-13:50</span><span>座学① HTML基礎（文章構造）</span>
<span class="schedule-time">13:50-14:10</span><span>体験① HTMLで文章構造を作る</span>
<span class="schedule-time">14:10-14:15</span><span>休憩</span>
<span class="schedule-time">14:15-14:35</span><span>座学② CSS最小限（見た目の調整）</span>
<span class="schedule-time">14:35-15:00</span><span>座学③ Bootstrap入門</span>
<span class="schedule-time">15:00-15:05</span><span>休憩</span>
<span class="schedule-time">15:05-16:35</span><span>実践 Bootstrap Web制作演習（90分）</span>
<span class="schedule-time">16:35-17:35</span><span>成果発表（60分）</span>
</div>

---

## 環境確認

### VSCode + Live Server の動作確認

**手順**:

1. VSCodeを開く
2. HTMLファイルを開く
3. 右クリック → **「Open with Live Server」**
4. ブラウザで表示されることを確認

<div class="warning">

**動かない場合**：講師に知らせてください。個別にサポートします

</div>

---

<!-- _class: title -->

# 座学①
# HTML基礎

---

## HTMLは文章構造のマークアップ

### HTMLの本質

<div class="two-columns">

<div>

**HTMLはデザインツールではない**

- 見た目を作るものではない
- **意味を与えるもの**

**セマンティックHTML**

- h1 = 大見出し
- h2 = 中見出し
- p = 段落
- ul/li = リスト

</div>

<div>

**例：新聞**

- 見出し（大・中・小）
- 本文
- 箇条書き
- 画像

→ これらに**意味**を与える

</div>

</div>

<div class="highlight">

**重要**: HTMLは文章構造のマークアップ。デザインはCSSの役割！

</div>

---

## HTMLの基本構造

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ページタイトル</title>
</head>
<body>
  <!-- ここに内容 -->
  <h1>大見出し</h1>
  <p>段落です。</p>
</body>
</html>
```

- `<head>`: ページの設定情報（タイトル、文字コードなど）
- `<body>`: 実際に表示される内容

---

## よく使うHTMLタグ

| タグ | 意味 | 例 |
|------|------|-----|
| `<h1>` | 大見出し | `<h1>タイトル</h1>` |
| `<h2>`, `<h3>` | 中・小見出し | `<h2>セクション</h2>` |
| `<p>` | 段落 | `<p>本文です</p>` |
| `<ul>`, `<li>` | リスト | `<ul><li>項目1</li></ul>` |
| `<img>` | 画像 | `<img src="image.jpg">` |
| `<a>` | リンク | `<a href="https://...">リンク</a>` |
| `<div>` | グループ化 | `<div>内容</div>` |

<div class="highlight">

**細かい文法は覚えなくてOK！** わからなければAIに聞こう

</div>

---

## タグの入れ子構造

```html
<div>
  <h2>セクション</h2>
  <p>説明文</p>
  <ul>
    <li>項目1</li>
    <li>項目2</li>
  </ul>
</div>
```

**ルール**:

- タグの中にタグを入れられる
- **開いたら必ず閉じる**（例：`<h1>...</h1>`）
- 正しい順番で閉じる

---

## デモ：HTMLだけで文章を構造化

### HTMLのみ（CSSなし）のページ

**見た目**:

- シンプルで地味
- でも**構造は明確**

**ブラウザが自動的に**:

- h1は大きく表示
- pは普通のサイズ
- ulは箇条書き

→ これがHTMLの役割！

---

## VSCodeとLive Serverの使い方

### ファイルを作成して表示する

**手順**:

1. VSCodeで新しいファイルを作成（`index.html`）
2. HTMLコードを書く
3. 保存（`Cmd+S` or `Ctrl+S`）
4. 右クリック → **「Open with Live Server」**
5. ブラウザで自動的に開く
6. ファイルを編集して保存すると、**即座に反映**

<div class="highlight">

Live Server = 保存すると自動でブラウザに反映される便利ツール

</div>

---

## 体験① HTMLで文章構造を作る

### 自己紹介ページの構造を作ろう

**やること**:

- テンプレート（`01_html-structure.html`）を使う
- h1（名前）、h2（セクション）、p（説明）、ul/li（リスト）を編集
- **デザインは一切せず、構造のみに集中**

**時間**: 20分

**AI活用OK**: わからなければChatGPTに聞こう
例：「HTMLでリストを作る方法を教えて」

---

<!-- _class: title -->

# 座学②
# CSS最小限

---

## CSSの役割

### CSSとは

**CSS = Cascading Style Sheets**

- HTMLは**構造**
- CSSは**見た目**

<div class="two-columns">

<div>

**CSSでできること**

- 文字色を変える
- 背景色をつける
- 余白を調整する
- ボーダーをつける

</div>

<div>

**書き方**

```css
h1 {
  color: blue;
  font-size: 32px;
}
```

- **セレクタ** = どこに（h1）
- **プロパティ** = 何を（color）
- **値** = どうする（blue）

</div>

</div>

---

## 最小限のCSSプロパティ

### これだけ知っていればOK

| プロパティ | 意味 | 例 |
|-----------|------|-----|
| `color` | 文字色 | `color: red;` |
| `background-color` | 背景色 | `background-color: #f0f0f0;` |
| `border` | ボーダー | `border: 2px solid black;` |
| `padding` | 内側の余白 | `padding: 10px;` |
| `margin` | 外側の余白 | `margin: 20px;` |

<div class="highlight">

**細かいプロパティは覚えなくてOK！** わからなければAI or 検証ツール

</div>

**AIへの質問例**: 「h1タグの文字色を青にするCSSを教えて」

---

## CSSボックスモデル

### padding と margin の違い

```
┌─────────────────────────┐ ← margin（外側の余白）
│  margin                  │
│  ┌───────────────────┐   │
│  │  border           │   │
│  │  ┌─────────────┐  │   │
│  │  │  padding    │  │   │
│  │  │  ┌───────┐  │  │   │
│  │  │  │content│  │  │   │
│  │  │  └───────┘  │  │   │
│  │  │             │  │   │
│  │  └─────────────┘  │   │
│  └───────────────────┘   │
└─────────────────────────┘
```

- **padding**: 要素の内側の余白
- **margin**: 要素の外側の余白

---

## Chrome検証ツールの使い方

### 他サイトのデザインを参考にする

**手順**:

1. Webページ上で **右クリック → 検証**
2. HTMLとCSSが見える
3. 他サイトのデザインを見て学べる

<div class="two-columns">

<div>

**できること**

- HTMLの構造を確認
- CSSのプロパティを確認
- その場で値を変えて試せる

</div>

<div>

**活用方法**

- 「この色いいな」→ 色コードをコピー
- 「この余白いいな」→ padding値を確認
- 参考にして自分のサイトに応用

</div>

</div>

---

<!-- _class: title -->

# 座学③
# Bootstrap入門

---

## Bootstrapとは

### CSSフレームワーク = よく使うスタイルの詰め合わせ

<div class="two-columns">

<div>

**なぜBootstrapを使うのか**

- ゼロから書かなくていい
- **レスポンシブ対応が簡単**
- デザインが統一される
- 学習コストが低い

</div>

<div>

**使い方**

1. CDNで読み込む
2. クラス名を書く
3. 完成！

**例**:
`<button class="btn btn-primary">ボタン</button>`

→ 青いボタンが完成

</div>

</div>

<div class="highlight">

**重要**: 公式ドキュメントからコピペでOK！細かいクラス名は覚えなくていい

</div>

---

## Bootstrapの読み込み方法

### CDN経由で簡単に読み込める

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Site</title>

  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css"
        rel="stylesheet">
</head>
```

**CDN = Content Delivery Network**

- ダウンロード不要
- URLを貼るだけで使える

---

## グリッドシステム

### 12カラムシステムで柔軟なレイアウト

```html
<div class="container">
  <div class="row">
    <div class="col-md-4">列1</div>
    <div class="col-md-4">列2</div>
    <div class="col-md-4">列3</div>
  </div>
</div>
```

**仕組み**:

- `container` = 全体を囲む
- `row` = 行
- `col-md-4` = 中サイズ画面で4/12幅（3等分）

<div class="highlight">

**col-md-4 を3つ並べる = 3カラム（4+4+4=12）**

</div>

---

## レスポンシブデザインの仕組み

### 画面サイズに応じて表示を変える

| サイズ | クラス | 画面幅 | デバイス |
|--------|--------|--------|----------|
| Extra Small | （なし） | < 576px | スマホ縦 |
| Small | `sm` | ≥ 576px | スマホ横 |
| Medium | `md` | ≥ 768px | タブレット |
| Large | `lg` | ≥ 992px | PC |
| Extra Large | `xl` | ≥ 1200px | 大画面PC |

**例**: `col-md-4` = タブレット以上で4/12幅、スマホでは全幅（12/12）

---

## コンポーネント①：navbar

### ナビゲーションバー

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">My Site</a>
    <div class="navbar-nav">
      <a class="nav-link" href="#">ホーム</a>
      <a class="nav-link" href="#">About</a>
    </div>
  </div>
</nav>
```

**クラスの意味**:

- `navbar` = ナビゲーションバー
- `navbar-expand-lg` = 大画面で横並び
- `navbar-light bg-light` = 明るい背景

---

## コンポーネント②：card

### カード（情報をまとめる箱）

```html
<div class="card">
  <img src="image.jpg" class="card-img-top" alt="画像">
  <div class="card-body">
    <h5 class="card-title">タイトル</h5>
    <p class="card-text">説明文です。</p>
    <a href="#" class="btn btn-primary">詳細</a>
  </div>
</div>
```

**よく使う場面**:

- 商品紹介
- ブログ記事一覧
- プロフィール

---

## コンポーネント③：button

### ボタン

```html
<button class="btn btn-primary">ボタン</button>
<button class="btn btn-success">成功</button>
<button class="btn btn-danger">危険</button>
<button class="btn btn-outline-secondary">アウトライン</button>
```

**色のバリエーション**:

- `btn-primary` = 青（主要）
- `btn-success` = 緑（成功）
- `btn-danger` = 赤（危険）
- `btn-warning` = 黄（警告）
- `btn-outline-*` = アウトライン

---

## ユーティリティクラス

### よく使う便利クラス

| クラス | 意味 | 例 |
|--------|------|-----|
| `mt-3` | margin-top: 3 | 上に余白 |
| `mb-4` | margin-bottom: 4 | 下に余白 |
| `p-3` | padding: 3 | 内側に余白 |
| `text-center` | 中央揃え | テキストを中央に |
| `text-white` | 白文字 | 文字色を白に |
| `bg-primary` | 背景色（青） | 背景を青に |
| `d-flex` | flexbox | フレックスレイアウト |

<div class="highlight">

**数字は0-5**: 0=なし、1=小、3=中、5=大

</div>

---

## 公式ドキュメントの使い方

### Bootstrap公式サイト

**URL**: https://getbootstrap.com/

**使い方**:

1. 「Components」セクションから探す
2. コピペできる例がたくさん
3. カスタマイズの方法も記載

<div class="two-columns">

<div>

**例を探す**

- Navbar
- Cards
- Buttons
- Forms

</div>

<div>

**コピペして使う**

1. 例をコピー
2. 自分のHTMLに貼り付け
3. 文字や画像を変更
4. 完成！

</div>

</div>

**AIへの質問例**: 「Bootstrapで3カラムのカードレイアウトを作りたい」

---

<!-- _class: title -->

# 実践
# Bootstrap Web制作演習

---

## 実践：「好きなもの」サイト制作

### テーマ

**自分の好きなもの**に関するWebサイトを作ろう

- ゲーム
- アイドル・アニメ
- スポーツチーム
- 勉強している分野
- ファッション
- 映画・ドラマ
- なんでもOK！

**時間**: 90分

---

## 必須要件（5つ）

1. **Bootstrapのnavbar**（ナビゲーションバー）
2. **Bootstrapのcardを3つ以上**
3. **画像を3枚以上使用**
4. **「好きなもの」に関する説明文**（100文字以上）
5. **レスポンシブ対応**（グリッドシステム使用）

<div class="warning">

**最低限これだけは達成しよう！** 推奨要素は時間があれば追加

</div>

---

## 推奨要素

### 余裕があれば追加しよう

- **ボタン**（`btn`）の配置
- **カスタムカラー**（自分の好きな色）
- **コンテンツの充実**（説明文を詳しく書く）
- **ホバーエフェクト**（マウスを乗せると変化）
- **画像の工夫**（サイズや配置）

<div class="highlight">

**重要**: 完璧を目指さなくてOK！まず動くものを作ろう

</div>

---

## ページ構成サンプル

### 例：ゲーム紹介サイト

```
┌─────────────────────────┐
│ [Navbar] 私の好きなゲーム │
├─────────────────────────┤
│   ╔═══════════════════╗  │
│   ║  ヒーローイメージ   ║  │  ← 大きな画像
│   ║ 「ゲームタイトル」  ║  │
│   ╚═══════════════════╝  │
├─────────────────────────┤
│ ┌────┐ ┌────┐ ┌────┐   │
│ │Card│ │Card│ │Card│   │  ← 3つのカード
│ │キャラ│ │武器 │ │ステ│  │
│ └────┘ └────┘ └────┘   │
├─────────────────────────┤
│     ゲームの魅力を語る      │  ← 説明文
│     説明文セクション        │
└─────────────────────────┘
```

---

## AI活用を積極的に推奨

### わからなければすぐAIに聞こう

**AI活用の流れ**:

1. **概念を理解**（座学で学んだこと）
2. **AIに質問**（具体的に聞く）
3. **出力をコピペ**して試す
4. **動かない場合**はAIに改善を依頼

<div class="highlight">

**AIへの質問例**:
「Bootstrapで3カラムのカードレイアウトを作りたい」
「navbarに自分のサイト名を入れる方法を教えて」
「画像を丸く表示する方法を教えて」

</div>

---

## 制作時間：90分

### タイムライン

<div class="schedule-grid">
<span class="schedule-time">0-5分</span><span>役割分担・企画</span>
<span class="schedule-time">5-75分</span><span>制作（各自 or チームで相談しながら）</span>
<span class="schedule-time">75-85分</span><span>仕上げ・動作確認</span>
<span class="schedule-time">85-90分</span><span>提出</span>
</div>

**チームワーク**:

- わからないことはチームメンバーに聞く
- 助け合いながら進める
- 講師も巡回してサポート

---

## 成果発表

### 発表内容（各チーム8分）

1. **何を作ったか**（テーマ）
2. **工夫したポイント**
3. **つまずいたポイント**
4. **AIをどう活用したか**（任意）

**発表時間**: 60分（全7チーム × 8分 + バッファ）

**相互フィードバック**: 各チーム発表後に質問・感想タイム

---

<!-- _class: title -->

# まとめ

---

## 今日学んだこと

### 3つの重要な概念

1. **HTMLは文章構造のマークアップ**
   - デザインではなく、意味を与えるもの

2. **CSSは見た目の調整**
   - 文字色、背景色、余白などを調整

3. **Bootstrapは効率的なWeb制作ツール**
   - 公式ドキュメントからコピペでOK
   - AIに聞いて使う

<div class="highlight">

**重要**: 細かい文法は覚えなくてOK！概念を理解してAIに聞けるようになることが大事

</div>

---

## さらに学びたい人へ

### おすすめの学習リソース

**学習サイト**:

- **Progate** - HTML/CSS基礎コース（無料）
- **ドットインストール** - 動画で学ぶ（無料）
- **MDN Web Docs** - 公式リファレンス（日本語あり）

**公式ドキュメント**:

- **Bootstrap公式サイト** - https://getbootstrap.com/
- 例をコピペして使える

**画像素材**:

- **Unsplash**, **Pixabay** - 無料の高品質写真

---

<!-- _class: title -->

# ご清聴ありがとうございました

**質問があればいつでも連絡してください！**
