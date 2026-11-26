# PhotoCraft for Google Antigravity

Edit photos and layered designs: resize, crop, Camera Raw, 123 filters, background removal, text, and PSD/PNG/JPEG/WebP conversion.

## Bundled Antigravity Components

- **Skill (`/photocraft`)**: On-demand workflow guide and verified JSON tool patterns (`skills/photocraft/SKILL.md`).
- **Always-On Rule**: Non-destructive file safety, coordinate conventions, and `file:///` output link rules (`rules/AGENTS.md`).
- **MCP Server (`photocraft_photocraft_mcp`)**: 10 high-level local tools backed by `photocraft-cli` (`dist/bundle.cjs`).
- **Live Desktop Control**: Open files in the desktop app or drive it live over loopback port `7878`.

## Requirements

1. **[PhotoCraft](https://github.com/storytold/photocraft/releases)** installed locally (Windows, macOS, or Linux):
   - **Windows**: MSI installer or portable zip (auto-detected in `C:\Program Files\PhotoCraft`, `%LOCALAPPDATA%\Programs\PhotoCraft`, or `PATH`).
   - **macOS**: `.dmg` app **plus** the `photocraft-cli-*-macos-universal.zip` binary placed in `/usr/local/bin` or `/opt/homebrew/bin`.
   - **Linux**: `.deb`, `.rpm`, or `.tar.gz` (includes `photocraft-cli`; auto-detected in `/usr/bin`, `/usr/local/bin`, `/opt/photocraft/bin`, or `PATH`).
2. **Node.js >= 20** on `PATH`.

## Install in Google Antigravity

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/photocraft
```

## Optional Environment Variables

If PhotoCraft is installed in a custom directory, set `PHOTOCRAFT_DIR` or `PHOTOCRAFT_CLI` in your environment before launching Antigravity.

## License

Apache-2.0. Upstream connector source: [photocraft-mcp-server](https://github.com/jhonsu01/photocraft-mcp-server). PhotoCraft belongs to its authors ([Storytold](https://github.com/storytold/photocraft)).
