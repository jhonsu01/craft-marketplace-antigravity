# VectorCraft for Google Antigravity

Vectorize bitmaps with Image Trace, compose vector art and charts, recolor, and convert across 20 formats (SVG, PDF, AI, EPS, DXF).

## Bundled Antigravity Components

- **Skill (`/vectorcraft`)**: On-demand workflow guide and verified JSON tool patterns (`skills/vectorcraft/SKILL.md`).
- **Always-On Rule**: Non-destructive file safety, coordinate conventions, and `file:///` output link rules (`rules/AGENTS.md`).
- **MCP Server (`vectorcraft_vectorcraft_mcp`)**: 10 high-level local tools backed by `vectorcraft-cli` (`dist/bundle.cjs`).
- **Live Desktop Control**: Open files in the desktop app or drive it live over loopback port `7979`.

## Requirements

1. **[VectorCraft](https://github.com/storytold/vectorcraft/releases)** installed locally (Windows, macOS, or Linux):
   - **Windows**: MSI installer or portable zip (auto-detected in `C:\Program Files\VectorCraft`, `%LOCALAPPDATA%\Programs\VectorCraft`, or `PATH`).
   - **macOS**: `.dmg` app **plus** the `vectorcraft-cli-*-macos-universal.zip` binary placed in `/usr/local/bin` or `/opt/homebrew/bin`.
   - **Linux**: `.deb`, `.rpm`, or `.tar.gz` (includes `vectorcraft-cli`; auto-detected in `/usr/bin`, `/usr/local/bin`, `/opt/vectorcraft/bin`, or `PATH`).
2. **Node.js >= 20** on `PATH`.

## Install in Google Antigravity

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/vectorcraft
```

## Optional Environment Variables

If VectorCraft is installed in a custom directory, set `VECTORCRAFT_DIR` or `VECTORCRAFT_CLI` in your environment before launching Antigravity.

## License

Apache-2.0. Upstream connector source: [vectorcraft-mcp-server](https://github.com/jhonsu01/vectorcraft-mcp-server). VectorCraft belongs to its authors ([Storytold](https://github.com/storytold/vectorcraft)).
