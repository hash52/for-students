# 画像素材リソース

## 無料画像素材サイト

### Unsplash

**URL**: https://unsplash.com/

**特徴**:
- 高品質な写真が豊富
- 完全無料
- クレジット表記不要（推奨）
- 商用利用OK

**使い方**:
1. キーワードで検索（例：「game」「anime」「sport」）
2. 気に入った画像をクリック
3. 「Download」をクリック
4. 画像URLをコピーして使用

**おすすめのキーワード**:
- ゲーム: game, gaming, controller
- スポーツ: soccer, basketball, sports
- 食べ物: food, ramen, sushi
- 自然: nature, mountain, sea
- 都市: city, tokyo, building

---

### Pixabay

**URL**: https://pixabay.com/ja/

**特徴**:
- 写真・イラスト・動画が利用可能
- 完全無料
- クレジット表記不要
- 商用利用OK
- 日本語対応

**使い方**:
1. 検索バーにキーワードを入力
2. 「写真」「イラスト」「ベクター」を選択
3. 気に入った画像をクリック
4. 「無料ダウンロード」をクリック

**おすすめのキーワード**:
- アニメ: anime, manga, character
- アイドル: idol, music, concert
- 技術: technology, programming, computer
- ファッション: fashion, clothing, style

---

### Pexels

**URL**: https://www.pexels.com/ja-jp/

**特徴**:
- 高品質な写真・動画
- 完全無料
- クレジット表記不要
- 商用利用OK
- 日本語対応

**使い方**:
1. キーワードで検索
2. 気に入った画像をクリック
3. 「無料ダウンロード」をクリック

**おすすめのキーワード**:
- ビジネス: business, office, work
- 学習: study, education, book
- ライフスタイル: lifestyle, people, happy

---

### Placeholder.com

**URL**: https://placeholder.com/

**特徴**:
- **仮画像**を簡単に生成
- サイズ指定可能
- 開発・プロトタイプ作成に便利

**使い方**:

```html
<!-- 300x200の仮画像 -->
<img src="https://via.placeholder.com/300x200" alt="仮画像">

<!-- 背景色とテキスト色を指定 -->
<img src="https://via.placeholder.com/300x200/0000FF/FFFFFF" alt="青背景・白文字">

<!-- テキストを追加 -->
<img src="https://via.placeholder.com/300x200?text=Sample+Image" alt="サンプル画像">
```

**サイズ例**:
- カード用: `300x200`
- ヒーロー画像用: `1200x400`
- アイコン用: `100x100`
- 正方形: `500x500`

---

## 画像の使い方

### HTMLで画像を表示

```html
<!-- ローカルファイル -->
<img src="images/photo.jpg" alt="写真の説明">

<!-- Web上の画像（URL） -->
<img src="https://images.unsplash.com/photo-1234567890/..." alt="写真の説明">
```

### Bootstrapで画像を使う

```html
<!-- レスポンシブ画像 -->
<img src="image.jpg" class="img-fluid" alt="レスポンシブ画像">

<!-- 丸い画像 -->
<img src="image.jpg" class="rounded-circle" alt="丸い画像">

<!-- 角丸画像 -->
<img src="image.jpg" class="rounded" alt="角丸画像">

<!-- カードの中で使う -->
<div class="card">
  <img src="image.jpg" class="card-img-top" alt="カード画像">
  <div class="card-body">
    <h5 class="card-title">タイトル</h5>
  </div>
</div>
```

---

## 画像URL取得方法

### Unsplashの場合

1. 画像ページを開く
2. URLバーのURLをコピー
   - 例: `https://images.unsplash.com/photo-1234567890/...`
3. HTMLに貼り付け

```html
<img src="https://images.unsplash.com/photo-1234567890/..." alt="写真">
```

### Pixabayの場合

1. 画像ページを開く
2. 「無料ダウンロード」の上にある画像を右クリック
3. 「画像のURLをコピー」
4. HTMLに貼り付け

---

## 画像サイズの調整

### CSSで調整

```css
img {
  width: 100%;  /* 親要素の幅に合わせる */
  height: auto; /* 高さは自動調整（縦横比維持） */
}

/* 最大幅を指定 */
img {
  max-width: 500px;
  height: auto;
}

/* 特定のサイズに固定 */
img {
  width: 300px;
  height: 200px;
  object-fit: cover; /* 縦横比を維持してトリミング */
}
```

### Bootstrapで調整

```html
<!-- レスポンシブ（親要素の幅に合わせる） -->
<img src="image.jpg" class="img-fluid" alt="レスポンシブ画像">

<!-- サムネイル風 -->
<img src="image.jpg" class="img-thumbnail" alt="サムネイル">
```

---

## よくある質問

### Q: 画像が表示されません

**原因1: URLが間違っている**
- 解決策: URLをコピペし直す

**原因2: 画像のパスが間違っている**
- 解決策: `images/photo.jpg` の場所を確認

**原因3: ネット接続の問題**
- 解決策: インターネット接続を確認

### Q: 画像のサイズが大きすぎます

**解決策**: `class="img-fluid"` を追加

```html
<img src="image.jpg" class="img-fluid" alt="画像">
```

### Q: 画像を丸くしたいです

**解決策**: `class="rounded-circle"` を追加

```html
<img src="image.jpg" class="rounded-circle" alt="丸い画像">
```

---

## おすすめの画像検索キーワード（日本語）

### ゲーム関連
- ゲーム、コントローラー、eスポーツ、ゲーミング

### スポーツ関連
- サッカー、野球、バスケ、テニス、スポーツ

### アニメ・マンガ関連
- アニメ、マンガ、イラスト、キャラクター

### 音楽・アイドル関連
- 音楽、ライブ、コンサート、ステージ

### 食べ物関連
- 料理、ラーメン、寿司、カレー、食べ物

### 勉強・学習関連
- 勉強、本、図書館、学習、教育

### ファッション関連
- ファッション、服、スタイル、おしゃれ

### 自然・風景関連
- 自然、山、海、空、風景

---

## 参考リンク

- **Unsplash**: https://unsplash.com/
- **Pixabay**: https://pixabay.com/ja/
- **Pexels**: https://www.pexels.com/ja-jp/
- **Placeholder.com**: https://placeholder.com/
