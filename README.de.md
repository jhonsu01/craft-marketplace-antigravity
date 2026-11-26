<p align="center"><img src="plugins/designcraft/assets/logo.png" width="96" alt="Craft Suite for Antigravity"></p>

<h1 align="center">Craft Suite für Google Antigravity</h1>

<p align="center">
  <a href="README.md">English</a> · <a href="README.es.md">Español</a> · <a href="README.pt-BR.md">Português</a> · <a href="README.fr.md">Français</a> · <b>Deutsch</b> · <a href="README.ru.md">Русский</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a>
</p>

<p align="center">Nativer Google-Antigravity-Plugin-Marketplace für die 11 quelloffenen Craft-Anwendungen auf Ihrem Computer (Windows, macOS, Linux).</p>

---

## Plugins (11 Native Pakete)

Jedes Plugin bündelt **1 Skill** (`/<plugin>`), **1 Aktive Regel** (`rules/AGENTS.md`), **3 Starter-Prompts** und **1 Lokalen MCP-Server** (`${PLUGIN_ROOT}/dist/bundle.cjs`), der komplett lokal ohne Cloud-Upload arbeitet.

| Plugin & Befehl | Was es tut | Voraussetzung |
| --- | --- | --- |
| **DesignCraft** (`/designcraft`) | Seitenlayout, CSV-Datenzusammenführung, InDesign-IDML, druckfertiges PDF/X-4, PNG, EPUB und HTML | [DesignCraft](https://github.com/storytold/designcraft) + Node.js ≥ 20 |
| **EffectCraft** (`/effectcraft`) | Motion Graphics, animierte Titel, Video-VFX, Vorlagen; MP4, ProRes, WebM, GIF, Lottie | [EffectCraft](https://github.com/storytold/effectcraft) + Node.js ≥ 20 |
| **LightCraft** (`/lightcraft`) | RAW-Entwicklung: Auto-Tonwert, 125 Regler, Vorgaben, Masken, HDR und Panoramen; JPEG, TIFF, WebP, AVIF, DNG | [LightCraft](https://github.com/storytold/lightcraft) + Node.js ≥ 20 |
| **PhotoCraft** (`/photocraft`) | Bildbearbeitung mit Ebenen: Größe, Zuschnitt, Camera Raw, 123 Filter, Freistellen, Text; PSD, PNG, JPEG, WebP | [PhotoCraft](https://github.com/storytold/photocraft) + Node.js ≥ 20 |
| **VectorCraft** (`/vectorcraft`) | Vektorgrafik: Bildnachzeichner, Formen, Text und Diagramme, Umfärben; SVG, PDF, AI, EPS, DXF, PNG | [VectorCraft](https://github.com/storytold/vectorcraft) + Node.js ≥ 20 |
| **PdfCraft** (`/pdfcraft`) | PDF-Werkzeuge: Zusammenführen, Teilen, Seiten, OCR, Formulare, Signaturen, Schwärzen, Passwörter; nach Word, HTML, Bilder, PDF/A | [PdfCraft](https://github.com/storytold/pdfcraft) + Node.js ≥ 20 |
| **FilmCraft** (`/filmcraft`) | Videoschnitt: Teilen, Trimmen, 131 Effekte, Lumetri-Farblooks, Titel, Übergänge; H.264, ProRes, GIF, FCPXML, OTIO | [FilmCraft](https://github.com/storytold/filmcraft) + Node.js ≥ 20 |
| **WordCraft** (`/wordcraft`) | Textverarbeitung: Dokumente mit Überschriften, Tabellen und Bildern, Suchen/Ersetzen, Kommentare, Änderungsverfolgung, Serienbriefe; DOCX, PDF, ODT, RTF, Markdown, LaTeX | [WordCraft](https://github.com/storytold/wordcraft) + Node.js ≥ 20 |
| **SoundCraft** (`/soundcraft`) | Digital Audio Workstation: Mehrspur-Audio & MIDI-Synths/Drums, 30 Plugins, Busse, LUFS-Lautheit, Stems; WAV, AIFF, FLAC | [SoundCraft](https://github.com/storytold/soundcraft) + Node.js ≥ 20 |
| **DeckCraft** (`/deckcraft`) | Präsentationen: Folien mit Aufzählungen, Bildern, Diagrammen, Tabellen und Notizen, Designs, Übergänge; PowerPoint-PPTX, PDF-Handouts, PNG | [DeckCraft](https://github.com/storytold/deckcraft) + Node.js ≥ 20 |
| **GridCraft** (`/gridcraft`) | Tabellenkalkulation: Arbeitsmappen mit 515 Live-Formeln, Tabellen, Diagrammen und PivotTables; XLSX, CSV, ODS, JSON, HTML, PDF | [GridCraft](https://github.com/storytold/gridcraft) + Node.js ≥ 20 |

## In Google Antigravity Harness installieren

### 1. Direkte Ein-Befehl-Installation (`agy` CLI)

Installieren Sie jedes Plugin direkt von GitHub ohne manuelles Klonen. Installierte Plugins synchronisieren automatisch zwischen **Antigravity CLI**, **Antigravity App** (*Customizations → Installed*) und **Antigravity IDE**:

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

> In einer interaktiven `agy`-Sitzung können Sie auch `/plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/<plugin-name>` ausführen.

### 2. Alle 11 Plugins der Suite auf Einmal installieren

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

### 3. Antigravity App & Antigravity IDE (Global oder Workspace)

- **Global**: `agy plugin install` speichert jedes Plugin unter `~/.gemini/config/plugins/<name>` (`%USERPROFILE%\.gemini\config\plugins\<name>` unter Windows) und zeigt es unter **Customizations → Installed** an.
- **Workspace**: Kopieren Sie `plugins/<name>` nach `.agents/plugins/<name>` im Projektstamm oder öffnen Sie dieses Repository direkt als Workspace (`.agents/plugins.json`).

## Voraussetzungen & Plattform-Setup

- **Node.js ≥ 20** im `PATH`.
- **Die jeweilige quelloffene Craft-App** von [Storytold](https://github.com/storytold): Windows (`.msi`/`.zip`), macOS (`.dmg` + `<app>-cli` in `/usr/local/bin` oder `/opt/homebrew/bin`) oder Linux (`.deb`, `.rpm`, `.tar.gz`).
- **Eigener Installationspfad (optional)**: Setzen Sie `<APP>_DIR` oder `<APP>_CLI` (z. B. `DESIGNCRAFT_DIR`) als Systemumgebungsvariable.

## Verwalten, Validieren & Aktualisieren

Verwenden Sie `agy plugin`, um Plugins aufzulisten, umzuschalten, zu prüfen oder zu aktualisieren:

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

## Andere Programme & Marketplaces

- **OpenAI Codex & DeepSeek Harness**: Siehe [jhonsu01/craft-marketplace](https://github.com/jhonsu01/craft-marketplace).
- **Claude Desktop & Sunsam Code (`.mcpb`-Pakete)**:

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

## Lizenz

Apache-2.0. Die Craft-Apps gehören ihren Autoren ([Storytold](https://github.com/storytold)); diese Plugins sind weder mit ihnen verbunden noch von ihnen unterstützt.
