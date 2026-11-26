<p align="center"><img src="plugins/designcraft/assets/logo.png" width="96" alt="Craft Suite for Antigravity"></p>

<h1 align="center">Google Antigravity용 Craft 스위트</h1>

<p align="center">
  <a href="README.md">English</a> · <a href="README.es.md">Español</a> · <a href="README.pt-BR.md">Português</a> · <a href="README.fr.md">Français</a> · <a href="README.de.md">Deutsch</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.ja.md">日本語</a> · <b>한국어</b>
</p>

<p align="center">컴퓨터(Windows, macOS, Linux)에 설치된 11개의 오픈 소스 Craft 앱을 연결하는 Google Antigravity 네이티브 플러그인 마켓플레이스입니다.</p>

---

## 플러그인 목록 (11개 네이티브 번들)

모든 플러그인은 **스킬 1개**(`/<plugin>`), **항상 켜짐 규칙 1개**(`rules/AGENTS.md`), **시작 프롬프트 칩 3개**, 클라우드 업로드 없이 로컬 헤드리스로 동작하는 **로컬 MCP 서버 1개**(`${PLUGIN_ROOT}/dist/bundle.cjs`)를 포함합니다.

| 플러그인 및 슬래시 명령 | 기능 | 필요 사항 |
| --- | --- | --- |
| **DesignCraft** (`/designcraft`) | 페이지 레이아웃, CSV 데이터 병합, InDesign IDML, 인쇄용 PDF/X-4, PNG, EPUB, HTML | [DesignCraft](https://github.com/storytold/designcraft) + Node.js ≥ 20 |
| **EffectCraft** (`/effectcraft`) | 모션 그래픽, 애니메이션 타이틀, 비디오 VFX, 템플릿; MP4, ProRes, WebM, GIF, Lottie | [EffectCraft](https://github.com/storytold/effectcraft) + Node.js ≥ 20 |
| **LightCraft** (`/lightcraft`) | RAW 현상: 자동 톤, 125개 슬라이더, 프리셋, 로컬 마스크, HDR·파노라마 병합; JPEG, TIFF, WebP, AVIF, DNG | [LightCraft](https://github.com/storytold/lightcraft) + Node.js ≥ 20 |
| **PhotoCraft** (`/photocraft`) | 레이어 사진 편집: 크기 조절, 자르기, Camera Raw, 123개 필터, 배경 제거, 텍스트; PSD, PNG, JPEG, WebP | [PhotoCraft](https://github.com/storytold/photocraft) + Node.js ≥ 20 |
| **VectorCraft** (`/vectorcraft`) | 벡터 디자인: 이미지 추적(Image Trace), 도형·텍스트·차트, 색상 변경; SVG, PDF, AI, EPS, DXF, PNG | [VectorCraft](https://github.com/storytold/vectorcraft) + Node.js ≥ 20 |
| **PdfCraft** (`/pdfcraft`) | PDF 도구 모음: 병합, 분할, 페이지, OCR, 양식, 전자 서명, 민감 정보 가리기, 암호화; Word, HTML, 이미지, PDF/A 변환 | [PdfCraft](https://github.com/storytold/pdfcraft) + Node.js ≥ 20 |
| **FilmCraft** (`/filmcraft`) | 영상 편집: 분할, 트림, 131개 효과, Lumetri 색 보정, 타이틀, 전환 효과; H.264, ProRes, GIF, FCPXML, OTIO | [FilmCraft](https://github.com/storytold/filmcraft) + Node.js ≥ 20 |
| **WordCraft** (`/wordcraft`) | 워드 프로세서: 제목·표·이미지 문서 작성, 찾기/바꾸기, 메모, 변경 내용 추적, 편지 병합; DOCX, PDF, ODT, RTF, Markdown, LaTeX | [WordCraft](https://github.com/storytold/wordcraft) + Node.js ≥ 20 |
| **SoundCraft** (`/soundcraft`) | 디지털 오디오 워크스테이션(DAW): 멀티트랙 오디오 & MIDI 신스/드럼, 30개 플러그인, 버스, LUFS 음압 측정, 스템; WAV, AIFF, FLAC | [SoundCraft](https://github.com/storytold/soundcraft) + Node.js ≥ 20 |
| **DeckCraft** (`/deckcraft`) | 프레젠테이션: 글머리 기호·그림·차트·표·발표자 노트 슬라이드, 테마, 전환; PowerPoint PPTX, 유인물 PDF, PNG | [DeckCraft](https://github.com/storytold/deckcraft) + Node.js ≥ 20 |
| **GridCraft** (`/gridcraft`) | 스프레드시트: 515개 실시간 Excel 수식, 표, 차트, 피벗 테이블 통합 문서; XLSX, CSV, ODS, JSON, HTML, PDF | [GridCraft](https://github.com/storytold/gridcraft) + Node.js ≥ 20 |

## Google Antigravity Harness에 설치

### 1. GitHub에서 한 줄 명령으로 설치 (`agy` CLI)

수동 클론 없이 GitHub 하위 경로에서 바로 설치할 수 있습니다. 설치된 플러그인은 **Antigravity CLI**, **Antigravity App**(*Customizations → Installed*), **Antigravity IDE** 간에 자동 동기화됩니다:

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

> 대화형 `agy` 세션 안에서는 `/plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/<플러그인-이름>` 명령도 사용할 수 있습니다.

### 2. 11개 전체 Craft 스위트 한 번에 설치

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

### 3. Antigravity App 및 Antigravity IDE (전역 또는 워크스페이스)

- **전역 설치**: `agy plugin install`은 `~/.gemini/config/plugins/<이름>`(Windows는 `%USERPROFILE%\.gemini\config\plugins\<이름>`)에 설치하며 앱의 **Customizations → Installed** 탭에 즉시 표시됩니다.
- **워크스페이스 설치**: 프로젝트 루트의 `.agents/plugins/<이름>`에 복사하거나 이 저장소를 직접 워크스페이스로 여세요(`.agents/plugins.json` 사전 구성됨).

## 필수 구성 요소 및 크로스 플랫폼 설정

- `PATH`에 설치된 **Node.js ≥ 20**.
- [Storytold](https://github.com/storytold)의 해당 **오픈 소스 Craft 앱**: Windows(`.msi`/`.zip`), macOS(`.dmg` 앱 **및** `/usr/local/bin` 또는 `/opt/homebrew/bin`의 `<app>-cli`), Linux(`.deb`, `.rpm`, `.tar.gz`).
- **사용자 지정 경로(선택)**: 기본 폴더가 아닌 곳에 설치했다면 `<APP>_DIR` 또는 `<APP>_CLI`(예: `DESIGNCRAFT_DIR`)를 시스템 환경 변수로 설정하세요.

## 관리, 검증 및 업데이트

`agy plugin` 명령으로 목록 확인, 활성화/비활성화, 검증 및 업데이트를 수행합니다:

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

## 다른 호스트 및 마켓플레이스

- **OpenAI Codex 및 DeepSeek Harness**: 자매 저장소 [jhonsu01/craft-marketplace](https://github.com/jhonsu01/craft-marketplace)를 참고하세요.
- **Claude Desktop 및 Sunsam Code (`.mcpb` 원클릭 번들)**:

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

## 라이선스

Apache-2.0. Craft 앱의 권리는 원저작자([Storytold](https://github.com/storytold))에게 있으며, 이 플러그인들은 그들과 관련이 없거나 보증을 받지 않았습니다.
