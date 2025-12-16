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
    background-color: #e5e7eb;
    padding: 0.1rem 0.3rem;
    border-radius: 0.2rem;
    font-size: 0.9rem;
    color: #1f2937;
  }
  pre {
    background-color: #f6f8fa;
    color: #24292e;
    padding: 0.8rem;
    border-radius: 0.4rem;
    font-size: 0.85rem;
    overflow-x: auto;
    border: 1px solid #d0d7de;
  }
  pre code {
    background-color: transparent;
    color: #24292e;
    padding: 0;
  }
  /* シンタックスハイライト（highlight.js用） */
  pre code .hljs-tag,
  pre code .hljs-name {
    color: #116329;
  }
  pre code .hljs-attr {
    color: #0550ae;
  }
  pre code .hljs-string {
    color: #0a3069;
  }
  pre code .hljs-comment {
    color: #6e7781;
    font-style: italic;
  }
  pre code .hljs-doctag,
  pre code .hljs-keyword {
    color: #cf222e;
  }
  pre code .hljs-meta {
    color: #8250df;
  }
  /* シンタックスハイライト（Prism.js用） */
  pre code .token.tag {
    color: #116329;
  }
  pre code .token.attr-name {
    color: #0550ae;
  }
  pre code .token.attr-value,
  pre code .token.string {
    color: #0a3069;
  }
  pre code .token.comment {
    color: #6e7781;
    font-style: italic;
  }
  pre code .token.keyword {
    color: #cf222e;
  }
  pre code .token.function {
    color: #8250df;
  }
  pre code .token.punctuation {
    color: #24292e;
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

## 前回アンケートのフィードバック

### よかったこと ✅

- 全体的に概ね高評価
- 匿名チャットで質問できた件の評判がよかった

### 改善すべき点 📝

- チーム内でアイスブレークの時間が欲しい
- ChatGPTのプロジェクトの良さがイマイチ伝わらなかった

### 最も多かった質問 💡

**「業務でAI使う場面を知りたい」**

→ 次のスライドで詳しく説明します

---

## 業務でAIを活用する場面

<div class="two-columns">

<div>

**コーディング**

- コード生成・補完
- デバッグ支援

**資料作成**

- プレゼン資料
- ドキュメント作成

</div>

<div>

**AIエージェント作成**

- 業務自動化
- チャットボット

**その他**

- アイデア出し
- 調査・リサーチ

</div>

</div>

<div class="highlight">

AIを活用していない業務を考える方が難しい。
アウトプット8割はAIが作成、**自分は現場監督**。
このスライドもAIで作成しました（marp）

</div>

---

<!-- _class: title -->

# HTML/CSS/Bootstrap 入門<br>体験ワークショップ

**〜すぐに作れるWeb制作研修〜**


---

## 今日の目標 🎯

### この研修のゴール

**「細かいことを知らなくても、雑な知識でそれっぽいWebサイトが作れる」**

- 基礎から積み上げる「地味で退屈」な内容にはしたくない
- **すぐに実践できる楽しさ**を体験
- 今日学んだことを明日から使える

<div class="highlight">

**重要**: 細かい文法は覚えなくてOK！でも**概念は必要** 
→ なぜなら、概念を知らないとAIに聞けないから

</div>

---

## 本日の流れ

<div class="schedule-grid">
<span class="schedule-time">13:00-13:20</span><span>オープニング・環境確認</span>
<span class="schedule-time">13:20-13:30</span><span>体験演習：ブラウザでソース観察</span>
<span class="schedule-time">13:30-13:40</span><span>ブラウザの仕組み + HTML/CSS学習の必要性</span>
<span class="schedule-time">13:40-13:55</span><span>座学① HTML基礎（論理と見た目の分離含む）</span>
<span class="schedule-time">13:55-14:05</span><span>体験① HTMLで文章構造を作る</span>
<span class="schedule-time">14:05-14:25</span><span>座学② CSS + 体験② CSSミニワーク</span>
<span class="schedule-time">14:25-14:40</span><span>座学③ Bootstrap入門</span>
<span class="schedule-time">14:40-16:00</span><span>実践 Bootstrap Web制作演習（80分）</span>
<span class="schedule-time">16:00-16:45</span><span>成果発表（45分）</span>
<span class="schedule-time">16:45-16:50</span><span>まとめ</span>
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

## 【体験演習】Webサイトのソースを見てみよう

### ブラウザの検証ツールを使ってみよう（5分）

**やること**:

1. ブラウザでWebサイトを開く
2. 右クリック → **「検証」**
3. 発見すること：
   - サイト内で、どんな規則性がある？
   - Webサイトのコンテンツはどこに書かれている？
   - サイトを跨いで、構造に規則性はある？

<div class="highlight">

**目標**: HTMLとCSSがどう使われているか、実際のサイトで確認しよう

</div>

---

## ブラウザの仕組み

### Webサイトはどう表示されている？

**発見したこと**:

- HTMLのタグ（h1, p, divなど）がある
- テキストがそのまま書かれている
- 画像のURLやCSSの情報がある

<div class="two-columns">

<div>

**ブラウザがやっていること**

1. HTMLを読み込む
2. CSSを読み込む
3. 解釈して表示

</div>

<div>

**つまり**

- スマホもPCも同じ
- ソースがあれば表示できる
- **構造が重要**

</div>

</div>

---

<!-- _class: title -->

# 座学①
# HTML基礎

---

## HTMLは文章構造のマークアップ

### HTMLの本質：論理と見た目の分離

<div class="two-columns">

<div>

**HTMLはデザインツールではない**

- 見た目を作るものではない
- **意味、構造を与えるもの**

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

→ これらに**意味**を与える

**論理と見た目の分離**

- HTML = 構造・意味
- CSS = 見た目・デザイン

</div>

</div>

<div class="highlight">

**重要**: HTMLは文章構造のマークアップ。デザインはCSSの役割！

</div>

---

## 悪い例：見た目だけで構造を無視

### h1タグを間違って使った例

**デモ**: `samples/bad-example-携帯小説.html` を開いてみよう

<div class="warning">

**問題点**:

- h1は「ページの主題」を表すタグ
- 「大きく表示したい」だけで使うのはNG
- Googleは「このページは3つの主題がある」と誤解
- スクリーンリーダーで読み上げ時に混乱

</div>

<div class="highlight">

**正解**: pタグ + CSSで「大きなフォント」にする

</div>

---

## 良い例 vs 悪い例の比較

### 見た目は同じでも、構造が違う！

**デモ**: `samples/comparison-h1-vs-div.html` を開いて検証ツールで比較しよう

<div class="two-columns">

<div>

**良い例：h1タグで構造化**

```html
<h1>これは見出しです</h1>
<p>本文です。</p>
```

✅ Googleが「見出し」と認識
✅ スクリーンリーダーで正しく読み上げ
✅ CSSで一括デザイン変更可能
✅ 目次を自動生成できる

</div>

<div>

**悪い例：div+styleで見た目だけ**

```html
<div style="font-size:2rem; font-weight:bold">
  これは見出しです
</div>
<div>本文です。</div>
```

❌ Googleが「ただの大きな文字」と認識
❌ 構造が伝わらない
❌ 後で変更するのが大変
❌ 目次を作れない

</div>

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

### 自己紹介ページの構造を作ろう（10分）

**やること**:

- テンプレート（`01_html-structure.html`）を使う
- h1（名前）、h2（セクション）、p（説明）、ul/li（リスト）を編集
- **デザインは一切せず、構造のみに集中**

**AI活用OK**: わからなければChatGPTに聞こう
例：「HTMLでリストを作る方法を教えて」

<div class="highlight">

**ポイント**: 構造を意識して、適切なタグを使おう！

</div>

---

<!-- _class: title -->

# 座学②
# CSS

---

## CSSの役割

### 論理と見た目の分離を実現する

**CSS = Cascading Style Sheets**

- **HTML = 構造・意味**
- **CSS = 見た目・デザイン**

<div class="two-columns">

<div>

**CSSでできること**

- 文字色を変える
- 背景色をつける
- 余白を調整する
- ボーダーをつける

**書き方**

```css
h1 {
  color: blue;
  font-size: 32px;
}
```

</div>

<div>

**最小限のプロパティ**

| プロパティ | 意味 |
|-----------|------|
| `color` | 文字色 |
| `background-color` | 背景色 |
| `padding` | 内側の余白 |
| `margin` | 外側の余白 |

**Chrome検証ツール活用**

- 他サイトのデザインを参考に
- 色コードをコピー
- padding/margin値を確認

</div>

</div>

<div class="highlight">

**重要**: HTMLは構造、CSSは見た目！細かいプロパティは覚えなくてOK、AIに聞こう

</div>

---

## 体験② CSSミニワーク

### 実践でCSSの基本を学ぶ（10分）

**ファイル**: `templates/03_css-mini-exercise.html`

**ミッション**:

1. h1の色を好きな色に変える
2. boxにpaddingとmarginをつける
3. Chrome検証ツールで他サイトの色をコピー

**わからなければAI活用OK！**

- 「CSSでh1の色を変える方法は？」
- 「paddingとmarginの違いは？」

<div class="highlight">

**目標**: CSSを書く→ブラウザで確認→修正、のサイクルを体験しよう

</div>

---


## 論理と見た目の分離のメリット

### なぜHTML/CSSを学ぶのか？

<div class="two-columns">

<div>

**WYSIWYGツールの限界**

- Wix, WordPress
- 簡単だが構造が隠れる

**構造が重要な理由**

</div>

<div>

**メリット①：SEO**

- Googleは構造を見ている
- h1タグ → 検索上位表示

**メリット②：アクセシビリティ**

- スクリーンリーダーが構造を読む
- 視覚障害者もWebを利用できる

</div>

</div>

<div class="two-columns">

<div>

**メリット③：目次作成**

- 見出し構造から自動生成
- h1, h2, h3の階層が重要

</div>

<div>

**メリット④：一括デザイン変更**

- CSSで全ページを変更
- ブログでタイトルデザイン変更 → 全記事に反映

</div>

</div>

<div class="highlight">

**重要**: 見た目は同じでも、構造が違うと意味が違う

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

**使い方**

1. CDNで読み込む（`<link>`タグ）
2. クラス名を書く
3. 完成！

</div>

<div>

**CDN読み込み**

```html
<link href="https://cdn.jsdelivr.net/npm/
bootstrap@5.3.0/dist/css/bootstrap.min.css"
rel="stylesheet">
```

**例**:

```html
<button class="btn btn-primary">
  ボタン
</button>
```

→ 青いボタンが完成

</div>

</div>

<div class="highlight">

**重要**: 公式ドキュメントからコピペでOK！細かいクラス名は覚えなくていい

</div>

---

## グリッドシステム + コンポーネント

### 12カラムシステムとよく使うコンポーネント

<div class="two-columns">

<div>

**グリッドシステム**

```html
<div class="container">
  <div class="row">
    <div class="col-md-4">列1</div>
    <div class="col-md-4">列2</div>
    <div class="col-md-4">列3</div>
  </div>
</div>
```

- `col-md-4` = タブレット以上で4/12幅
- スマホでは全幅（自動調整）

**レスポンシブ**: `md` = タブレット、`lg` = PC

</div>

<div>

**よく使うコンポーネント**

**navbar**: ナビゲーションバー

```html
<nav class="navbar navbar-light bg-light">
  <a class="navbar-brand">My Site</a>
</nav>
```

**card**: 情報をまとめる箱

```html
<div class="card">
  <div class="card-body">
    <h5 class="card-title">タイトル</h5>
  </div>
</div>
```

**button**: ボタン

```html
<button class="btn btn-primary">ボタン</button>
```

</div>

</div>

---

## 公式ドキュメント + AI活用

### Bootstrap公式サイト + AI

**公式サイト**: https://getbootstrap.com/

- 「Components」セクションから探す
- コピペできる例がたくさん
- カスタマイズの方法も記載

**AIへの質問例**:

- 「Bootstrapで3カラムのカードレイアウトを作りたい」
- 「navbarに自分のサイト名を入れる方法を教えて」
- 「画像を丸く表示する方法を教えて」

<div class="highlight">

**座学はここまで！次は実践で80分間、Webサイトを作ります**

</div>

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

## 制作時間：80分（3段階）

### Phase別タイムライン

<div class="schedule-grid">
<span class="schedule-time">Phase 1（0-25分）</span><span>土台作り：navbar + ヒーローセクション</span>
<span class="schedule-time">Phase 2（25-55分）</span><span>コンテンツ充実：card 3つ + 説明文100字以上</span>
<span class="schedule-time">Phase 3（55-80分）</span><span>磨き上げ：カスタマイズ + 最終調整</span>
</div>

<div class="highlight">

**25分・55分時点で全員メインルームに戻り、進捗確認を行います**

</div>

**チームワーク**:

- わからないことはチームメンバーに聞く
- 助け合いながら進める
- 講師も巡回してサポート

---

## 成果発表

### 発表内容（1人約3分）

1. **何を作ったか**（テーマ）
2. **工夫したポイント**
3. **つまずいたポイント**
4. **AIをどう活用したか**（任意）

**発表時間**: 43分（15人 × 約3分）

<div class="highlight">

**簡潔に発表しよう！** 工夫点・つまずき点・AI活用に焦点を絞って

</div>

---

<!-- _class: title -->

# まとめ

---

## 今日学んだこと

### 4つの重要な概念

1. **論理と見た目の分離**
   - HTMLは構造・意味、CSSは見た目・デザイン
   - **SEO**: Googleは構造を見ている
   - **アクセシビリティ**: スクリーンリーダーが構造を読む
   - **目次作成**: 見出し構造から自動生成
   - **一括デザイン変更**: CSSで全ページを変更可能

2. **HTMLは文章構造のマークアップ**
   - デザインではなく、意味を与えるもの
   - h1は「ページの主題」、h2は「中見出し」

3. **CSSは見た目の調整**
   - 文字色、背景色、余白などを調整
   - HTMLとCSSを分離することで柔軟性が向上

4. **Bootstrapは効率的なWeb制作ツール**
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
