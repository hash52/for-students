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
    gap: 2rem;
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
    padding: 0.6rem;
    border-radius: 0.4rem;
    font-size: 0.85rem;
    overflow-x: auto;
    border: 1px solid #d0d7de;
    margin: 0.5rem 0;
  }
  /* シンタックスハイライト調整 */
  pre code .hljs-tag { color: #116329; }
  pre code .hljs-attr { color: #0550ae; }
  pre code .hljs-string { color: #0a3069; }
---

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
- PostgreSQL, Elasticsearch

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
<span class="schedule-time">13:30-13:40</span><span>ブラウザの仕組み + なぜソースを書くのか</span>
<span class="schedule-time">13:40-13:55</span><span>座学① HTML基礎（文章構造）</span>
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
2. ファイルを開く
3. 右クリック → **「Open with Live Server」**
4. ブラウザで表示されることを確認

<div class="warning">

**動かない場合**：講師に知らせてください。個別にサポートします

</div>

---

## 【体験演習】Webサイトの裏側を見てみよう

### ブラウザの検証ツールを使ってみよう（5分）

**やること**:

1. ブラウザでWebサイトを開く
2. 右クリック → **「検証」**
3. 発見すること：
   - 普段見ている画面の裏に「文字」が隠れている？
   - サイト内で、どんな規則性がある？
   - サイトを跨いで、共通するルールはある？

<div class="highlight">

**目標**: 普段見ている画面が「テキスト情報」から作られていることを体感しよう

</div>

---

## ブラウザの仕組み

### Webサイトはどう表示されている？

**発見したこと**:
- 裏側には「タグ（<>）」や「テキスト」による**命令書**がある
- 私たちが見ているのは、その命令書をブラウザが解釈した結果

<div class="two-columns">

<div>

**ブラウザがやっていること**

1. **ソースコード（命令書）** を読み込む
2. 命令に従って画面を描画する

</div>

<div>

**つまり**

- スマホもPCも仕組みは同じ
- **「ソースコード」** さえあれば表示できる
- 綺麗な画面も、元はただの文字情報

</div>

</div>

---

## なぜ「ソースコード」を学ぶのか？

### 便利なツール（Wix, WordPress）があるのに？

<div class="two-columns">

<div>

**ツールの限界（NoCodeなど）**
- 用意された機能しか使えない
- 「あと少しここを直したい」ができない

**AI時代の最大のメリット**
- **AIはソースコードを完璧に理解している**
- AIという「最強の大工」に指示を出すには、「壁」や「柱」の **名前（概念）** を知る必要がある

</div>

<div>

**概念を知らないと...**
❌ 「なんかいい感じにして」
→ AIも困る

**概念を知っていると...**
✅ 「ナビゲーションバーを右寄せにして」
→ AIが正確にコードを書く

**結論：AIへの指示出しのために学ぶ**

</div>

</div>

---

# 座学①
# HTML基礎

---

## HTMLは「文章構造」の定義

### 見た目のためではなく、意味を与えるもの

<div class="two-columns">

<div>

**HTMLの役割**

- デザインをする道具**ではない**
- **「これは見出し」「これは段落」** と定義する道具
- コンピュータに文章の**構造**を伝える

**新聞で例えると**

- 大見出し / 中見出し
- 本文 / 箇条書き
- 写真 / キャプション

</div>

<div>

**文章構造の例**

```html
<h1>一番大事な見出し</h1>
<p>これは段落です。</p>
<ul>
  <li>箇条書き1</li>
  <li>箇条書き2</li>
</ul>
```

→ これらに**意味**を与える作業

</div>

</div>

<div class="highlight">

**重要**: 色を変えたり中央寄せにするのは、HTMLの仕事ではありません！

</div>

---

## 良い例 vs 悪い例

### 見た目は同じでも、構造が違う！

<div class="two-columns">

<div>

**良い例：正しいタグで構造化**

```html
<h1>今日のニュース</h1>
<p>本文です。</p>
```

✅ コンピュータが「見出し」と認識
✅ 視覚障害者用ソフトが正しく読み上げ
✅ AIに「見出しのデザイン変えて」と言える
✅ 目次を自動生成できる

</div>

<div>

**悪い例：見た目だけの調整**

```html
<div style="font-size:30px">
  今日のニュース
</div>
<div>本文です。</div>
```

❌ ただの「大きな文字」と認識される
❌ 構造が伝わらない
❌ 後で修正するのが大変

</div>

</div>

---

## HTMLの基本構造

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>ページタイトル</title>
  </head>
<body>
  <h1>ようこそ</h1>
  <p>こんにちは。</p>
</body>
</html>
```

- `<head>`: ページの設定（タイトルなど、画面には出ない）
- `<body>`: 実際に画面に表示される内容

---

## よく使うHTMLタグ

| タグ | 意味 | 使い方のイメージ |
|------|------|-----|
| `<h1>` | 大見出し | ページのタイトル |
| `<h2>` | 中見出し | 章のタイトル |
| `<p>` | 段落 | 普通の文章 |
| `<ul>` `<li>` | リスト | 箇条書き |
| `<img>` | 画像 | 画像の埋め込み |
| `<a>` | リンク | ページ移動 |
| `<div>` | グループ化 | まとまりを作る |

<div class="highlight">

**細かい文法は覚えなくてOK！** 「リストを作るタグは何？」とAIに聞けばいい

</div>

---

## タグの入れ子構造

```html
<div>
  <h2>セクションのタイトル</h2>
  <p>説明文です。</p>
  <ul>
    <li>ポイント1</li>
    <li>ポイント2</li>
  </ul>
</div>
```

**ルール**:

- タグの中にタグを入れられる（マトリョーシカのイメージ）
- **開いたら必ず閉じる**（例：`<div>...</div>`）
- これにより「ここからここまでがひとまとまり」と表現する

---

## 体験① HTMLで文章構造を作る

### 自己紹介ページの構造を作ろう（10分）

**やること**:

- テンプレート（`01_html-structure.html`）を使う
- h1、h2、p、ul/liといったタグを付与していく
- **デザインは一切せず、構造のみに集中**

**AI活用OK**: わからなければChatGPTに聞こう
例：「HTMLでリストを作る方法を教えて」

<div class="highlight">

**ポイント**: 構造を意識して、適切なタグを使おう！

</div>

---

# 座学②
# CSS

---

## CSSの役割：見た目をデザインする

### HTMLは「構造」、CSSは「見た目」

<div class="two-columns">

<div>

**役割分担**

- **HTML (骨組み)**
  - 「ここは見出し」「ここはリスト」
- **CSS (肉付け)**
  - 「文字を赤く」「右に寄せる」

**CSSでできること**

- 文字の色や大きさを変える
- 背景に色をつける
- 余白を調整して見やすくする

</div>

<div>

**基本的な書き方**

「**どこの**」 「**何を**」 「**どうするか**」

```css
/* h1タグの 文字色を 青にする */
h1 {
  color: blue;
}
```

1. **セレクタ**: どこの (`h1`)
2. **プロパティ**: 何を (`color`)
3. **値**: どうする (`blue`)

</div>

</div>

---

## まず覚えるプロパティとツール

### 最小限の知識でスタートしよう

<div class="two-columns">

<div>

**頻出プロパティ 4選**

| プロパティ | 意味 | メモ |
|-----------|------|---|
| `color` | 文字色 | 文字自体の色 |
| `background` | 背景色 | 背景の色 |
| `padding` | **内側**の余白 | 枠線と文字の間 |
| `margin` | **外側**の余白 | 隣の要素との距離 |

</div>

<div>

**Chrome検証ツールの活用**

Webサイトの「デザインの種明かし」を見る

1. 気になる場所で右クリック → **「検証」**
2. **Styles**タブを見る（CSSが表示される）

</div>

</div>

<div class="highlight">

**AI活用のコツ**:
検証ツールで見慣れない単語（例: `border-radius`）を見つけたら、AIに「これ何？」と聞くのが一番の近道！

</div>

---

## 特定の要素だけデザインするには？

### 「タグ」指定の限界と「クラス」の登場

<div class="two-columns">

<div>

**タグ指定の弱点**

```css
p { color: red; }
```
これだと、ページ内の**全ての `<p>` が赤くなってしまう**。
「この段落だけ赤くしたい」ができない。

<br>

**解決策：クラス (class) を使う**

要素に「**名札（クラス名）**」をつけて、
その名前に対してスタイルを指定する。

</div>

<div>

**書き方のルール**

1. HTMLで名前をつける (`class="..."`)
2. CSSで **ドット(.)** をつけて指定する

**コード例**

```html
<p class="kaisetsu">ここは赤くなる</p>
<p>ここは普通のまま</p>
```

```css
/* CSS */
.kaisetsu {
  color: red;
}
```

</div>

</div>

---

## 何も意味を持たない「透明な箱」

### Web制作の必須アイテム：`<div>` と `<span>`

<div class="two-columns">

<div>

**特定の意味を持たないタグ**

`h1`（見出し）や `p`（段落）と違い、
これら自体には**意味がない**。

**じゃあ何に使うの？**

1. **グループ化する**
   複数の要素をまとめて、背景色をつけたりレイアウトを変えたりする。
2. **デザインのターゲットにする**
   「ここだけ色を変えたい」という場所に目印をつける。

</div>

<div>

**代表的な2つの箱**

- **`<div>` (ディブ)**
  - 大きな箱。
  - **レイアウトの骨組み**を作るのに使う。
- **`<span>` (スパン)**
  - 小さな袋。
  - **文章の一部**だけを装飾するのに使う。

</div>

</div>

---

## div と span の決定的な違い

### 「改行されるか、されないか」

<div class="two-columns">

<div>

**`<div>` = ブロック（積み木）**

- 前後に**改行が入る**
- 横幅いっぱいに広がる
- 「セクション」や「行」を作る

```html
<div>箱1</div>
<div>箱2</div>
```
↓
**[ 箱1 ]**
**[ 箱2 ]**
（縦に積まれる）

</div>

<div>

**`<span>` = インライン（マーカー）**

- **改行されない**（文章の途中に入れられる）
- 文字の長さ分しか幅を取らない
- 文中の「ここだけ」を変える

```html
<p>今日は<span>晴れ</span>です</p>
```
↓
今日は**晴れ**です
（横に並ぶ）

</div>

</div>


---

## 体験② CSSミニワーク

### クラスを使って箱（div）をデザインする（10分）

**ミッション**:

1. HTMLの `div` タグに `class="box"` という名前をつける
2. CSSで `.box` に対して**背景色** (`background-color`) を**水色**に指定する
3. **内側の余白** (`padding`) を**20px**に指定する

**AIへの質問例**:

- 「HTMLのdivにクラスをつける書き方は？」
- 「CSSで.boxに背景色を水色にして、余白を20pxにするコードは？」

<div class="highlight">

**目標**: 
**「名札(class)をつける」** → **「CSSでドット(.)で指定する」** の流れを掴む。
**「padding（内側の余白）」** の効果を確認する。

</div>

---


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

**読み込み（例）**

```html
<link href="...bootstrap.min.css" ...>
```

**ボタンを作る例**:

```html
<button class="btn btn-primary">
  ボタン
</button>
```

→ クラス名を書くだけで青いボタンが完成
→ 公式サイトからコピペでOK

</div>

</div>

---

## グリッドシステム + コンポーネント

<div class="two-columns">

<div>

**グリッドシステム (12分割)**
`row`(行)の中に`col`(列)を作る

```html
<div class="container">
  <div class="row">
    <div class="col-md-4">左</div>
    <div class="col-md-4">中</div>
    <div class="col-md-4">右</div>
  </div>
</div>
```

- `col-md-4`: PC/タブレットで4/12幅
- スマホでは自動で全幅になる

</div>

<div>

**よく使うコンポーネント**

**Navbar** (ナビゲーション)
```html
<nav class="navbar navbar-light bg-light">
  <a class="navbar-brand">Logo</a>
</nav>
```

**Card** (情報の箱)
```html
<div class="card">
  <div class="card-body">
    <h5>タイトル</h5>
  </div>
</div>
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

# 実践
# Bootstrap Web制作演習

---

## 実践：「好きなもの」サイト制作

### テーマ：あなたの「推し」を紹介しよう

**内容**
**自分の好きなもの**に関するWebサイトを作る
（ゲーム、アイドル、スポーツ、趣味、ペットなど何でもOK）

**時間** : **80分**

<div class="highlight">

**細かい要件はありません！**
今日学んだ `Navbar` `Grid` `Card` などを組み合わせて、
AIと相談しながら **「自分が楽しいと思えるサイト」** を作ってください。

</div>

---

## AI活用を積極的に推奨

### 開発フロー：わからなければすぐAI

**AI活用の4ステップ**:

1. **概念を思い出す**（座学で聞いた「グリッド」「Navbar」などの単語）
2. **AIに質問する**（やりたいことを具体的に伝える）
3. **コードをコピペ**してブラウザで確認
4. **動かない場合**はエラー内容や状況をAIに伝えて修正

<div class="highlight">

**ポイント**:
「自分でコードを全部書く」のではなく、**「AIが出したコードを監督する」** 気持ちで進めましょう。

</div>

---

## AIへのプロンプト例（基本編）

### コピペして少し変えるだけで使えます

<div class="two-columns">

<div>

**レイアウトを作りたい時**

> Bootstrap 5を使っています。
> 画面上部にナビゲーションバー、その下に大きなメイン画像、その下に3列のカードが並ぶレイアウトの**HTMLコードのみ**を書いてください。

**ナビゲーションを作りたい時**

> BootstrapのNavbarを作りたいです。
> 左側に「My Favorite」、右側に「Home」「About」「Link」というメニューを配置するコードを教えて。

</div>

<div>

**カードを作りたい時**

> 画像とタイトルと短い説明文が入ったBootstrapのCardコンポーネントのコードを教えて。
> 幅はスマホで1列、PCで3列になるようにグリッドシステムを使ってください。

**色を変えたい時**

> Navbarの背景色を、黒ではなく自分の好きな色（#ff9900）に変えるためのCSSの書き方を教えて。

</div>

</div>

---

## 発表を盛り上げるために：本物の画像を使おう


**手順1：画像を保存する「箱」を作る**

1. VSCodeの左側（ファイル一覧）の何もないところを右クリック
2. **「新しいフォルダー」** を選択
3. 名前を `images` にする

<div class="two-columns">

<div>

**フォルダ構成のイメージ**

```text
📂 プロジェクトフォルダ
 ┣ 📄 index.html
 ┗ 📂 images  <-- ここに保存
    ┣ 🖼 game.jpg
    ┗ 🖼 cat.png
```

</div>

<div>

**手順2：画像をダウンロード**

1. Google画像検索などで好きな画像を探す
2. 画像を右クリック → **「名前を付けて画像を保存」**
3. さっき作った `images` フォルダの中に保存
（例：`game1.png` など）

</div>

</div>

---

## 保存した画像をHTMLで表示する

### パス（ファイルの住所）を指定する

HTMLファイルから見て、「`images`フォルダの中の `ファイル名`」を指定します。

**書き方の基本**

```html
<img src="images/game1.jpg" class="img-fluid">
```

<div class="highlight">

**ポイント**:
`class="img-fluid"` (Bootstrapのクラス) をつけると、
画像が画面からはみ出さずに、いい感じで縮小してくれます。

</div>

---

## 画像が出ない！(404) ときのAI対処法

### パス（場所）の間違いは、AIに見てもらおう

「保存したはずなのに、画像が割れたマークになる…」
→ **VSCodeのファイル構成**をそのまま伝えると解決します。

<div class="highlight">

**AIへのプロンプト例**:

> HTMLで画像を表示したいのですが、表示されません。
>
> **今の状況**:
> - HTMLファイル：ルート直下の index.html
> - 画像ファイル：imagesフォルダの中にある game1.jpg
>
> **書いたコード**:
> `<img src="game1.jpg">`
>
> 正しい書き方を教えてください。

</div>

**コツ**: 「どのファイルがどこにあるか」を伝えると、AIは正しいパス（`images/game1.jpg`）を教えてくれます。

---

## 制作時間：80分


**チームワーク**:

- わからないことはチームメンバーに聞く
- 助け合いながら進める
- 講師も巡回してサポート

---

## 成果発表

### 発表内容（1人約3分）

1. **何を作ったか**
2. **選んだテーマの魅力**
3. **工夫したポイント/つまずいたポイントなど**

**発表時間**: 45分（15人 × 約3分）

---

# まとめ

---

## 今日学んだこと

### 4つの重要な概念

1. **論理と見た目の分離**
   - HTMLは構造・意味、CSSは見た目・デザイン
   - **AI活用**: 構造がわかればAIに正確な指示が出せる

2. **HTMLは文章構造のマークアップ**
   - h1は「ページの主題」、h2は「中見出し」

3. **CSSは見た目の調整**
   - プロパティ名は覚えなくても「余白を変えたい」と言えればOK

4. **Bootstrapは効率的なWeb制作ツール**
   - 公式ドキュメントからコピペでOK
   - 12カラムグリッドでレスポンシブも簡単

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

# ご清聴ありがとうございました

**質問があればいつでも連絡してください！**