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
  section.title p {
    color: white;
    font-size: 1.3rem;
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
  .schedule-grid-two {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
  }
  .schedule-grid-small {
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 0.2rem 0.6rem;
    font-size: 0.8rem;
  }
  .schedule-time-small {
    font-weight: 600;
    color: #2563eb;
    font-size: 0.75rem;
  }
---

<!-- _class: title -->

# DB研修<br>データ設計の本質を掴む

AI時代に生き残るエンジニアの核心スキル

---

## タイムスケジュール

<div class="schedule-grid-two">

<div class="schedule-grid-small">

<div class="schedule-time-small">13:00</div>
<div>オープニング：前回アンケートフィードバック/趣旨説明</div>

<div class="schedule-time-small">13:10</div>
<div>導入：Instagramの"データ"を列挙する</div>

<div class="schedule-time-small">13:30</div>
<div>演習1：Instagramの非正規データを正規化</div>

<div class="schedule-time-small">14:00</div>
<div>演習解答1：答え合わせと解説</div>

<div class="schedule-time-small">14:20</div>
<div>演習2：業務システムの正規化</div>

<div class="schedule-time-small">14:45</div>
<div>演習解答2：ポイント解説と質疑応答</div>

</div>

<div class="schedule-grid-small">

<div class="schedule-time-small">14:55</div>
<div>休憩</div>

<div class="schedule-time-small">15:00</div>
<div>チーム演習導入</div>

<div class="schedule-time-small">15:15</div>
<div>チーム演習：アプリ案のDB設計とテストデータ投入（70分）</div>

<div class="schedule-time-small">16:25</div>
<div>チーム発表</div>

<div class="schedule-time-small">16:40</div>
<div>総括：4月からの新卒研修に向けた展望、本日のまとめ</div>

<div class="schedule-time-small">16:50</div>
<div>終了</div>

</div>

</div>

---

## 研修の目的とゴール

### 本日の研修の趣旨

**SQLやツール操作ではなく「データ設計の本質」を理解する**

### 最終ゴール

- **DB正規化の概念を理解し、重複のない効率的な表を作成できる**
- **設計ミスがシステムに与える影響を理解し、設計の重要性を自覚する**


---

## なぜDB設計が重要なのか

### システム開発における設計の位置づけ

- **DBの設計ミスは後から修正が極めて困難**
- **プログラムではなく、データ設計が機能の限界を決める**
- **正しい設計が開発コストとシステムの寿命を左右する**

<div class="warning">

**重要**: データ設計の失敗は、プロジェクト全体に甚大な影響を与える

</div>

---

## 身近な例で考える - Instagram

### Instagramの構造を分解してみる

- **ユーザー**
- **投稿**
- **コメント**
- **いいね**

### これらをどう表（テーブル）にするか？

---


## 演習1

### 題材

**Instagramの非正規データ**

### ミッション

**重複を排除し、効率的な複数の表に分割する**

### 実施方法

- チームで協力して25分間で取り組む
- ※演習はGoogleスプレッドシートを使用

---

## 演習1で学ぶ3つのポイント

### ①別人問題（主キーの必要性）

表示名が同じ人が複数いたら？

### ②改名問題（不変性）

ユーザー名が変わっても過去データとの紐付けは？

### ③多対多の関係（中間テーブル）

投稿と「いいね」ユーザーの関係をどう表現？

---

## 正規化の本質

### 正規化とは

- **データの重複を排除する**
- **一つの事実は一箇所にだけ保存する**
- **更新時の矛盾を防ぐ**
- **「属性」ではなく「ID」で管理する**

<div class="highlight">

重複のないデータ構造が、システムの堅牢性を支える

</div>

---

## 読まれた合計時間ランキング

### 後出し要件の例

**「この投稿が読まれた合計時間」ランキングを表示したい**

### 実装可能にするための設計

- 設計段階で「**誰が**」「**いつから**」「**いつまで**」読んだかを保持する「箱」が必要
- これがなければ実装不可能

<div class="highlight">

**データ設計が機能の限界を決める実例**

</div>

---

## 演習2

### 題材

**業務システム（法人の拠点・契約・担当者管理）**

### ポイント

- 演習1で学んだロジックを実務ドメインに適用
- **会社名ではなく法人番号（ID）で管理する重要性**

---


## チーム演習の説明

### 内容

**AI活用研修で考案した「アプリ案」のDB設計**

### ステップ

1. **どのアプリを作るか、また、その機能の洗い出し**
2. **チームでアプリのデータ構造を議論**
3. **スプレッドシートで表を設計**
4. **AIにCSVデータを生成させる**
5. **データをインポートして動作確認**

---

## AI活用Tips

### 人間とAIの役割分担

- **人間の役割：データ構造（スキーマ）の設計**
- **AIの役割：テストデータの生成**

### 活用のポイント

- AIにデータを生成させる際のプロンプト
- CSV形式でのエクスポート/インポート方法

---

## チーム演習レギュレーション

### 実施内容

- **時間：70分**
- **評価ポイント：構造の「美しさ（重複のなさ）」**
- **発表内容：アプリ概要/作成したDB構造**

### 意識すること

- **「表で保存」**
- **「重複させない」**
- **「IDで管理」**

### 特別ルール
- **「設計はAIに任せないで、人間が考える」**

---

## 本日のまとめ - 3つの原則

### ①表で保存する

データは表形式で整理する

### ②重複させない

同じ情報は一箇所だけに保存

### ③属性ではなくIDで管理する

名前ではなく一意のIDを使う

---

## 4月からの新卒研修に向けて

### 本日学んだことが全ての基礎

- **本日学んだ正規化の考え方が全ての基礎**
- **SQLやプログラミング言語は後から学べる**
- **重要なのは「構造を考える力」**

**「構造を考える力」= AI時代に生き残るエンジニアの核心スキル**
