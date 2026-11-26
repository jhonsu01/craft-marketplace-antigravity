<p align="center"><img src="plugins/designcraft/assets/logo.png" width="96" alt="Craft Suite for Antigravity"></p>

<h1 align="center">Google Antigravity 版 Craft 插件套件</h1>

<p align="center">
  <a href="README.md">English</a> · <a href="README.es.md">Español</a> · <a href="README.pt-BR.md">Português</a> · <a href="README.fr.md">Français</a> · <a href="README.de.md">Deutsch</a> · <a href="README.ru.md">Русский</a> · <b>简体中文</b> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a>
</p>

<p align="center">面向 Google Antigravity 的原生 Craft 插件市场：连接你电脑上安装的 11 款开源 Craft 创作与办公应用（Windows、macOS、Linux）。</p>

---

## 插件列表（11 个原生插件包）

每个插件均内置 **1 个技能**（`/<plugin>`）、**1 条常驻规则**（`rules/AGENTS.md`）、**3 个启动提示词卡片** 和 **1 个本地 MCP 服务器**（`${PLUGIN_ROOT}/dist/bundle.cjs`），完全本地无头运行，不上传任何文件。

| 插件与斜杠命令 | 功能 | 依赖环境 |
| --- | --- | --- |
| **DesignCraft** (`/designcraft`) | 专业排版、CSV 数据合并、InDesign IDML、印刷级 PDF/X-4、PNG、EPUB 与 HTML | [DesignCraft](https://github.com/storytold/designcraft) + Node.js ≥ 20 |
| **EffectCraft** (`/effectcraft`) | 动态图形、动画标题、视频视觉特效、模板；导出 MP4、ProRes、WebM、GIF、Lottie | [EffectCraft](https://github.com/storytold/effectcraft) + Node.js ≥ 20 |
| **LightCraft** (`/lightcraft`) | RAW 照片冲洗：自动色调、125 个滑块、预设、局部蒙版、HDR 与全景合成；JPEG、TIFF、WebP、AVIF、DNG | [LightCraft](https://github.com/storytold/lightcraft) + Node.js ≥ 20 |
| **PhotoCraft** (`/photocraft`) | 图层照片编辑：缩放、裁剪、Camera Raw、123 种滤镜、抠图去背景、文字排版；PSD、PNG、JPEG、WebP | [PhotoCraft](https://github.com/storytold/photocraft) + Node.js ≥ 20 |
| **VectorCraft** (`/vectorcraft`) | 矢量设计：图像描摹、形状/文字/图表排版、重新着色；SVG、PDF、AI、EPS、DXF、PNG | [VectorCraft](https://github.com/storytold/vectorcraft) + Node.js ≥ 20 |
| **PdfCraft** (`/pdfcraft`) | PDF 全能工具：合并、拆分、页面管理、OCR、表单、数字签名、涂黑脱敏、加密；转 Word、HTML、图片、PDF/A | [PdfCraft](https://github.com/storytold/pdfcraft) + Node.js ≥ 20 |
| **FilmCraft** (`/filmcraft`) | 视频剪辑：分割、修剪、131 种特效、Lumetri 调色、字幕、转场拼接；H.264、ProRes、GIF、FCPXML、OTIO | [FilmCraft](https://github.com/storytold/filmcraft) + Node.js ≥ 20 |
| **WordCraft** (`/wordcraft`) | 文字处理：结构化文档生成、查找替换、批注、修订追踪、邮件合并；DOCX、PDF、ODT、RTF、Markdown、LaTeX | [WordCraft](https://github.com/storytold/wordcraft) + Node.js ≥ 20 |
| **SoundCraft** (`/soundcraft`) | 数字音频工作站（DAW）：多轨音频与 MIDI 合成器/鼓机、30 款内置插件、总线、LUFS 响度测量、分轨导出；WAV、AIFF、FLAC | [SoundCraft](https://github.com/storytold/soundcraft) + Node.js ≥ 20 |
| **DeckCraft** (`/deckcraft`) | 演示文稿：多级项目符号、图片、图表、表格与演讲者备注、主题与切换动画；PowerPoint PPTX、PDF 讲义、PNG | [DeckCraft](https://github.com/storytold/deckcraft) + Node.js ≥ 20 |
| **GridCraft** (`/gridcraft`) | 电子表格：支持 515 个实时 Excel 公式的工作簿、表格、图表与数据透视表；XLSX、CSV、ODS、JSON、HTML、PDF | [GridCraft](https://github.com/storytold/gridcraft) + Node.js ≥ 20 |

## 在 Google Antigravity Harness 中安装

### 1. 单条命令直接从 GitHub 安装（`agy` CLI）

无需手动克隆仓库，直接通过 GitHub 子目录链接安装任意插件。安装后会自动同步至 **Antigravity CLI**、**Antigravity App**（*Customizations → Installed*）与 **Antigravity IDE**：

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

> 在 `agy` 交互式界面中，也可直接输入 `/plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/<插件名>`。

### 2. 一键批量安装全部 11 款 Craft 插件

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

### 3. Antigravity App 与 Antigravity IDE（全局或工作区）

- **全局安装（所有项目生效）**：`agy plugin install` 会将插件解压至 `~/.gemini/config/plugins/<名称>`（Windows 为 `%USERPROFILE%\.gemini\config\plugins\<名称>`），可在桌面端 **Customizations → Installed** 查看并使用启动提示词卡片。
- **工作区级安装（单项目/团队共享）**：将任意 `plugins/<名称>` 复制到项目根目录的 `.agents/plugins/<名称>`，或直接将本仓库作为工作区打开（已预置 `.agents/plugins.json`）。

## 环境要求与跨平台配置

- `PATH` 中已安装 **Node.js ≥ 20**。
- 安装对应的开源 [Storytold Craft 应用](https://github.com/storytold)：Windows（`.msi` 或便携 `.zip`）、macOS（`.dmg` 应用 **外加** 放入 `/usr/local/bin` 或 `/opt/homebrew/bin` 的 `<app>-cli` 压缩包）、Linux（包含 CLI 的 `.deb`、`.rpm` 或 `.tar.gz`）。
- **自定义路径（可选）**：若应用安装在非标准目录，请设置 `<APP>_DIR` 或 `<APP>_CLI`（例如 `DESIGNCRAFT_DIR`）系统环境变量。

## 管理、严格校验与更新

使用 `agy plugin` 命令查看、启用/禁用、校验或更新插件：

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
agy plugin validate --strict https://raw.githubusercontent.com/jhonsu01/craft-marketplace-antigravity/main/.agents/plugins/marketplace.json
```

## 其他宿主与插件市场

- **OpenAI Codex 与 DeepSeek Harness**：请访问姊妹仓库 [jhonsu01/craft-marketplace](https://github.com/jhonsu01/craft-marketplace)。
- **Claude Desktop 与 Sunsam Code（双击安装 `.mcpb`）**：

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

## 许可证

Apache-2.0。Craft 系列应用归原作者（[Storytold](https://github.com/storytold)）所有；本仓库插件为独立社区集成，与原作者无隶属或背书关系。
