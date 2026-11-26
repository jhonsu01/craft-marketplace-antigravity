# LightCraft for Google Antigravity

Develop RAW photos and batches with auto tone, 125 sliders, presets, local masks, HDR/panorama DNG merges, and sharpness culling.

## Bundled Antigravity Components

- **Skill (`/lightcraft`)**: On-demand workflow guide and verified JSON tool patterns (`skills/lightcraft/SKILL.md`).
- **Always-On Rule**: Non-destructive file safety, coordinate conventions, and `file:///` output link rules (`rules/AGENTS.md`).
- **MCP Server (`lightcraft_lightcraft_mcp`)**: 10 high-level local tools backed by `lightcraft-cli` (`dist/bundle.cjs`).
- **Live Desktop Control**: Open files in the desktop app or drive it live over loopback port `7980`.

## Requirements

1. **[LightCraft](https://github.com/storytold/lightcraft/releases)** installed locally (Windows, macOS, or Linux):
   - **Windows**: MSI installer or portable zip (auto-detected in `C:\Program Files\LightCraft`, `%LOCALAPPDATA%\Programs\LightCraft`, or `PATH`).
   - **macOS**: `.dmg` app **plus** the `lightcraft-cli-*-macos-universal.zip` binary placed in `/usr/local/bin` or `/opt/homebrew/bin`.
   - **Linux**: `.deb`, `.rpm`, or `.tar.gz` (includes `lightcraft-cli`; auto-detected in `/usr/bin`, `/usr/local/bin`, `/opt/lightcraft/bin`, or `PATH`).
2. **Node.js >= 20** on `PATH`.

## Install in Google Antigravity

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/lightcraft
```

## Optional Environment Variables

If LightCraft is installed in a custom directory, set `LIGHTCRAFT_DIR` or `LIGHTCRAFT_CLI` in your environment before launching Antigravity.

## License

Apache-2.0. Upstream connector source: [lightcraft-mcp-server](https://github.com/jhonsu01/lightcraft-mcp-server). LightCraft belongs to its authors ([Storytold](https://github.com/storytold/lightcraft)).
