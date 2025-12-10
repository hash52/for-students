# VSCode + Live Server セットアップ手順

## 1. VSCodeのインストール

### Windows / Mac 共通

1. **公式サイトにアクセス**
   - URL: https://code.visualstudio.com/

2. **ダウンロード**
   - 「Download for Windows」または「Download for Mac」をクリック

3. **インストール**
   - ダウンロードしたファイルを開く
   - 指示に従ってインストール

---

## 2. Live Server拡張機能のインストール

### 手順

1. **VSCodeを開く**

2. **拡張機能タブを開く**
   - 左サイドバーの四角いアイコンをクリック
   - または `Cmd+Shift+X`（Mac） / `Ctrl+Shift+X`（Windows）

3. **Live Serverを検索**
   - 検索バーに「Live Server」と入力
   - 「Live Server」（作者: Ritwick Dey）を選択

4. **インストール**
   - 「Install」ボタンをクリック
   - インストール完了まで数秒待つ

---

## 3. HTMLファイルの開き方

### 新しいHTMLファイルを作成

1. **ファイル → 新規ファイル**（`Cmd+N` / `Ctrl+N`）

2. **ファイルを保存**
   - 「ファイル → 名前を付けて保存」
   - ファイル名を `index.html` にする
   - 保存場所を選ぶ

3. **HTMLコードを書く**
   - テンプレートをコピペするか、自分で書く

---

## 4. Live Serverの起動方法

### 方法1: 右クリックから起動

1. **HTMLファイルを開く**

2. **エディタ内で右クリック**

3. **「Open with Live Server」を選択**

4. **ブラウザが自動的に開く**
   - `http://127.0.0.1:5500/index.html` のようなURLで開く

### 方法2: ステータスバーから起動

1. **HTMLファイルを開く**

2. **画面下部のステータスバーの「Go Live」をクリック**

3. **ブラウザが自動的に開く**

---

## 5. 使い方のコツ

### ファイルを編集すると即座に反映

1. **HTMLを編集**

2. **保存**（`Cmd+S` / `Ctrl+S`）

3. **ブラウザが自動的に更新される**
   - わざわざブラウザをリロードしなくてOK！

### Live Serverを停止する

- ステータスバーの「Port: 5500」をクリック
- または右クリック → 「Stop Live Server」

---

## トラブルシューティング

### Live Serverが起動しない

**原因1: 拡張機能がインストールされていない**

- 解決策: 拡張機能タブで「Live Server」を検索してインストール

**原因2: HTMLファイルが保存されていない**

- 解決策: ファイルを保存してから起動

**原因3: ポート5500が既に使われている**

- 解決策: 他のアプリを閉じるか、VSCodeを再起動

### ブラウザが開かない

**原因: デフォルトブラウザが設定されていない**

- 解決策:
  1. VSCodeの設定を開く（`Cmd+,` / `Ctrl+,`）
  2. 「Live Server」で検索
  3. 「Live Server > Settings: Custom Browser」を設定

### ファイルの変更が反映されない

**原因: 保存していない**

- 解決策: 必ず `Cmd+S` / `Ctrl+S` で保存

**原因: キャッシュが残っている**

- 解決策: ブラウザで `Cmd+Shift+R` / `Ctrl+Shift+R` でスーパーリロード

---

## よくある質問

### Q: VSCodeは無料ですか？

A: はい、完全無料です。

### Q: Live Server以外の拡張機能も入れるべきですか？

A: 最初は不要です。慣れてきたら以下を検討：
- Auto Rename Tag（タグを自動でリネーム）
- HTML CSS Support（コード補完）
- Prettier（コード整形）

### Q: VSCodeが重い場合はどうすればいいですか？

A: 以下を試してください：
1. 不要な拡張機能を無効化
2. VSCodeを再起動
3. PCを再起動

---

## 参考リンク

- **VSCode公式サイト**: https://code.visualstudio.com/
- **Live Server拡張機能**: https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer
- **VSCode日本語ドキュメント**: https://code.visualstudio.com/docs
