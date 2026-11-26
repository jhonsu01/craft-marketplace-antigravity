# PdfCraft for Google Antigravity

Merge, split, OCR, watermark, redact, fill forms, digitally sign, encrypt, compress, and convert PDFs to Word, HTML, images, and PDF/A.

## Bundled Antigravity Components

- **Skill (`/pdfcraft`)**: On-demand workflow guide and verified JSON tool patterns (`skills/pdfcraft/SKILL.md`).
- **Always-On Rule**: Non-destructive file safety, coordinate conventions, and `file:///` output link rules (`rules/AGENTS.md`).
- **MCP Server (`pdfcraft_pdfcraft_mcp`)**: 21 high-level local tools backed by `pdfcraft-cli` (`dist/bundle.cjs`).
- **Desktop App Integration**: Open PDFs directly in the PdfCraft desktop GUI whenever interactive visual review is needed.

## Requirements

1. **[PdfCraft](https://github.com/storytold/pdfcraft/releases)** installed locally (Windows, macOS, or Linux):
   - **Windows**: MSI installer or portable zip (auto-detected in `C:\Program Files\PdfCraft`, `%LOCALAPPDATA%\Programs\PdfCraft`, or `PATH`).
   - **macOS**: `.dmg` app **plus** the `pdfcraft-cli-*-macos-universal.zip` binary placed in `/usr/local/bin` or `/opt/homebrew/bin`.
   - **Linux**: `.deb`, `.rpm`, or `.tar.gz` (includes `pdfcraft-cli`; auto-detected in `/usr/bin`, `/usr/local/bin`, `/opt/pdfcraft/bin`, or `PATH`).
2. **Node.js >= 20** on `PATH`.

## Install in Google Antigravity

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/pdfcraft
```

## Optional Environment Variables

If PdfCraft is installed in a custom directory, set `PDFCRAFT_DIR` or `PDFCRAFT_CLI` in your environment before launching Antigravity.

## License

Apache-2.0. Upstream connector source: [pdfcraft-mcp-server](https://github.com/jhonsu01/pdfcraft-mcp-server). PdfCraft belongs to its authors ([Storytold](https://github.com/storytold/pdfcraft)).
