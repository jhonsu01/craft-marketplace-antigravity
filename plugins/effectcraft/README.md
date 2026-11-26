# EffectCraft for Google Antigravity

Create motion graphics, animated titles, templates, keyframes, expressions, and VFX; render MP4, ProRes, WebM, GIF, and Lottie.

## Bundled Antigravity Components

- **Skill (`/effectcraft`)**: On-demand workflow guide and verified JSON tool patterns (`skills/effectcraft/SKILL.md`).
- **Always-On Rule**: Non-destructive file safety, coordinate conventions, and `file:///` output link rules (`rules/AGENTS.md`).
- **MCP Server (`effectcraft_effectcraft_mcp`)**: 11 high-level local tools backed by `effectcraft-cli` (`dist/bundle.cjs`).
- **Live Desktop Control**: Open files in the desktop app or drive it live over loopback port `9877`.

## Requirements

1. **[EffectCraft](https://github.com/storytold/effectcraft/releases)** installed locally (Windows, macOS, or Linux):
   - **Windows**: MSI installer or portable zip (auto-detected in `C:\Program Files\EffectCraft`, `%LOCALAPPDATA%\Programs\EffectCraft`, or `PATH`).
   - **macOS**: `.dmg` app **plus** the `effectcraft-cli-*-macos-universal.zip` binary placed in `/usr/local/bin` or `/opt/homebrew/bin`.
   - **Linux**: `.deb`, `.rpm`, or `.tar.gz` (includes `effectcraft-cli`; auto-detected in `/usr/bin`, `/usr/local/bin`, `/opt/effectcraft/bin`, or `PATH`).
2. **Node.js >= 20** on `PATH`.

## Install in Google Antigravity

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/effectcraft
```

## Optional Environment Variables

If EffectCraft is installed in a custom directory, set `EFFECTCRAFT_DIR` or `EFFECTCRAFT_CLI` in your environment before launching Antigravity.

## License

Apache-2.0. Upstream connector source: [effectcraft-mcp-server](https://github.com/jhonsu01/effectcraft-mcp-server). EffectCraft belongs to its authors ([Storytold](https://github.com/storytold/effectcraft)).
