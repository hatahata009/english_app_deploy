# 生成AI英会話アプリ

OpenAIのAPIを活用した、実践的な英語学習Webアプリケーションです。
「日常英会話」「シャドーイング」「ディクテーション」の3つのモードを搭載し、ユーザーのレベル（初級・中級・上級）に合わせてAIが対話相手やコーチになります。

## ✨ 特徴

* **3つの学習モード**:
    1. **日常英会話**: AIと音声でフリートークを行います。会話の文脈を記憶し、自然なやり取りが可能です。
    2. **シャドーイング**: AIが生成した英文を聞き取り、復唱（録音）します。発音や正確さをAIが評価します。
    3. **ディクテーション**: AIが読み上げた音声をチャット欄に入力します。綴りや文法の正確さをAIが採点します。
* **レベル調整機能**: 初級・中級・上級を選択でき、レベルに応じた語彙や難易度で出題・会話が行われます。
* **再生速度調整**: リスニングの難易度に合わせて、音声の再生速度（0.6倍〜2.0倍）を変更可能です。
* **フィードバック機能**: シャドーイングやディクテーションの結果に対し、AIが具体的な改善点と学習アドバイスを提供します。

## 🛠 使用技術

* **Frontend**: Streamlit
* **LLM**: OpenAI (GPT-4o-mini)
* **Speech-to-Text**: OpenAI Whisper
* **Text-to-Speech**: OpenAI TTS (tts-1)
* **Framework**: LangChain
* **Audio Processing**: Pydub, PyAudio

## 🚀 セットアップ手順

ローカル環境で実行するための手順です。

### 1. 前提条件
* Python 3.10以上
* OpenAI APIキーの取得
* **FFmpegのインストール**
    * 本アプリは音声処理に `pydub` を使用しており、システムに FFmpeg がインストールされている必要があります。
    * **Mac**: `brew install ffmpeg`
    * **Windows**: [公式サイト](https://ffmpeg.org/download.html)からダウンロードし、PATHを通してください。

### 2. リポジトリのクローン
```bash
git clone [https://github.com/あなたのユーザー名/english_app_deploy.git](https://github.com/あなたのユーザー名/english_app_deploy.git)
cd english_app_deploy

```

### 3. 依存関係のインストール

```bash
pip install -r requirements.txt

```

### 4. 環境変数の設定

ルートディレクトリに `.env` ファイルを作成し、OpenAIのAPIキーを設定してください。

```env
OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

```

### 5. アプリケーションの起動

```bash
streamlit run main.py

```

ブラウザが自動的に起動し、アプリが表示されます。

## 📖 使い方

1. **設定**: 画面上部で「再生速度」「モード」「英語レベル」を選択し、「開始」ボタンを押します。
2. **日常英会話モード**:
* マイクに向かって話しかけると、AIが音声で応答します。


3. **シャドーイングモード**:
* 問題文が再生されるので、続いて発話（録音）してください。AIが再現度を評価します。


4. **ディクテーションモード**:
* 問題文が再生されるので、聞き取った内容をチャット欄に入力してください。AIが正誤判定を行います。



## 📂 ディレクトリ構成

```text
english_app_deploy/
├── audio/
│   ├── input/       # ユーザーの音声入力一時保存先
│   └── output/      # AIの音声出力一時保存先
├── images/          # アイコン画像など
├── functions.py     # 音声処理、Chain作成などの関数群
├── constants.py     # 定数、プロンプト定義
├── main.py          # アプリケーションのエントリーポイント
├── requirements.txt # 依存ライブラリ一覧
└── README.md        # ドキュメント

```

## ⚠️ 注意事項

* 本アプリはOpenAIのAPIを使用するため、実行にはAPI利用料が発生します。
* 音声入出力を行うため、マイクとスピーカーが有効な環境で実行してください。

## 👤 著者

Satoshi Hatanaka

```

```
