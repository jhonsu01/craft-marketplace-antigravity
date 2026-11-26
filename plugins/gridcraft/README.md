# GridCraft for Google Antigravity

Build, edit, evaluate live formulas (515 Excel functions), chart, PivotTable, and convert spreadsheets across XLSX, CSV, ODS, JSON, HTML, and PDF.

## Bundled Antigravity Components

- **Skill (`/gridcraft`)**: On-demand workflow guide and verified JSON tool patterns (`skills/gridcraft/SKILL.md`).
- **Always-On Rule**: Non-destructive file safety, coordinate conventions, and `file:///` output link rules (`rules/AGENTS.md`).
- **MCP Server (`gridcraft_gridcraft_mcp`)**: 9 high-level local tools backed by `gridcraft-cli` (`dist/bundle.cjs`).
- **Live Desktop Control**: Open files in the desktop app or drive it live over loopback port `7979`.

## Requirements

1. **[GridCraft](https://github.com/storytold/gridcraft/releases)** installed locally (Windows, macOS, or Linux):
   - **Windows**: MSI installer or portable zip (auto-detected in `C:\Program Files\GridCraft`, `%LOCALAPPDATA%\Programs\GridCraft`, or `PATH`).
   - **macOS**: `.dmg` app **plus** the `gridcraft-cli-*-macos-universal.zip` binary placed in `/usr/local/bin` or `/opt/homebrew/bin`.
   - **Linux**: `.deb`, `.rpm`, or `.tar.gz` (includes `gridcraft-cli`; auto-detected in `/usr/bin`, `/usr/local/bin`, `/opt/gridcraft/bin`, or `PATH`).
2. **Node.js >= 20** on `PATH`.

## Install in Google Antigravity

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/gridcraft
```

## Optional Environment Variables

If GridCraft is installed in a custom directory, set `GRIDCRAFT_DIR` or `GRIDCRAFT_CLI` in your environment before launching Antigravity.

## License

Apache-2.0. Upstream connector source: [gridcraft-mcp-server](https://github.com/jhonsu01/gridcraft-mcp-server). GridCraft belongs to its authors ([Storytold](https://github.com/storytold/gridcraft)).
