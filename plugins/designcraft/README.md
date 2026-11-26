# DesignCraft for Google Antigravity

Page layout, CSV data merge, InDesign IDML, and print-ready PDF/X-4, PNG, EPUB, and HTML using your local DesignCraft engine.

## Bundled Antigravity Components

- **Skill (`/designcraft`)**: On-demand workflow guide and verified JSON tool patterns (`skills/designcraft/SKILL.md`).
- **Always-On Rule**: Non-destructive file safety, coordinate conventions, and `file:///` output link rules (`rules/AGENTS.md`).
- **MCP Server (`designcraft_designcraft_mcp`)**: 10 high-level local tools backed by `designcraft-cli` (`dist/bundle.cjs`).
- **Live Desktop Control**: Open files in the desktop app or drive it live over loopback port `7981`.

## Requirements

1. **[DesignCraft](https://github.com/storytold/designcraft/releases)** installed locally (Windows, macOS, or Linux):
   - **Windows**: MSI installer or portable zip (auto-detected in `C:\Program Files\DesignCraft`, `%LOCALAPPDATA%\Programs\DesignCraft`, or `PATH`).
   - **macOS**: `.dmg` app **plus** the `designcraft-cli-*-macos-universal.zip` binary placed in `/usr/local/bin` or `/opt/homebrew/bin`.
   - **Linux**: `.deb`, `.rpm`, or `.tar.gz` (includes `designcraft-cli`; auto-detected in `/usr/bin`, `/usr/local/bin`, `/opt/designcraft/bin`, or `PATH`).
2. **Node.js >= 20** on `PATH`.

## Install in Google Antigravity

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/designcraft
```

## Optional Environment Variables

If DesignCraft is installed in a custom directory, set `DESIGNCRAFT_DIR` or `DESIGNCRAFT_CLI` in your environment before launching Antigravity.

## License

Apache-2.0. Upstream connector source: [designcraft-mcp-server](https://github.com/jhonsu01/designcraft-mcp-server). DesignCraft belongs to its authors ([Storytold](https://github.com/storytold/designcraft)).
