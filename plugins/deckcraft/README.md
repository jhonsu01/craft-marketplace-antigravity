# DeckCraft for Google Antigravity

Create, edit, inspect, and convert PowerPoint (.pptx) decks with themes, bullets, charts, tables, speaker notes, PDF handouts, and PNG slides.

## Bundled Antigravity Components

- **Skill (`/deckcraft`)**: On-demand workflow guide and verified JSON tool patterns (`skills/deckcraft/SKILL.md`).
- **Always-On Rule**: Non-destructive file safety, coordinate conventions, and `file:///` output link rules (`rules/AGENTS.md`).
- **MCP Server (`deckcraft_deckcraft_mcp`)**: 9 high-level local tools backed by `deckcraft-cli` (`dist/bundle.cjs`).
- **Live Desktop Control**: Open files in the desktop app or drive it live over loopback port `7990`.

## Requirements

1. **[DeckCraft](https://github.com/storytold/deckcraft/releases)** installed locally (Windows, macOS, or Linux):
   - **Windows**: MSI installer or portable zip (auto-detected in `C:\Program Files\DeckCraft`, `%LOCALAPPDATA%\Programs\DeckCraft`, or `PATH`).
   - **macOS**: `.dmg` app **plus** the `deckcraft-cli-*-macos-universal.zip` binary placed in `/usr/local/bin` or `/opt/homebrew/bin`.
   - **Linux**: `.deb`, `.rpm`, or `.tar.gz` (includes `deckcraft-cli`; auto-detected in `/usr/bin`, `/usr/local/bin`, `/opt/deckcraft/bin`, or `PATH`).
2. **Node.js >= 20** on `PATH`.

## Install in Google Antigravity

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/deckcraft
```

## Optional Environment Variables

If DeckCraft is installed in a custom directory, set `DECKCRAFT_DIR` or `DECKCRAFT_CLI` in your environment before launching Antigravity.

## License

Apache-2.0. Upstream connector source: [deckcraft-mcp-server](https://github.com/jhonsu01/deckcraft-mcp-server). DeckCraft belongs to its authors ([Storytold](https://github.com/storytold/deckcraft)).
