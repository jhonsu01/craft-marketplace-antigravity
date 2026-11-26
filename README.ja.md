<p align="center"><img src="plugins/designcraft/assets/logo.png" width="96" alt="Craft Suite for Antigravity"></p>

<h1 align="center">Craft Suite for Google Antigravity</h1>

<p align="center">
  <a href="README.md">English</a> · <a href="README.es.md">Español</a> · <a href="README.pt-BR.md">Português</a> · <a href="README.fr.md">Français</a> · <a href="README.de.md">Deutsch</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh-CN.md">简体中文</a> · <b>日本語</b> · <a href="README.ko.md">한국어</a>
</p>

<p align="center">お使いのコンピューター（Windows、macOS、Linux）にインストールされた 11 個のオープンソース Craft アプリを Google Antigravity につなぐネイティブプラグインマーケットプレイスです。</p>

---

## 収録プラグイン（全 11 種）

各プラグインには **1 つのスキル**（`/<plugin>`）、**1 つの常時有効ルール**（`rules/AGENTS.md`）、**3 つのスタータープロンプト**、およびクラウド送信なしでローカル動作する **1 つの MCP サーバー**（`${PLUGIN_ROOT}/dist/bundle.cjs`）が含まれています。

| プラグイン / スキル | 機能 | 必要なもの |
| --- | --- | --- |
| **DesignCraft** (`/designcraft`) | ページレイアウト、CSV データ結合、InDesign IDML、印刷用 PDF/X-4、PNG、EPUB、HTML | [DesignCraft](https://github.com/storytold/designcraft) + Node.js ≥ 20 |
| **EffectCraft** (`/effectcraft`) | モーショングラフィックス、アニメーションタイトル、動画 VFX、テンプレート；MP4、ProRes、WebM、GIF、Lottie | [EffectCraft](https://github.com/storytold/effectcraft) + Node.js ≥ 20 |
| **LightCraft** (`/lightcraft`) | RAW 現像：自動トーン、125 スライダー、プリセット、マスク、HDR・パノラマ合成；JPEG、TIFF、WebP、AVIF、DNG | [LightCraft](https://github.com/storytold/lightcraft) + Node.js ≥ 20 |
| **PhotoCraft** (`/photocraft`) | レイヤー写真編集：リサイズ、切り抜き、Camera Raw、123 フィルター、背景除去、テキスト；PSD、PNG、JPEG、WebP | [PhotoCraft](https://github.com/storytold/photocraft) + Node.js ≥ 20 |
| **VectorCraft** (`/vectorcraft`) | ベクターデザイン：画像トレース、図形・テキスト・グラフ作成、再配色；SVG、PDF、AI、EPS、DXF、PNG | [VectorCraft](https://github.com/storytold/vectorcraft) + Node.js ≥ 20 |
| **PdfCraft** (`/pdfcraft`) | PDF ツール：結合、分割、ページ編集、OCR、フォーム、署名、墨消し、暗号化；Word、HTML、画像、PDF/A 変換 | [PdfCraft](https://github.com/storytold/pdfcraft) + Node.js ≥ 20 |
| **FilmCraft** (`/filmcraft`) | 動画編集：分割、トリム、131 エフェクト、Lumetri ルック、タイトル、トランジション；H.264、ProRes、GIF、FCPXML、OTIO | [FilmCraft](https://github.com/storytold/filmcraft) + Node.js ≥ 20 |
| **WordCraft** (`/wordcraft`) | ワープロ：見出し・表・画像からの文書作成、検索/置換、コメント、変更履歴、差し込み印刷；DOCX、PDF、ODT、RTF、Markdown、LaTeX | [WordCraft](https://github.com/storytold/wordcraft) + Node.js ≥ 20 |
| **SoundCraft** (`/soundcraft`) | DAW（音楽・音声制作）：マルチトラック音声＆MIDI シンセ/ドラム、30 プラグイン、バス、LUFS 測定、ステム書き出し；WAV、AIFF、FLAC | [SoundCraft](https://github.com/storytold/soundcraft) + Node.js ≥ 20 |
| **DeckCraft** (`/deckcraft`) | プレゼンテーション：箇条書き・画像・グラフ・表・ノート付きスライド、テーマ、切り替え；PowerPoint PPTX、配布資料 PDF、PNG | [DeckCraft](https://github.com/storytold/deckcraft) + Node.js ≥ 20 |
| **GridCraft** (`/gridcraft`) | スプレッドシート：515 個の Excel 数式、テーブル、グラフ、ピボットテーブル対応ブック；XLSX、CSV、ODS、JSON、HTML、PDF | [GridCraft](https://github.com/storytold/gridcraft) + Node.js ≥ 20 |

## Google Antigravity Harness へのインストール

### 1. GitHub から 1 コマンドで直接インストール（`agy` CLI）

手動クローン不要で GitHub から直接インストールできます。インストールしたプラグインは **Antigravity CLI**、**Antigravity App**（*Customizations → Installed*）、**Antigravity IDE** 間で自動同期されます：

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/designcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/effectcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/lightcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/photocraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/vectorcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/pdfcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/filmcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/wordcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/soundcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/deckcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/gridcraft
```

> 対話型 `agy` セッション内では `/plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/<プラグイン名>` も実行できます。

### 2. 全 11 プラグインを一括インストール

**macOS / Linux（Bash / Zsh）：**

```bash
git clone https://github.com/jhonsu01/craft-marketplace-antigravity.git
for p in craft-marketplace-antigravity/plugins/*; do agy plugin install "$p"; done
```

**Windows（PowerShell）：**

```powershell
git clone https://github.com/jhonsu01/craft-marketplace-antigravity.git
Get-ChildItem .\craft-marketplace-antigravity\plugins -Directory | ForEach-Object { agy plugin install $_.FullName }
```

### 3. Antigravity App & Antigravity IDE（グローバル／ワークスペース）

- **グローバルインストール**：`agy plugin install` は `~/.gemini/config/plugins/<名前>`（Windows は `%USERPROFILE%\.gemini\config\plugins\<名前>`）に配置され、アプリの **Customizations → Installed** に表示されます。
- **ワークスペース単位**：`plugins/<名前>` をプロジェクト直下の `.agents/plugins/<名前>` にコピーするか、このリポジトリ自体をワークスペースとして開きます（`.agents/plugins.json` 設定済み）。

## 前提条件とマルチプラットフォーム設定

- `PATH` 上の **Node.js ≥ 20**。
- [Storytold](https://github.com/storytold) の各 **Craft アプリ**：Windows（`.msi`/`.zip`）、macOS（`.dmg` 本体 **および** `/usr/local/bin` または `/opt/homebrew/bin` に配置した `<app>-cli`）、Linux（`.deb`、`.rpm`、`.tar.gz`）。
- **カスタムパス（任意）**：標準以外の場所にインストールした場合は `<APP>_DIR` または `<APP>_CLI`（例：`DESIGNCRAFT_DIR`）を環境変数に設定してください。

## 管理・検証・アップデート

`agy plugin` コマンドで一覧表示、有効化／無効化、検証、更新を行えます：

```bash
# List installed plugins & bundled components
agy plugin list

# Enable / disable / uninstall a plugin
agy plugin disable designcraft
agy plugin enable designcraft
agy plugin uninstall designcraft

# Update a plugin to the latest version from GitHub
agy plugin uninstall designcraft && agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/designcraft

# Validate every plugin in the marketplace catalog
agy plugin validate https://github.com/jhonsu01/craft-marketplace-antigravity/blob/main/.agents/plugins/marketplace.json
```

## その他のアプリ・マーケットプレイス

- **OpenAI Codex & DeepSeek Harness**：姉妹リポジトリ [jhonsu01/craft-marketplace](https://github.com/jhonsu01/craft-marketplace) をご覧ください。
- **Claude Desktop & Sunsam Code（`.mcpb` パッケージ）**：

- **DesignCraft**: [designcraft-mcp-server.mcpb](https://github.com/jhonsu01/designcraft-mcp-server/releases/latest/download/designcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/designcraft-mcp-server)
- **EffectCraft**: [effectcraft-mcp-server.mcpb](https://github.com/jhonsu01/effectcraft-mcp-server/releases/latest/download/effectcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/effectcraft-mcp-server)
- **LightCraft**: [lightcraft-mcp-server.mcpb](https://github.com/jhonsu01/lightcraft-mcp-server/releases/latest/download/lightcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/lightcraft-mcp-server)
- **PhotoCraft**: [photocraft-mcp-server.mcpb](https://github.com/jhonsu01/photocraft-mcp-server/releases/latest/download/photocraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/photocraft-mcp-server)
- **VectorCraft**: [vectorcraft-mcp-server.mcpb](https://github.com/jhonsu01/vectorcraft-mcp-server/releases/latest/download/vectorcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/vectorcraft-mcp-server)
- **PdfCraft**: [pdfcraft-mcp-server.mcpb](https://github.com/jhonsu01/pdfcraft-mcp-server/releases/latest/download/pdfcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/pdfcraft-mcp-server)
- **FilmCraft**: [filmcraft-mcp-server.mcpb](https://github.com/jhonsu01/filmcraft-mcp-server/releases/latest/download/filmcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/filmcraft-mcp-server)
- **WordCraft**: [wordcraft-mcp-server.mcpb](https://github.com/jhonsu01/wordcraft-mcp-server/releases/latest/download/wordcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/wordcraft-mcp-server)
- **SoundCraft**: [soundcraft-mcp-server.mcpb](https://github.com/jhonsu01/soundcraft-mcp-server/releases/latest/download/soundcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/soundcraft-mcp-server)
- **DeckCraft**: [deckcraft-mcp-server.mcpb](https://github.com/jhonsu01/deckcraft-mcp-server/releases/latest/download/deckcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/deckcraft-mcp-server)
- **GridCraft**: [gridcraft-mcp-server.mcpb](https://github.com/jhonsu01/gridcraft-mcp-server/releases/latest/download/gridcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/gridcraft-mcp-server)

## ライセンス

Apache-2.0。Craft アプリの権利は作者（[Storytold](https://github.com/storytold)）に帰属します。本プラグイン群は作者とは無関係であり、承認も受けていません。
