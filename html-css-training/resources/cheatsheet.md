# HTML/CSS/Bootstrap チートシート

## HTMLタグ一覧

### 見出し（h1-h6）

```html
<h1>大見出し</h1>
<h2>中見出し</h2>
<h3>小見出し</h3>
<h4>さらに小さい見出し</h4>
<h5>もっと小さい見出し</h5>
<h6>最も小さい見出し</h6>
```

**使い分け**:
- `h1`: ページ全体のタイトル（1ページに1つ）
- `h2`: 大きなセクションの見出し
- `h3`: サブセクションの見出し

---

### 段落（p）

```html
<p>これは段落です。文章を書くときに使います。</p>
```

---

### リスト（ul/ol、li）

**箇条書きリスト（ul）**:

```html
<ul>
  <li>項目1</li>
  <li>項目2</li>
  <li>項目3</li>
</ul>
```

**番号付きリスト（ol）**:

```html
<ol>
  <li>最初</li>
  <li>次</li>
  <li>最後</li>
</ol>
```

---

### グループ化（div、span）

**div（ブロック要素）**:

```html
<div>
  <h2>セクション</h2>
  <p>内容</p>
</div>
```

**span（インライン要素）**:

```html
<p>これは<span>強調したい部分</span>です。</p>
```

---

### 画像（img）

```html
<img src="image.jpg" alt="画像の説明">
```

**属性**:
- `src`: 画像のURL
- `alt`: 画像の説明文（SEO対策、アクセシビリティ）

---

### リンク（a）

```html
<a href="https://example.com">リンクテキスト</a>
```

**属性**:
- `href`: リンク先のURL
- `target="_blank"`: 新しいタブで開く

---

## CSS最小限

### 文字色（color）

```css
h1 {
  color: blue;
}

/* 16進数カラーコード */
h1 {
  color: #2563eb;
}
```

---

### 背景色（background-color）

```css
body {
  background-color: #f0f0f0;
}

div {
  background-color: lightblue;
}
```

---

### ボーダー（border）

```css
div {
  border: 2px solid black;
}

/* 個別指定 */
div {
  border-width: 2px;
  border-style: solid;
  border-color: black;
}
```

**border-style**:
- `solid`: 実線
- `dashed`: 破線
- `dotted`: 点線

---

### 余白（padding、margin）

**padding（内側の余白）**:

```css
div {
  padding: 20px;
}

/* 個別指定 */
div {
  padding-top: 10px;
  padding-right: 20px;
  padding-bottom: 10px;
  padding-left: 20px;
}
```

**margin（外側の余白）**:

```css
div {
  margin: 20px;
}

/* 個別指定 */
div {
  margin-top: 10px;
  margin-right: 20px;
  margin-bottom: 10px;
  margin-left: 20px;
}
```

**ボックスモデル**:

```
┌─────────────────────────┐
│  margin（外側の余白）      │
│  ┌───────────────────┐   │
│  │  border           │   │
│  │  ┌─────────────┐  │   │
│  │  │  padding    │  │   │
│  │  │  ┌───────┐  │  │   │
│  │  │  │content│  │  │   │
│  │  │  └───────┘  │  │   │
│  │  └─────────────┘  │   │
│  └───────────────────┘   │
└─────────────────────────┘
```

---

## Bootstrapクラス一覧

### グリッドシステム

**基本構造**:

```html
<div class="container">
  <div class="row">
    <div class="col-md-4">列1</div>
    <div class="col-md-4">列2</div>
    <div class="col-md-4">列3</div>
  </div>
</div>
```

**カラムクラス**:
- `col-md-1` 〜 `col-md-12`: 1/12 〜 12/12 幅
- `col-md-4` × 3 = 3カラム（4+4+4=12）
- `col-md-6` × 2 = 2カラム（6+6=12）

**レスポンシブ対応**:
- `col-sm-*`: スマホ横以上（≥576px）
- `col-md-*`: タブレット以上（≥768px）
- `col-lg-*`: PC以上（≥992px）
- `col-xl-*`: 大画面PC以上（≥1200px）

---

### コンポーネント

**navbar（ナビゲーションバー）**:

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">サイト名</a>
  </div>
