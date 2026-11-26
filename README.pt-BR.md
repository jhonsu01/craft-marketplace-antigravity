<p align="center"><img src="plugins/designcraft/assets/logo.png" width="96" alt="Craft Suite for Antigravity"></p>

<h1 align="center">Suíte Craft para Google Antigravity</h1>

<p align="center">
  <a href="README.md">English</a> · <a href="README.es.md">Español</a> · <b>Português</b> · <a href="README.fr.md">Français</a> · <a href="README.de.md">Deutsch</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a>
</p>

<p align="center">Marketplace nativo de plugins do Google Antigravity para os 11 aplicativos abertos Craft instalados no seu computador (Windows, macOS, Linux).</p>

---

## Plugins (11 Pacotes Nativos)

Cada plugin inclui **1 Skill** (`/<plugin>`), **1 Regra Sempre Ativa** (`rules/AGENTS.md`), **3 Prompts Iniciais** e **1 Servidor MCP Local** (`${PLUGIN_ROOT}/dist/bundle.cjs`) rodando em modo headless sem enviar arquivos para a nuvem.

| Plugin e Comando | O que faz | Requer |
| --- | --- | --- |
| **DesignCraft** (`/designcraft`) | Diagramação, mala direta CSV, IDML do InDesign, PDF/X-4 para gráfica, PNG, EPUB e HTML | [DesignCraft](https://github.com/storytold/designcraft) + Node.js ≥ 20 |
| **EffectCraft** (`/effectcraft`) | Motion graphics, títulos animados, efeitos VFX em vídeo, modelos; MP4, ProRes, WebM, GIF, Lottie | [EffectCraft](https://github.com/storytold/effectcraft) + Node.js ≥ 20 |
| **LightCraft** (`/lightcraft`) | Revelação RAW: tom automático, 125 controles, predefinições, máscaras, HDR e panoramas; JPEG, TIFF, WebP, AVIF, DNG | [LightCraft](https://github.com/storytold/lightcraft) + Node.js ≥ 20 |
| **PhotoCraft** (`/photocraft`) | Edição de fotos em camadas: tamanho, recorte, Camera Raw, 123 filtros, remoção de fundo, texto; PSD, PNG, JPEG, WebP | [PhotoCraft](https://github.com/storytold/photocraft) + Node.js ≥ 20 |
| **VectorCraft** (`/vectorcraft`) | Arte vetorial: vetorização Image Trace, formas, texto e gráficos, recolorir; SVG, PDF, AI, EPS, DXF, PNG | [VectorCraft](https://github.com/storytold/vectorcraft) + Node.js ≥ 20 |
| **PdfCraft** (`/pdfcraft`) | PDF completo: juntar, dividir, páginas, OCR, formulários, assinaturas, tarjas, senhas; para Word, HTML, imagens, PDF/A | [PdfCraft](https://github.com/storytold/pdfcraft) + Node.js ≥ 20 |
| **FilmCraft** (`/filmcraft`) | Edição de vídeo: dividir, cortar, 131 efeitos, looks Lumetri, títulos, transições; H.264, ProRes, GIF, FCPXML, OTIO | [FilmCraft](https://github.com/storytold/filmcraft) + Node.js ≥ 20 |
| **WordCraft** (`/wordcraft`) | Processador de texto: documentos estruturados, localizar/substituir, comentários, controle de alterações, mala direta; DOCX, PDF, ODT, RTF, Markdown, LaTeX | [WordCraft](https://github.com/storytold/wordcraft) + Node.js ≥ 20 |
| **SoundCraft** (`/soundcraft`) | Estação de áudio (DAW): sessões multipista com áudio e synths/bateria MIDI, 30 plugins, buses, LUFS, stems; WAV, AIFF, FLAC | [SoundCraft](https://github.com/storytold/soundcraft) + Node.js ≥ 20 |
| **DeckCraft** (`/deckcraft`) | Apresentações: slides com tópicos, imagens, gráficos, tabelas e notas, temas e transições; PowerPoint PPTX, handouts PDF, PNG | [DeckCraft](https://github.com/storytold/deckcraft) + Node.js ≥ 20 |
| **GridCraft** (`/gridcraft`) | Planilhas: pastas com 515 fórmulas Excel vivas, tabelas, gráficos e tabelas dinâmicas; XLSX, CSV, ODS, JSON, HTML, PDF | [GridCraft](https://github.com/storytold/gridcraft) + Node.js ≥ 20 |

## Instalar no Google Antigravity Harness

### 1. Instalação Direta com Um Comando (`agy` CLI)

Instale qualquer plugin diretamente do GitHub sem clonar manualmente. Os plugins sincronizam automaticamente entre **Antigravity CLI**, **Antigravity App** (*Customizations → Installed*) e **Antigravity IDE**:

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

> Dentro do TUI interativo do `agy`, você também pode executar `/plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/<nome-do-plugin>`.

### 2. Instalar Toda a Suíte de 11 Plugins de Uma Vez

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

### 3. Antigravity App e Antigravity IDE (Global ou Workspace)

- **Instalação global**: `agy plugin install` salva cada pacote em `~/.gemini/config/plugins/<nome>` (`%USERPROFILE%\.gemini\config\plugins\<nome>` no Windows) e o ativa no painel **Customizations → Installed**.
- **Instalação no workspace**: Copie `plugins/<nome>` para `.agents/plugins/<nome>` na raiz do seu projeto, ou abra este repositório diretamente (pré-configurado com `.agents/plugins.json`).

## Pré-requisitos e Configuração Multiplataforma

- **Node.js ≥ 20** no `PATH`.
- **O aplicativo Craft correspondente** da [Storytold](https://github.com/storytold): Windows (`.msi`/`.zip`), macOS (`.dmg` + binário `<app>-cli` em `/usr/local/bin` ou `/opt/homebrew/bin`) ou Linux (`.deb`, `.rpm`, `.tar.gz`).
- **Pasta personalizada (opcional)**: Defina `<APP>_DIR` ou `<APP>_CLI` (ex.: `DESIGNCRAFT_DIR`) como variável de ambiente do sistema.

## Gerenciar, Validar e Atualizar

Use os comandos do `agy plugin` para listar, ativar/desativar, validar ou atualizar:

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

## Outros Programas e Marketplaces

- **OpenAI Codex e DeepSeek Harness**: Veja [jhonsu01/craft-marketplace](https://github.com/jhonsu01/craft-marketplace).
- **Claude Desktop e Sunsam Code (pacotes `.mcpb`)**:

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

## Licença

Apache-2.0. Os apps Craft pertencem aos seus autores ([Storytold](https://github.com/storytold)); estes plugins não são afiliados nem endossados por eles.
