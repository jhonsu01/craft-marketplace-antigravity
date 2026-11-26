# FilmCraft for Google Antigravity

Split, trim, color-grade with Lumetri looks, apply 131 video effects, join clips with transitions, and export MP4, ProRes, GIF, and FCPXML.

## Bundled Antigravity Components

- **Skill (`/filmcraft`)**: On-demand workflow guide and verified JSON tool patterns (`skills/filmcraft/SKILL.md`).
- **Always-On Rule**: Non-destructive file safety, coordinate conventions, and `file:///` output link rules (`rules/AGENTS.md`).
- **MCP Server (`filmcraft_filmcraft_mcp`)**: 11 high-level local tools backed by `filmcraft-cli` (`dist/bundle.cjs`).
- **Live Desktop Control**: Open files in the desktop app or drive it live over loopback port `9876`.

## Requirements

1. **[FilmCraft](https://github.com/storytold/filmcraft/releases)** installed locally (Windows, macOS, or Linux):
   - **Windows**: MSI installer or portable zip (auto-detected in `C:\Program Files\FilmCraft`, `%LOCALAPPDATA%\Programs\FilmCraft`, or `PATH`).
   - **macOS**: `.dmg` app **plus** the `filmcraft-cli-*-macos-universal.zip` binary placed in `/usr/local/bin` or `/opt/homebrew/bin`.
   - **Linux**: `.deb`, `.rpm`, or `.tar.gz` (includes `filmcraft-cli`; auto-detected in `/usr/bin`, `/usr/local/bin`, `/opt/filmcraft/bin`, or `PATH`).
2. **Node.js >= 20** on `PATH`.

## Install in Google Antigravity

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/filmcraft
```

## Optional Environment Variables

If FilmCraft is installed in a custom directory, set `FILMCRAFT_DIR` or `FILMCRAFT_CLI` in your environment before launching Antigravity.

## License

Apache-2.0. Upstream connector source: [filmcraft-mcp-server](https://github.com/jhonsu01/filmcraft-mcp-server). FilmCraft belongs to its authors ([Storytold](https://github.com/storytold/filmcraft)).
