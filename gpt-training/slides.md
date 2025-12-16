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
  .service-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 0.8rem;
    margin-top: 0.6rem;
  }
  .service-item {
    text-align: center;
    padding: 0.5rem;
    border: 2px solid #e5e7eb;
    border-radius: 0.6rem;
    background: #f9fafb;
  }
  .service-item img {
    width: 70px;
    height: 70px;
    object-fit: contain;
    margin-bottom: 0.3rem;
  }
  .service-item h3 {
    font-size: 1rem;
    margin: 0.2rem 0;
  }
  .service-item p {
    font-size: 0.75rem;
    color: #6b7280;
    margin: 0;
    line-height: 1.25;
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
  .profile-section {
    background: #f8fafc;
    padding: 0.8rem;
    border-radius: 0.5rem;
    margin: 0.4rem 0;
  }
---

<!-- _class: title -->

# 生成 AI 活用入門<br>体験ワークショップ

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

### 初めて生成 AI を触る人

**便利さを体感する**

- 実際に使ってみて、どんなことができるのかを知る
- 日常や仕事でどう活用できるかイメージする

### 既に生成 AI を触っている人

**より効率的な、一歩進んだ活用ができるようになる**

- プロンプトエンジニアリングの基礎を学ぶ
- より質の高い回答を引き出すテクニックを身につける

---

## 本日の流れ 📅

<div class="schedule-grid">

<div class="schedule-time">13:00 ~ 13:10</div>
<div>オープニング</div>

<div class="schedule-time">13:10 ~ 13:40</div>
<div>グループワーク①</div>

<div class="schedule-time">13:40 ~ 14:00</div>
<div>発表</div>

<div class="schedule-time">14:00 ~ 14:05</div>
<div>トイレ休憩 🚻</div>

<div class="schedule-time">14:05 ~ 14:40</div>
<div>座学① プロンプトエンジニアリング基礎</div>

<div class="schedule-time">14:40 ~ 15:50</div>
<div>グループワーク②</div>

<div class="schedule-time">15:50 ~ 16:20</div>
<div>発表</div>

<div class="schedule-time">16:20 ~ 16:50</div>
<div>座学② セキュリティとハルシネーション</div>

</div>

---

## ChatGPT とは

### 🤖 どんなサービスか

**OpenAI 社が開発した対話型 AI**

- 自然な会話でやりとりできる
- 質問に答える、文章を書く、アイデアを出すなど多様なタスクに対応
- 2022 年 11 月に公開され、世界中で爆発的に普及

### 💡 何の役に立つか

**日常生活やビジネスで幅広く活用**

- 情報検索・調べ物
- アイデア出し・ブレインストーミング
- 文章作成・添削
- プログラミング支援

---

<!-- _class: title -->

# 体験 ①

# 2 泊 3 日旅行プランを作ろう

**制限時間：20 分**

---

## 体験 ① 2 泊 3 日旅行プランを作ろう

### 📋 ワークの流れ

**① 役割分担（5 分）**

- **ファシリテーター**: 議論をリードする
- **タイムキーパー**: 時間管理
- **書記**: 内容を記録
- **発表者**: グループの成果を発表

**② ChatGPT で旅行プランを作成（15 分）**

- グループで協力して、色々な聞き方を試してみる
- より良い回答を得るための工夫を考える

---

## 体験 ① 成果物

### 📝 まとめていただきたいこと

**より良い回答を得るための方法 3 つ**

- どんな聞き方・工夫をすると良い回答が得られたか
- 具体的なプロンプト例とともに

**一番回答が微妙だったプロンプト 1 つ**

- どんな点が微妙だったか
- なぜそうなったと思うか

---

## 体験からの気づき共有

### 💬 各グループの発表

- より良い回答を得るための方法
- 失敗から学んだこと

---

<!-- _class: title -->

# 座学 ①

# プロンプトエンジニアリング基礎

---

## Q: シングルターン vs マルチターン

### どっちの精度が良い？ 🤔

<div class="two-columns">

<div>

#### シングルターン

**一度に全ての指示を詰め込む**

```
私は東京在住の30代会社員です。
2泊3日で京都旅行を計画しています。
予算は5万円で、寺社仏閣巡りと
美味しい和食を楽しみたいです。
おすすめのプランを教えてください。
```

</div>

<div>

#### マルチターン

**段階的に会話を重ねる**

```
京都に旅行したいです
→ 2泊3日です
→ 予算は5万円です
→ 寺社仏閣が好きです
→ 和食を楽しみたいです
```

</div>

</div>

---

## A: 圧倒的にシングルターン

### 📊 研究で立証されている

<div class="two-columns">

<div>

#### 研究結果

- マルチターンは能力が少し落ち、
  **信頼性がガクンと下がる**
- コーディング、数学、要約など様々なタスクで検証
- 最新モデルでも同様の傾向

**参考:** [https://arxiv.org/abs/2505.06120](https://arxiv.org/abs/2505.06120)

</div>

<div>

#### なぜ？

- **AI は最初の仮説に引っ張られる傾向が強い**
- 最初に立てた仮説から軌道修正しにくい

</div>

</div>

### 💡 実践のポイント

- **回答が微妙になってきたら、チャットの仕切り直しを**
- **できるだけ最初のプロンプトに指示を詰め込んで**

---

## 良いプロンプトの 5 要素

### 📝 質の高い回答を得るための構成要素

<div class="three-columns">

<div>

**① 指示**

- 何をしてほしいか
- 明確に具体的に

**② 文脈情報**

- 背景・前提
- 目的・用途

</div>

<div>

**③ ルール**

- 守ってほしいこと
- 制約条件

**④ フォーマット**

- 出力形式
- 構造の指定

</div>

<div>

**⑤ 例（Few-shots）**

- 具体例を示す
- 期待する形式を提示

</div>

</div>

---

## 良いプロンプトの 5 要素（例）

<div class="two-columns">

<div>

### ❌ 改善前

```
京都の旅行プランを
教えてください
```

**問題点**

- 情報が少なすぎる
- AI が推測で補完するしかない

</div>

<div>

### ✅ 改善後

```
# 指示
京都の2泊3日旅行プランを作成してください

# 文脈情報
- 東京在住の30代会社員
- 初めての京都旅行

# ルール
- 予算: 5万円以内
- 移動は公共交通機関のみ

# フォーマット
1日目、2日目、3日目で分けて時間帯ごとに記載

# 例
10:00 清水寺参拝（所要時間: 1時間）
```

</div>

</div>

---

## 構造化プロンプトとマークダウン

### 📐 情報を AI が読みやすい形で

**AI が理解しやすいフォーマットを使う**

- **Markdown**: 見出し、リストなどで構造化
- **YAML**: データを整理して渡す
- **XML**: 要素を明確に区別

### メリット

- AI が情報を正確に理解できる
- 複雑な指示を整理して伝えられる
- 再利用・修正がしやすい

---

## マークダウンとは

### 📄 シンプルなドキュメント記法

**元々はエンジニアがよく使っていた書き方**

- 文章をシンプルに構造化できる
- 特別なソフト不要。テキストエディタで書け、AI 登場以前から広く使われている

### 基本的な記法

```markdown
# 大見出し

## 中見出し

- 箇条書き 1
- 箇条書き 2
```

<div class="highlight">
💡 <strong>この2つの記法だけでも、プロンプトが格段に読みやすくなる！</strong>
</div>

---

## 逆プロンプト

### 🔄 プロンプト自体を AI に作らせる

### アプローチ

1. まず雑なプロンプトでやりたいことを伝える
2. 出力を見て「ここが違う」「もっとこうしてほしい」と伝え、
   AI にプロンプトを改善してもらう

### メリット

- **実物を見てから修正する方が効率的**
  人間は自分が欲しいものを正確に言語化できないため

### 使い方

```
この出力は〇〇が不足しています。
より良い結果が得られるプロンプトを作成してください。
```

---

## ChatGPT のプロジェクト機能

### 📁 コンテキストを再利用可能に

### プロジェクトとは

- 特定のタスクや目的のために、指示やルールをまとめておける機能
- プロジェクト内では、毎回同じ前提情報を使って AI が回答

### メリット

- **毎回同じ説明を繰り返さなくていい**
- チームで共通のプロンプトやルールを共有できる
- 一度作った良いプロンプトを資産として蓄積

### 活用例

- 「卒論執筆用」プロジェクト → 研究テーマや参考文献を登録、一貫した視点で相談
- 「旅行計画用」プロジェクト → 予算や好みを設定、複数の旅行で使い回し

---

<!-- _class: title -->

# 体験 ②

# 社会課題を解決する<br>WEB サービスを企画しよう

**制限時間：70 分**

---

## 体験 ② 社会課題を解決する WEB サービスを企画しよう

### 📋 ワークの流れ

**① 社会課題の洗い出し & 対象の選定（15 分）**

- どんな社会課題があるか、グループでブレインストーミング
- その中から 1 つ選定

**② ペルソナ作成（15 分）**

- サービスを使うユーザー像を具体的に設定
- 年齢、職業、困っていることなどを詳細に

---

## 体験 ② 社会課題を解決する WEB サービスを企画しよう

### 📋 ワークの流れ（続き）

**③ サービスコンセプトの深掘り（30 分）**

- コンセプトを具体化
- 目玉となる機能を考える
- どう課題を解決するのか
- 魅力的なサービスを自由に企画

**④ 企画書（Markdown 形式）にまとめる（10 分）**

- サービスコンセプト
- ペルソナ
- 目玉機能
- その他アピールポイント

---

## 発表 📢

### 各グループの企画を共有

- サービスコンセプト
- どんな課題をどう解決するか
- 目玉機能

---

<!-- _class: title -->

# 座学 ②

# セキュリティとハルシネーション

---

## セキュリティ 🔒

### ⚠️ AI は外部サービスであることを強く意識

**チャットすべきでない情報**

- 個人情報（氏名、住所、電話番号、メールアドレス）
- 機密情報（社内の戦略、未公開の情報）
- 認証情報（パスワード、API キー、トークン）
- 顧客情報（取引先の情報、契約内容）
- ソースコード（企業の独自実装、アルゴリズム）

---

## セキュリティ 🔒

<div class="warning" style="font-size: 1.1rem; padding: 1rem 1.2rem;">
⚠️ <strong>黎明期で組織の取り組みが追いついていないからこそ、各個人のリテラシーが重要</strong>

- ルールが整備されていない今だからこそ、一人ひとりの判断が問われる
- 「みんなやってるから大丈夫」ではなく、自分で考えて行動する
- 情報漏洩は取り返しがつかない
- 迷ったら入力しない、上司や情報セキュリティ担当者に相談する
</div>

---

## ハルシネーション 🎭

### AI は仕組み上、必ずウソをつく

**ハルシネーションとは**

- AI が事実でない情報を、もっともらしく回答すること
- 「幻覚」という意味

### なぜ起こる？

**AI の本質は「補完機」**

- 次に来る確率の高い単語を選んでいるだけ
- 本質的には **「ガチャ」**
- 正しいかどうかを判断しているわけではない

---

## ハルシネーション 🎭

### 💡 重要な心構え

<div class="warning" style="font-size: 1.1rem; padding: 1rem 1.2rem;">
⚠️ <strong>出力を利用し人を巻き込む場合は、必ず内容に責任を！</strong>

- AI の出力をそのまま信用しない
- 特に事実確認が必要な情報は、必ず裏を取る
- 他の人に共有する前に、自分でチェックする
- 「AI が言っていた」は言い訳にならない
</div>

**AI は強力な道具だが、完璧ではない**

- 最終的な責任は人間が持つ
- AI を賢く使いこなす姿勢が大切

---

## その他生成 AI の紹介

<div class="service-grid">

<div class="service-item">

![Gemini](images/gemini.png)

### Gemini

Google 関連サービスと連携可

</div>

<div class="service-item">

![Claude](images/claude.png)

### Claude

長文処理が得意

</div>

<div class="service-item">

![Grok](images/grok.png)

### Grok

X の投稿をリアルタイム取得<br>トレンド把握に最適

</div>

<div class="service-item">

![Copilot](images/copilot.png)

### Copilot

VSCode & <br>GitHub Copilot 連携<br>（情報系学生向け）

</div>

<div class="service-item">

![Cursor](images/cursor.png)

### Cursor

AI 協業型エディタ<br>(情報系学生向け)

</div>

<div class="service-item">

![NotebookLM](images/notebooklm.png)

### NotebookLM

資料丸ごと AI に学習させる<br>全学生、活用すべし！！

</div>

</div>

---

<!-- _class: title -->

# ご清聴ありがとうございました

**後ほど送付するアンケートへの**
**ご協力お願いします** 📝
