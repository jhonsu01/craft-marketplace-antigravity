# SoundCraft for Google Antigravity

Compose multitrack audio and MIDI synth/drum sessions, mix with 30 built-in plugins, measure LUFS loudness, and export WAV, FLAC, stems, and MIDI.

## Bundled Antigravity Components

- **Skill (`/soundcraft`)**: On-demand workflow guide and verified JSON tool patterns (`skills/soundcraft/SKILL.md`).
- **Always-On Rule**: Non-destructive file safety, coordinate conventions, and `file:///` output link rules (`rules/AGENTS.md`).
- **MCP Server (`soundcraft_soundcraft_mcp`)**: 10 high-level local tools backed by `soundcraft-cli` (`dist/bundle.cjs`).
- **Live Desktop Control**: Open files in the desktop app or drive it live over loopback port `7801`.

## Requirements

1. **[SoundCraft](https://github.com/storytold/soundcraft/releases)** installed locally (Windows, macOS, or Linux):
   - **Windows**: MSI installer or portable zip (auto-detected in `C:\Program Files\SoundCraft`, `%LOCALAPPDATA%\Programs\SoundCraft`, or `PATH`).
   - **macOS**: `.dmg` app **plus** the `soundcraft-cli-*-macos-universal.zip` binary placed in `/usr/local/bin` or `/opt/homebrew/bin`.
   - **Linux**: `.deb`, `.rpm`, or `.tar.gz` (includes `soundcraft-cli`; auto-detected in `/usr/bin`, `/usr/local/bin`, `/opt/soundcraft/bin`, or `PATH`).
2. **Node.js >= 20** on `PATH`.

## Install in Google Antigravity

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/soundcraft
```

## Optional Environment Variables

If SoundCraft is installed in a custom directory, set `SOUNDCRAFT_DIR` or `SOUNDCRAFT_CLI` in your environment before launching Antigravity.

## License

Apache-2.0. Upstream connector source: [soundcraft-mcp-server](https://github.com/jhonsu01/soundcraft-mcp-server). SoundCraft belongs to its authors ([Storytold](https://github.com/storytold/soundcraft)).
