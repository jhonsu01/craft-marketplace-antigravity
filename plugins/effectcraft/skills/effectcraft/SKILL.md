---
name: effectcraft
description: Create motion graphics, animated titles, templates, keyframes, expressions, and visual effects (308 effects, 766 commands), and render MP4, ProRes, WebM, GIF, image sequences, Lottie, and .ecproj using the local EffectCraft desktop application and CLI engine.
---

# EffectCraft Motion Graphics & VFX Compositor Automation

This skill enables full integration with the **EffectCraft** After Effects-class compositor and headless CLI engine (`effectcraft-cli`) installed on your local computer.

## Available Capabilities & Tools

EffectCraft exposes 11 high-level MCP tools:

1. **`create_motion_graphic`**: Build compositions of any resolution, frame rate, and duration from top-to-bottom layers (text, shapes, solids, images/videos/audio, nulls, adjustment layers) with entrance/exit animations (`fade`, `slide_left`/`right`/`up`/`down`, `pop`, `zoom`, `blur`, `typewriter`, `spin`), keyframes, After Effects-style JavaScript expressions, and 308 visual effects. Exports MP4, HEVC, AV1, ProRes (with alpha), WebM, GIF, image sequences, Lottie, and editable `.ecproj`.
2. **`apply_effects`**: Apply visual effects (with animated keyframes), trims, speed changes, and top-layer titles/logos to one video/image or a whole folder.
3. **`use_template`**: Populate built-in Essential Graphics templates (`lower-third`, `title-card`, `logo-reveal`, `kinetic-type`, `social-square`, `vertical-story`, `slideshow`, `3d-text-orbit`) or `.ectemplate` files with custom text/color values and background media.
4. **`render_project`**: Render any composition of an `.ecproj` file with custom time ranges, resolution, frame rate, quality, alpha channel, and output formats without modifying the source project.
5. **`get_project_info`**: Inspect compositions, layer stacks, footage items (including missing files), and Essential Graphics template controls in an `.ecproj` or `.ectemplate`.
6. **`render_frame`**: Render preview frames at specific timestamps (`times` in seconds) from an `.ecproj` or video file.
7. **`list_effectcraft_catalog`**: Browse 308 visual effects (with parameter IDs), motion templates (with control names), installed fonts, 766 engine commands, and supported formats.
8. **`run_effectcraft_script`**: Execute After Effects-style JavaScript (`app.project`, `addComp`, `layers.addText`, `setValueAtTime`, expressions) and render outputs.
9. **`run_effectcraft_commands`**: Run raw EffectCraft engine commands (`comp.new`, `set_property`, `add_keyframe`, `add_effect`, `$steps[N]` references) headless or live (`live: true`, port `9877`).
10. **`open_in_effectcraft`**: Open `.ecproj` projects or media files in the EffectCraft desktop application.
11. **`get_effectcraft_status`**: Check installation paths, `effectcraft-cli` version, command/effect counts, and live control port status.

## Practical Examples

### 1. Creating an Animated Intro (MP4 + GIF + Lottie + .ecproj)

```json
{
  "name": "Intro_Antigravity",
  "width": 1280,
  "height": 720,
  "fps": 30,
  "duration": 4,
  "background": "#0F172A",
  "layers": [
    {
      "type": "text",
      "text": "EFFECTCRAFT LIVE",
      "size": 84,
      "color": "#FFFFFF",
      "y": 340,
      "animate_in": { "type": "typewriter", "duration": 1.2 },
      "effects": [{ "effect": "Glow" }]
    },
    {
      "type": "shape",
      "shape": "ellipse",
      "width": 520,
      "height": 520,
      "color": "#7C3AED",
      "opacity": 35,
      "expressions": [
        {
          "property": "scale",
          "expression": "[100 + 6*Math.sin(time*3), 100 + 6*Math.sin(time*3)]"
        }
      ]
    }
  ],
  "formats": ["mp4", "gif", "lottie", "ecproj"],
  "output_dir": "/path/to/workspace"
}
```

### 2. Rendering a Lower Third Template Over Footage

```json
{
  "template": "lower-third",
  "values": {
    "Name": "Jhon Supelano",
    "Title": "Arquitectura Agéntica v8",
    "Bar Color": "#7C3AED"
  },
  "background_media": "/path/to/workspace\\test_filmcraft_showcase.mp4",
  "duration": 4,
  "formats": ["mp4", "ecproj"],
  "output_dir": "/path/to/workspace"
}
```

## Best Practices

- Always supply **absolute paths** (e.g. `/Users/alex/project/file.ext` on macOS/Linux or `C:\Users\alex\project\file.ext` on Windows).
- Layers in `create_motion_graphic` are ordered **top to bottom** (first layer in the array renders in front).
- Positions are in **pixels from the top-left**; durations and timestamps are in **seconds**.
- Always surface output file links using `[filename](file:///absolute/path/to/file)`.