</nav>
```

**card（カード）**:

```html
<div class="card">
  <img src="image.jpg" class="card-img-top" alt="画像">
  <div class="card-body">
    <h5 class="card-title">タイトル</h5>
    <p class="card-text">説明文</p>
    <a href="#" class="btn btn-primary">ボタン</a>
  </div>
</div>
```

**button（ボタン）**:

```html
<button class="btn btn-primary">ボタン</button>
<button class="btn btn-success">成功</button>
<button class="btn btn-danger">危険</button>
<button class="btn btn-outline-secondary">アウトライン</button>
```

---

### ユーティリティクラス

**余白（margin、padding）**:

| クラス | 意味 |
|--------|------|
| `mt-0` | margin-top: 0 |
| `mt-1` | margin-top: 小 |
| `mt-2` | margin-top: やや小 |
| `mt-3` | margin-top: 中 |
| `mt-4` | margin-top: やや大 |
| `mt-5` | margin-top: 大 |

**方向**:
- `mt-*`: margin-top
- `mb-*`: margin-bottom
- `ms-*`: margin-start（左）
- `me-*`: margin-end（右）
- `mx-*`: margin 左右
- `my-*`: margin 上下
- `m-*`: margin 全方向

**padding も同様**:
- `pt-*`, `pb-*`, `ps-*`, `pe-*`, `px-*`, `py-*`, `p-*`

---

**テキスト配置**:

| クラス | 意味 |
|--------|------|
| `text-start` | 左揃え |
| `text-center` | 中央揃え |
| `text-end` | 右揃え |

---

**文字色**:

| クラス | 色 |
|--------|-----|
| `text-primary` | 青 |
| `text-success` | 緑 |
| `text-danger` | 赤 |
| `text-warning` | 黄 |
| `text-info` | 水色 |
| `text-white` | 白 |
| `text-dark` | 黒 |
| `text-muted` | グレー |

---

**背景色**:

| クラス | 色 |
|--------|-----|
| `bg-primary` | 青 |
| `bg-success` | 緑 |
| `bg-danger` | 赤 |
| `bg-warning` | 黄 |
| `bg-info` | 水色 |
| `bg-light` | 明るいグレー |
| `bg-dark` | 暗いグレー |

---

**display**:

| クラス | 意味 |
|--------|------|
| `d-none` | 非表示 |
| `d-block` | ブロック表示 |
| `d-inline` | インライン表示 |
| `d-flex` | フレックスボックス |

---

### よく使う組み合わせ

**中央揃えのカード**:

```html
<div class="card text-center">
  <div class="card-body">
    <h5 class="card-title">タイトル</h5>
    <p class="card-text">説明文</p>
  </div>
</div>
```

**余白付きのセクション**:

```html
<div class="container mt-5 mb-5">
  <h2>セクションタイトル</h2>
  <p>内容</p>
</div>
```

**3カラムグリッド（レスポンシブ）**:

```html
<div class="row">
  <div class="col-md-4 mb-3">
    <div class="card">...</div>
  </div>
  <div class="col-md-4 mb-3">
    <div class="card">...</div>
  </div>
  <div class="col-md-4 mb-3">
    <div class="card">...</div>
  </div>
</div>
```

---

## AIへの質問例

### HTML関連

- 「HTMLでリストを作る方法を教えて」
- 「HTMLで画像を表示する方法を教えて」
- 「HTMLでリンクを作る方法を教えて」

### CSS関連

- 「h1タグの文字色を青にするCSSを教えて」
- 「divタグに背景色をつける方法を教えて」
- 「CSSでボーダーをつける方法を教えて」
- 「CSSで余白を調整する方法を教えて」

### Bootstrap関連

- 「Bootstrapで3カラムのカードレイアウトを作りたい」
- 「Bootstrapのnavbarに自分のサイト名を入れる方法を教えて」
- 「Bootstrapで画像を丸く表示する方法を教えて」
- 「Bootstrapでボタンの色を変える方法を教えて」

---

## 参考リンク

- **Bootstrap公式ドキュメント**: https://getbootstrap.com/
- **MDN Web Docs（HTML）**: https://developer.mozilla.org/ja/docs/Web/HTML
- **MDN Web Docs（CSS）**: https://developer.mozilla.org/ja/docs/Web/CSS
