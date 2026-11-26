<p align="center"><img src="plugins/designcraft/assets/logo.png" width="96" alt="Craft Suite for Antigravity"></p>

<h1 align="center">Suite Craft para Google Antigravity</h1>

<p align="center">
  <a href="README.md">English</a> · <b>Español</b> · <a href="README.pt-BR.md">Português</a> · <a href="README.fr.md">Français</a> · <a href="README.de.md">Deutsch</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a>
</p>

<p align="center">Marketplace nativo de plugins de Google Antigravity para las 11 aplicaciones abiertas Craft instaladas en tu equipo (Windows, macOS, Linux).</p>

---

## Plugins Incluidos (11 Paquetes Nativos)

Cada plugin empaqueta **1 Habilidad** (`/<plugin>`), **1 Regla Activa** (`rules/AGENTS.md`), **3 Prompts Sugeridos** y **1 Servidor MCP Local** (`${PLUGIN_ROOT}/dist/bundle.cjs`) que opera en modo headless sin subir tus archivos a la nube.

| Plugin y Comando | Qué hace | Necesita |
| --- | --- | --- |
| **DesignCraft** (`/designcraft`) | Maquetación editorial, combinación de datos CSV, IDML de InDesign, PDF/X-4 para imprenta, PNG, EPUB y HTML | [DesignCraft](https://github.com/storytold/designcraft) + Node.js ≥ 20 |
| **EffectCraft** (`/effectcraft`) | Motion graphics, títulos animados, efectos VFX en video, plantillas; MP4, ProRes, WebM, GIF, Lottie | [EffectCraft](https://github.com/storytold/effectcraft) + Node.js ≥ 20 |
| **LightCraft** (`/lightcraft`) | Revelado RAW: tono automático, 125 controles, presets, máscaras locales, HDR y panorámicas; JPEG, TIFF, WebP, AVIF, DNG | [LightCraft](https://github.com/storytold/lightcraft) + Node.js ≥ 20 |
| **PhotoCraft** (`/photocraft`) | Edición de fotos por capas: tamaño, recorte, Camera Raw, 123 filtros, quitar fondo, texto; PSD, PNG, JPEG, WebP | [PhotoCraft](https://github.com/storytold/photocraft) + Node.js ≥ 20 |
| **VectorCraft** (`/vectorcraft`) | Arte vectorial: vectorización Image Trace, formas, texto y gráficos, recolorear; SVG, PDF, AI, EPS, DXF, PNG | [VectorCraft](https://github.com/storytold/vectorcraft) + Node.js ≥ 20 |
| **PdfCraft** (`/pdfcraft`) | Suite PDF: unir, dividir, páginas, OCR, formularios, firmas digitales, censura, cifrado; a Word, HTML, imágenes, PDF/A | [PdfCraft](https://github.com/storytold/pdfcraft) + Node.js ≥ 20 |
| **FilmCraft** (`/filmcraft`) | Edición de video: dividir, recortar, 131 efectos, looks Lumetri, títulos, transiciones; H.264, ProRes, GIF, FCPXML, OTIO | [FilmCraft](https://github.com/storytold/filmcraft) + Node.js ≥ 20 |
| **WordCraft** (`/wordcraft`) | Procesador de textos: documentos con títulos, tablas e imágenes, buscar/reemplazar, comentarios, control de cambios, mail merge; DOCX, PDF, ODT, RTF, Markdown, LaTeX | [WordCraft](https://github.com/storytold/wordcraft) + Node.js ≥ 20 |
| **SoundCraft** (`/soundcraft`) | Estación de audio (DAW): sesiones multipista con audio y sintetizadores/batería MIDI, 30 plugins, buses, sonoridad LUFS, stems; WAV, AIFF, FLAC | [SoundCraft](https://github.com/storytold/soundcraft) + Node.js ≥ 20 |
| **DeckCraft** (`/deckcraft`) | Presentaciones: diapositivas con viñetas, imágenes, gráficos, tablas y notas del orador, temas y transiciones; PowerPoint PPTX, handouts PDF, PNG | [DeckCraft](https://github.com/storytold/deckcraft) + Node.js ≥ 20 |
| **GridCraft** (`/gridcraft`) | Hojas de cálculo: libros con 515 fórmulas Excel en vivo, tablas, formato condicional, gráficos y tablas dinámicas; XLSX, CSV, ODS, JSON, HTML, PDF | [GridCraft](https://github.com/storytold/gridcraft) + Node.js ≥ 20 |

## Instalar en Google Antigravity Harness

### 1. Instalación Directa en un Comando (`agy` CLI)

Instala cualquier plugin directamente desde GitHub sin clonar manualmente. Los plugins instalados se sincronizan automáticamente entre **Antigravity CLI**, **Antigravity App** (*Customizations → Installed*) y **Antigravity IDE**:

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

> Dentro de una sesión interactiva de `agy`, también puedes ejecutar `/plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/<nombre-plugin>`.

### 2. Instalar la Suite Completa de 11 Plugins de una Sola Vez

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

### 3. Antigravity App y Antigravity IDE (Global o por Proyecto)

- **Instalación global (todos tus proyectos)**: `agy plugin install` instala cada paquete en `~/.gemini/config/plugins/<nombre>` (`%USERPROFILE%\.gemini\config\plugins\<nombre>` en Windows). Abre **Customizations → Installed** en Antigravity App para ver las tarjetas, prompts iniciales, skills, reglas y herramientas MCP.
- **Instalación por workspace (equipo/proyecto)**: Copia cualquier carpeta `plugins/<nombre>` dentro de `.agents/plugins/<nombre>` en la raíz de tu repositorio, o abre este repositorio directamente como workspace (preconfigurado mediante `.agents/plugins.json`).

## Requisitos y Configuración Multiplataforma

- **Node.js ≥ 20** en el `PATH` (Antigravity lo utiliza para iniciar el servidor MCP `dist/bundle.cjs` de cada plugin).
- **La aplicación abierta Craft correspondiente** de [Storytold](https://github.com/storytold):
  - **Windows**: Instalador `.msi` o `.zip` portable (detección automática en `C:\Program Files\<App>`, `%LOCALAPPDATA%\Programs\<App>` o `PATH`).
  - **macOS**: App `.dmg` **más** el binario `<app>-cli-*-macos-universal.zip` en `/usr/local/bin` o `/opt/homebrew/bin`.
  - **Linux**: Paquete `.deb`, `.rpm` o `.tar.gz` (incluyen `<app>-cli`; AppImage/Flatpak solo contienen la interfaz gráfica).
- **Ruta personalizada (opcional)**: Define `<APP>_DIR` o `<APP>_CLI` (p. ej. `DESIGNCRAFT_DIR`, `SOUNDCRAFT_DIR`, `LIGHTCRAFT_DIR`) como variable de entorno del sistema si instalaste la app en otra carpeta.

## Gestión, Validación y Actualizaciones

Usa los subcomandos oficiales de `agy plugin` para listar, activar/desactivar, validar o actualizar cualquier plugin de la suite:

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

## Otros Entornos y Marketplaces

- **OpenAI Codex y DeepSeek Harness**: Usa el repositorio hermano [jhonsu01/craft-marketplace](https://github.com/jhonsu01/craft-marketplace).
- **Claude Desktop y Sunsam Code (paquetes `.mcpb` de doble clic)**:

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

## Licencia

Apache-2.0. Las aplicaciones Craft pertenecen a sus autores ([Storytold](https://github.com/storytold)); estos plugins no están afiliados ni respaldados por ellos.
