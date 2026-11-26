<p align="center"><img src="plugins/designcraft/assets/logo.png" width="96" alt="Craft Suite for Antigravity"></p>

<h1 align="center">Пакет Craft для Google Antigravity</h1>

<p align="center">
  <a href="README.md">English</a> · <a href="README.es.md">Español</a> · <a href="README.pt-BR.md">Português</a> · <a href="README.fr.md">Français</a> · <a href="README.de.md">Deutsch</a> · <b>Русский</b> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a>
</p>

<p align="center">Нативный маркетплейс плагинов Google Antigravity для 11 открытых приложений Craft, установленных на вашем компьютере (Windows, macOS, Linux).</p>

---

## Плагины (11 Нативных Пакетов)

Каждый плагин включает **1 Навык** (`/<plugin>`), **1 Постоянное Правило** (`rules/AGENTS.md`), **3 Стартовых Промпта** и **1 Локальный MCP-сервер** (`${PLUGIN_ROOT}/dist/bundle.cjs`), работающий локально без загрузки файлов в облако.

| Плагин и Команда | Что делает | Требуется |
| --- | --- | --- |
| **DesignCraft** (`/designcraft`) | Вёрстка страниц, слияние CSV, InDesign IDML, печатный PDF/X-4, PNG, EPUB и HTML | [DesignCraft](https://github.com/storytold/designcraft) + Node.js ≥ 20 |
| **EffectCraft** (`/effectcraft`) | Моушн-графика, анимированные титры, видеоэффекты VFX, шаблоны; MP4, ProRes, WebM, GIF, Lottie | [EffectCraft](https://github.com/storytold/effectcraft) + Node.js ≥ 20 |
| **LightCraft** (`/lightcraft`) | Проявка RAW: автотон, 125 ползунков, пресеты, маски, HDR и панорамы; JPEG, TIFF, WebP, AVIF, DNG | [LightCraft](https://github.com/storytold/lightcraft) + Node.js ≥ 20 |
| **PhotoCraft** (`/photocraft`) | Редактирование фото по слоям: размер, кадрирование, Camera Raw, 123 фильтра, удаление фона, текст; PSD, PNG, JPEG, WebP | [PhotoCraft](https://github.com/storytold/photocraft) + Node.js ≥ 20 |
| **VectorCraft** (`/vectorcraft`) | Векторная графика: трассировка изображений, фигуры, текст и диаграммы, перекраска; SVG, PDF, AI, EPS, DXF, PNG | [VectorCraft](https://github.com/storytold/vectorcraft) + Node.js ≥ 20 |
| **PdfCraft** (`/pdfcraft`) | Работа с PDF: объединение, разделение, страницы, OCR, формы, подписи, скрытие данных, пароли; в Word, HTML, изображения, PDF/A | [PdfCraft](https://github.com/storytold/pdfcraft) + Node.js ≥ 20 |
| **FilmCraft** (`/filmcraft`) | Видеомонтаж: нарезка, обрезка, 131 эффект, цветокоррекция Lumetri, титры, переходы; H.264, ProRes, GIF, FCPXML, OTIO | [FilmCraft](https://github.com/storytold/filmcraft) + Node.js ≥ 20 |
| **WordCraft** (`/wordcraft`) | Текстовый процессор: документы с заголовками, таблицами и изображениями, поиск/замена, комментарии, правки, слияние; DOCX, PDF, ODT, RTF, Markdown, LaTeX | [WordCraft](https://github.com/storytold/wordcraft) + Node.js ≥ 20 |
| **SoundCraft** (`/soundcraft`) | Цифровая аудиостанция (DAW): многодорожечное аудио и MIDI-синтезаторы/ударные, 30 плагинов, шины, громкость LUFS, стемы; WAV, AIFF, FLAC | [SoundCraft](https://github.com/storytold/soundcraft) + Node.js ≥ 20 |
| **DeckCraft** (`/deckcraft`) | Презентации: слайды со списками, картинками, диаграммами, таблицами и заметками, темы, переходы; PowerPoint PPTX, раздаточные PDF, PNG | [DeckCraft](https://github.com/storytold/deckcraft) + Node.js ≥ 20 |
| **GridCraft** (`/gridcraft`) | Электронные таблицы: книги с 515 живыми формулами Excel, таблицами, диаграммами и сводными таблицами; XLSX, CSV, ODS, JSON, HTML, PDF | [GridCraft](https://github.com/storytold/gridcraft) + Node.js ≥ 20 |

## Установка в Google Antigravity Harness

### 1. Прямая Установка Одной Командой (`agy` CLI)

Установите любой плагин напрямую из GitHub без ручного клонирования. Установленные плагины автоматически синхронизируются между **Antigravity CLI**, **Antigravity App** (*Customizations → Installed*) и **Antigravity IDE**:

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

> В интерактивном режиме `agy` также можно выполнить `/plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/<имя-плагина>`.

### 2. Установка Всех 11 Плагинов Сразу

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

### 3. Antigravity App и Antigravity IDE (Глобально или для Проекта)

- **Глобальная установка**: `agy plugin install` распаковывает плагин в `~/.gemini/config/plugins/<имя>` (`%USERPROFILE%\.gemini\config\plugins\<имя>` в Windows), после чего он сразу доступен во вкладке **Customizations → Installed**.
- **Для конкретного проекта (workspace)**: Скопируйте `plugins/<имя>` в `.agents/plugins/<имя>` в корне проекта или откройте сам этот репозиторий (настроен через `.agents/plugins.json`).

## Требования и Кроссплатформенная Настройка

- **Node.js ≥ 20** в `PATH`.
- **Соответствующее открытое приложение Craft** от [Storytold](https://github.com/storytold): Windows (`.msi`/`.zip`), macOS (`.dmg` + бинарный файл `<app>-cli` в `/usr/local/bin` или `/opt/homebrew/bin`) или Linux (`.deb`, `.rpm`, `.tar.gz`).
- **Нестандартная папка (опционально)**: Задайте `<APP>_DIR` или `<APP>_CLI` (например `DESIGNCRAFT_DIR`) в переменных окружения системы.

## Управление, Проверка и Обновление

Используйте команды `agy plugin` для просмотра списка, включения/выключения, валидации и обновления:

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

## Другие Среды и Маркетплейсы

- **OpenAI Codex и DeepSeek Harness**: См. [jhonsu01/craft-marketplace](https://github.com/jhonsu01/craft-marketplace).
- **Claude Desktop и Sunsam Code (пакеты `.mcpb`)**:

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

## Лицензия

Apache-2.0. Приложения Craft принадлежат их авторам ([Storytold](https://github.com/storytold)); эти плагины не связаны с ними и не одобрены ими.
