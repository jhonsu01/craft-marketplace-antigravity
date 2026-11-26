<p align="center"><img src="plugins/designcraft/assets/logo.png" width="96" alt="Craft Suite for Antigravity"></p>

<h1 align="center">Craft Suite for Google Antigravity</h1>

<p align="center">
  <b>English</b> · <a href="README.es.md">Español</a> · <a href="README.pt-BR.md">Português</a> · <a href="README.fr.md">Français</a> · <a href="README.de.md">Deutsch</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a>
</p>

<p align="center">Native Google Antigravity plugin marketplace for the 11 Craft creative & productivity apps installed on your computer (Windows, macOS, Linux).</p>

---

## Plugins (11 Native Bundles)

Every plugin bundles **1 Skill** (`/<plugin>`), **1 Always-On Rule** (`rules/AGENTS.md`), **3 Starter Prompt Chips**, and **1 Local MCP Server** (`${PLUGIN_ROOT}/dist/bundle.cjs`) running headless with zero cloud uploads.

| Plugin & Slash Skill | What it does | Needs |
| --- | --- | --- |
| **DesignCraft** (`/designcraft`) | Page layout, CSV data merge, InDesign IDML, print-ready PDF/X-4, PNG, EPUB, and HTML | [DesignCraft](https://github.com/storytold/designcraft) + Node.js ≥ 20 |
| **EffectCraft** (`/effectcraft`) | Motion graphics, animated titles, video VFX, templates; MP4, ProRes, WebM, GIF, Lottie | [EffectCraft](https://github.com/storytold/effectcraft) + Node.js ≥ 20 |
| **LightCraft** (`/lightcraft`) | RAW photo development: auto tone, 125 sliders, presets, masks, HDR & panoramas; JPEG, TIFF, WebP, AVIF, DNG | [LightCraft](https://github.com/storytold/lightcraft) + Node.js ≥ 20 |
| **PhotoCraft** (`/photocraft`) | Photo & layer editing: resize, crop, Camera Raw, 123 filters, background removal, text; PSD, PNG, JPEG, WebP | [PhotoCraft](https://github.com/storytold/photocraft) + Node.js ≥ 20 |
| **VectorCraft** (`/vectorcraft`) | Vector art: Image Trace, shapes, styled text & charts, recolor; SVG, PDF, AI, EPS, DXF, PNG | [VectorCraft](https://github.com/storytold/vectorcraft) + Node.js ≥ 20 |
| **PdfCraft** (`/pdfcraft`) | PDF toolkit: merge, split, pages, OCR, forms, signatures, redaction, encryption; to Word, HTML, images, PDF/A | [PdfCraft](https://github.com/storytold/pdfcraft) + Node.js ≥ 20 |
| **FilmCraft** (`/filmcraft`) | Video editing: split, trim, 131 effects, Lumetri color looks, titles, transitions; H.264, ProRes, GIF, FCPXML, OTIO | [FilmCraft](https://github.com/storytold/filmcraft) + Node.js ≥ 20 |
| **WordCraft** (`/wordcraft`) | Word processing: structured docs, find/replace, comments, tracked changes, mail merge; DOCX, PDF, ODT, RTF, Markdown, LaTeX | [WordCraft](https://github.com/storytold/wordcraft) + Node.js ≥ 20 |
| **SoundCraft** (`/soundcraft`) | Digital Audio Workstation: multitrack audio & MIDI synths/drums, 30 plugins, busses, LUFS loudness, stems; WAV, AIFF, FLAC | [SoundCraft](https://github.com/storytold/soundcraft) + Node.js ≥ 20 |
| **DeckCraft** (`/deckcraft`) | Presentations: slides with bullets, images, charts, tables & speaker notes, themes, transitions; PowerPoint PPTX, PDF handouts, PNG | [DeckCraft](https://github.com/storytold/deckcraft) + Node.js ≥ 20 |
| **GridCraft** (`/gridcraft`) | Spreadsheets: multi-sheet workbooks with 515 live Excel formulas, tables, charts & PivotTables; XLSX, CSV, ODS, JSON, HTML, PDF | [GridCraft](https://github.com/storytold/gridcraft) + Node.js ≥ 20 |

## Install in Google Antigravity Harness

### 1. Direct One-Command Install (`agy` CLI)

Install any individual plugin directly from GitHub — no manual cloning required. Installed plugins automatically sync across **Antigravity CLI**, **Antigravity App** (*Customizations → Installed*), and **Antigravity IDE**:

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

> Inside an interactive `agy` session, you can also run `/plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/<plugin-name>`.

### 2. Install the Entire 11-Plugin Suite at Once

**macOS / Linux (Bash / Zsh):**

```bash
git clone https://github.com/jhonsu01/craft-marketplace-antigravity.git
for p in craft-marketplace-antigravity/plugins/*; do agy plugin install "$p"; done
```

**Windows (PowerShell):**

```powershell
git clone https://github.com/jhonsu01/craft-marketplace-antigravity.git
Get-ChildItem .\craft-marketplace-antigravity\plugins -Directory | ForEach-Object { agy plugin install $_.FullName }
```

### 3. Antigravity App & Antigravity IDE (Global or Workspace)

- **Global install (all projects)**: `agy plugin install` unpacks each plugin into `~/.gemini/config/plugins/<name>` (`%USERPROFILE%\.gemini\config\plugins\<name>` on Windows). Open **Customizations → Installed** in the Antigravity App to see starter prompt chips, skills, rules, and MCP tools.
- **Workspace-only install (single repo/team)**: Copy any `plugins/<name>` folder into `.agents/plugins/<name>` at the root of your project, or open this repository directly as a workspace (preconfigured via `.agents/plugins.json`).

## Prerequisites & Cross-Platform Setup

- **Node.js ≥ 20** on `PATH` (used by Antigravity to launch each bundled `dist/bundle.cjs` MCP server).
- **The matching open-source Craft desktop/CLI app** from [Storytold](https://github.com/storytold):
  - **Windows**: Install the `.msi` or portable `.zip` (`C:\Program Files\<App>`, `%LOCALAPPDATA%\Programs\<App>`, or `PATH` are auto-detected).
  - **macOS**: Install the `.dmg` app **plus** the separate `<app>-cli-*-macos-universal.zip` binary into `/usr/local/bin` or `/opt/homebrew/bin`.
  - **Linux**: Install the `.deb`, `.rpm`, or `.tar.gz` package (which includes `<app>-cli`; AppImage/Flatpak only bundle the GUI).
- **Custom install path (optional)**: Set `<APP>_DIR` or `<APP>_CLI` (for example `DESIGNCRAFT_DIR`, `SOUNDCRAFT_DIR`, `LIGHTCRAFT_DIR`) as a system environment variable if an app lives outside standard folders.

## Manage, Validate & Update

Use standard `agy plugin` commands to inspect, toggle, validate, or update any Craft plugin:

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

## Other AI Hosts & Marketplaces

- **OpenAI Codex & DeepSeek Harness**: Use the sibling repository [jhonsu01/craft-marketplace](https://github.com/jhonsu01/craft-marketplace).
- **Claude Desktop & Sunsam Code (`.mcpb` one-click bundles)**:

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

## License

Apache-2.0. The Craft applications belong to their authors ([Storytold](https://github.com/storytold)); these plugins are independent community integrations and are not affiliated with or endorsed by them.
