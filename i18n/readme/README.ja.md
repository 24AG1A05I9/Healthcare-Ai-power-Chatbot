# 🚀 **OpenHealth**

<div align="center">

**AIヘルスアシスタント | あなたのデータを活用**

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Web-blue?style=for-the-badge" alt="Platform">
  <img src="https://img.shields.io/badge/Language-TypeScript-blue?style=for-the-badge" alt="Language">
  <img src="https://img.shields.io/badge/Framework-Next.js-black?style=for-the-badge" alt="Framework">
</p>

> **📢 ウェブ版が利用可能になりました！**  
> より使いやすくするために、2つのカスタマイズされたオプションをご用意しました：  
> **[クリニック](https://qna.open-health.me/)** - 迅速で簡単な健康相談  
> **[フルプラットフォーム](https://www.open-health.me/)** - 包括的な健康管理のための高度なツール

### 🌟 概要

OpenHealthは、**あなたの健康データを管理**するお手伝いをします。AIとあなたの個人健康情報を活用し、
OpenHealthはプライベートなアシスタントを提供し、健康をより良く理解し管理することを支援します。最大限のプライバシー保護のため、完全にローカルで実行することができます。

### ✨ プロジェクトの特徴

- 📊 **集中化された健康データ入力：** すべての健康データを一箇所で簡単に統合
- 🛠️ **スマート解析：** 健康データを自動的に解析し、構造化されたデータファイルを生成
- 🤝 **文脈に基づく会話：** GPT駆動のAIとのパーソナライズされた対話のために構造化データを活用

### 📥 サポートされているデータソースと言語モデル

| **追加可能なデータソース** | **サポートされている言語モデル** |
|--------------------------|--------------------------------|
| 血液検査結果              | LLaMA,DeepSeek-V3               |
| 健康診断データ            | GPT,Claude,Gemini               |
| 個人の身体情報            |                                |
| 家族歴                    |                                |
| 症状                      |                                |

### 🤔 OpenHealthを作った理由

- 💡 **あなたの健康はあなたの責任です。**
- ✅ 真の健康管理は**あなたのデータ** + **インテリジェンス**を組み合わせ、洞察を実行可能な計画に変換します。
- 🧠 AIは長期的な健康管理を効果的に導き、支援する偏りのないツールとして機能します。

### 🗺️ プロジェクト図

```plaintext
健康データ入力 --> データ解析モジュール --> 構造化データファイル --> GPT統合
```

> **注意:** データ解析機能は現在、別のPythonサーバーで実装されており、将来的にTypeScriptへの移行を予定しています。

## はじめに

## ⚙️ OpenHealthの実行方法

1. **リポジトリのクローン:**
   ```bash
   git clone https://github.com/OpenHealthForAll/open-health.git
   cd open-health
   ```

2. **セットアップと実行:**
   ```bash
   # 環境設定ファイルをコピー
   cp .env.example .env

   # Docker Composeでアプリケーションを起動
   docker compose --env-file .env up
   ```

   既存ユーザーの場合:
   ```bash
   # .envファイルのENCRYPTION_KEYを生成:
   # 以下のコマンドを実行し、出力を.envのENCRYPTION_KEYに追加してください
   echo $(head -c 32 /dev/urandom | base64)

   # イメージを再ビルドして起動
   docker compose --env-file .env up --build
   ```

3. **OpenHealthへのアクセス:**
   ブラウザで `http://localhost:3000` にアクセスしてOpenHealthを開始します。

> **注意:** システムはパースとLLMの2つの主要コンポーネントで構成されています。パースについては、doclingを使用して完全なローカル実行が可能で、LLMコンポーネントはOllamaを使用して完全にローカルで実行できます。

> **注意:** DockerでOllamaを使用する場合、Ollama APIエンドポイントを次のように設定してください: `http://docker.for.mac.localhost:11434`（Macの場合）または `http://host.docker.internal:11434`（Windowsの場合）

### 🌐 コミュニティとサポート

<div align="center">

### 💫 あなたの体験を共有し、最新情報を入手
[![AIDoctor Subreddit](https://img.shields.io/badge/r/AIDoctor-FF4500?style=for-the-badge&logo=reddit&logoColor=white)](https://www.reddit.com/r/AIDoctor/)
[![Discord](https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/B9K654g4wf)

### 🤝 チームと話す
[![Calendly](https://img.shields.io/badge/ミーティングを予約-00A2FF?style=for-the-badge&logo=calendar&logoColor=white)](https://calendly.com/open-health/30min)
[![Email](https://img.shields.io/badge/メールを送信-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:sj@open-health.me)

</div> 