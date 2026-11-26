# WordCraft for Google Antigravity

Author, edit with tracked changes and comments, mail-merge, and convert documents across DOCX, PDF, ODT, RTF, HTML, Markdown, and LaTeX.

## Bundled Antigravity Components

- **Skill (`/wordcraft`)**: On-demand workflow guide and verified JSON tool patterns (`skills/wordcraft/SKILL.md`).
- **Always-On Rule**: Non-destructive file safety, coordinate conventions, and `file:///` output link rules (`rules/AGENTS.md`).
- **MCP Server (`wordcraft_wordcraft_mcp`)**: 11 high-level local tools backed by `wordcraft-cli` (`dist/bundle.cjs`).
- **Live Desktop Control**: Open files in the desktop app or drive it live over loopback port `7985`.

## Requirements

1. **[WordCraft](https://github.com/storytold/wordcraft/releases)** installed locally (Windows, macOS, or Linux):
   - **Windows**: MSI installer or portable zip (auto-detected in `C:\Program Files\WordCraft`, `%LOCALAPPDATA%\Programs\WordCraft`, or `PATH`).
   - **macOS**: `.dmg` app **plus** the `wordcraft-cli-*-macos-universal.zip` binary placed in `/usr/local/bin` or `/opt/homebrew/bin`.
   - **Linux**: `.deb`, `.rpm`, or `.tar.gz` (includes `wordcraft-cli`; auto-detected in `/usr/bin`, `/usr/local/bin`, `/opt/wordcraft/bin`, or `PATH`).
2. **Node.js >= 20** on `PATH`.

## Install in Google Antigravity

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/wordcraft
```

## Optional Environment Variables

If WordCraft is installed in a custom directory, set `WORDCRAFT_DIR` or `WORDCRAFT_CLI` in your environment before launching Antigravity.

## License

Apache-2.0. Upstream connector source: [wordcraft-mcp-server](https://github.com/jhonsu01/wordcraft-mcp-server). WordCraft belongs to its authors ([Storytold](https://github.com/storytold/wordcraft)).
