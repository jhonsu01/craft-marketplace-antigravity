---
name: filmcraft
description: Split, trim, edit (131 video effects, 18 Lumetri looks, animated titles, speed, 58 audio effects), join with 112 transitions, convert, and export video and editable timelines (.fcproj, FCPXML, OTIO, Premiere XML) using the local FilmCraft desktop application and CLI engine.
---

# FilmCraft Video Editing & Timeline Automation

This skill enables full integration with the **FilmCraft** desktop NLE application and headless CLI engine (`filmcraft-cli`) installed on your local computer.

## Available Capabilities & Tools

FilmCraft exposes 11 high-level MCP tools:

1. **`split_video`**: Cut one or multiple videos into frame-accurate N-second segments (`<name>_001.mp4`...), creating one folder per input, with optional `.fcproj` timeline output.
2. **`edit_video`**: Apply 131 video effects (with parameters and keyframes), 18 Lumetri color looks, burned-in animated titles, speed/reverse changes, 58 audio effects, volume, and fades on one or many files, plus optional editable outputs (`.fcproj`, `otio`, `fcpxml`, `xml`, `edl`, `aaf`).
3. **`trim_video`**: Extract a specific time range (`start` to `end` in seconds) with optional `fade_in` and `fade_out`.
4. **`concat_videos`**: Join multiple video clips, still images, and audio tracks using any of 112 transitions (e.g. `cross_dissolve`).
5. **`convert_media`**: Transcode media across H.264 MP4, ProRes, DNxHR, MJPEG, MXF, animated GIF, PNG/TIFF sequences, or extract WAV/AIFF audio using custom settings or 45 export presets.
6. **`get_media_info`**: Inspect container format, duration, video codec, dimensions, frame rate, and audio streams.
7. **`render_frame`**: Render a single frame at any timestamp (`seconds`) from a video file or `.fcproj` project to PNG for visual inspection.
8. **`list_catalog`**: Browse all video effects, audio effects, transitions, Lumetri color presets, export presets, and engine commands.
9. **`run_commands`**: Execute raw FilmCraft engine commands sequentially with `$steps[N]` cross-references, headless or against a live FilmCraft window (`live: true`, port `9876`).
10. **`open_in_filmcraft`**: Open `.fcproj` projects or media files directly in the FilmCraft desktop application.
11. **`get_filmcraft_status`**: Verify installation paths, `filmcraft-cli` version, control port status, and catalog counts.

## Practical Examples

### 1. Editing a Clip with Lumetri Look, Keyframes, Title & FCPXML Export

```json
{
  "input_path": "/path/to/Videos/clip_playa.mp4",
  "effects": [
    { "effect": "vignette", "params": { "amount": -60 } },
    {
      "effect": "motion",
      "keyframes": {
        "scale": [
          { "seconds": 0, "value": 100 },
          { "seconds": 3, "value": 115 }
        ]
      }
    }
  ],
  "color_preset": "Golden Dusk",
  "texts": [
    {
      "text": "Miami Sunset 2026",
      "placement": "bottom",
      "color": "#FFCC00",
      "stroke_color": "#000000",
      "size": 56
    }
  ],
  "fade_in": 0.5,
  "save_project": true,
  "interchange": ["fcpxml", "otio"]
}
```

### 2. Joining Multiple Clips with Cross Dissolve

```json
{
  "inputs": [
    "/path/to/Videos/toma_01.mp4",
    "/path/to/Videos/toma_02.mp4",
    "/path/to/Videos/toma_03.mp4"
  ],
  "output_path": "/path/to/Videos/montaje_final.mp4",
  "transition": "cross_dissolve",
  "transition_seconds": 0.5,
  "save_project": true
}
```

### 3. Splitting a Video into 15-Second Reels

```json
{
  "input_path": "/path/to/Videos/entrevista.mp4",
  "segment_seconds": 15,
  "output_dir": "/path/to/Videos/segmentos",
  "save_project": true
}
```

## Best Practices

- Always supply **absolute paths** (e.g. `/Users/alex/project/file.ext` on macOS/Linux or `C:\Users\alex\project\file.ext` on Windows).
- Existing files are never overwritten unless `overwrite: true` is passed.
- Use `render_frame` when visual confirmation of titles, effects, or color grading is helpful.
- Always surface output file links using `[filename](file:///absolute/path/to/file)`.
