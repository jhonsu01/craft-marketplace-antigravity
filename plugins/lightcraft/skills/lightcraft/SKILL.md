---
name: lightcraft
description: Develop RAW photos and batches (auto tone, white balance, 125 sliders, Lightroom .xmp presets, camera profiles, local masks, spot healing), merge HDR and panoramas to DNG, cull bursts by sharpness, and export JPEG, PNG, TIFF, WebP, AVIF, and DNG using the local LightCraft application and CLI engine (392 commands).
---

# LightCraft RAW Photo Developer & Culling Automation

This skill enables full integration with the **LightCraft** Lightroom-class photo developer and headless CLI engine (`lightcraft-cli`) installed on your local computer.

## Available Capabilities & Tools

LightCraft exposes 10 high-level MCP tools:

1. **`develop_photos`**: Non-destructively develop a photo, list of photos, or entire folder using `auto` tone, `white_balance` (`daylight`, `cloudy`, `tungsten`, custom Kelvin, or eyedropper), any of the 125 develop `values` sliders, built-in `preset` or external Lightroom `preset_file` (`.xmp`, `.lrtemplate`, `.lcpreset`), camera/creative `profile`, `black_and_white`, `curve_preset`, `crop`/straighten, `heal` spot removal, and local `masks` (`linear`, `radial`, `luminance`, `color`, `brush`, `subject`, `sky`, `background`). Exports to `jpg`, `png`, `tiff`, `webp`, `avif`, or `dng` (for RAWs) with custom `long_edge`, `quality`, color space (`sRGB`, `Display P3`, `Adobe RGB`, `ProPhoto RGB`, `Rec. 2020`), bit depth, and `watermark`.
2. **`convert_photos`**: Batch convert and resize RAW (`DNG`, `CR2`, `CR3`, `ARW`, `NEF`, `RAF`, `RW2`, `PEF`, `ORF`, `SRW`) and standard images to `jpg`, `png`, `tiff`, `webp`, `avif`, or `dng`.
3. **`render_preview`**: Render a visual preview of a photo (optionally applying trial `values` or presets) without writing permanent exports unless `output_path` is provided.
4. **`get_photo_info`**: Read camera model, lens, ISO, shutter, aperture, capture timestamp, GPS, dimensions, RAW flag, and full EXIF/XMP metadata (`all_metadata: true`).
5. **`merge_photos`**: Merge bracketed exposures into `hdr`, overlapping frames into `panorama`, or `hdr_panorama`, producing an editable `dng` plus optional developed `jpg`/`tiff` in `output_dir`.
6. **`analyze_photos`**: Evaluate sharpness/focus and highlight/shadow clipping across a folder, group bursts, and optionally copy the sharpest selects into `copy_best_to`.
7. **`list_lightcraft_catalog`**: Browse 125 `controls` (with exact IDs and min/max ranges), built-in `presets`, `profiles`, `curves`, `export_presets`, 392 `commands`, and supported `formats`.
8. **`run_lightcraft_commands`**: Execute raw LightCraft engine commands (`develop.set`, `mask.add`, `mask.adjust`, `preset.create`, `photo.rate`) with `$steps[N].field` references in headless mode or live (`live: true`, port `7980`).
9. **`open_in_lightcraft`**: Open photos in the LightCraft desktop application (optionally enabling the live control channel on port `7980`).
10. **`get_lightcraft_status`**: Check platform, `lightcraft-cli` version, command and develop-control counts, executable paths, and live control port status.

## Practical Examples

### 1. Developing a Folder of Photos with Local Sky Mask & Watermark

```json
{
  "input_dir": "/path/to/workspace\\miami_sunset",
  "auto": true,
  "white_balance": { "mode": "daylight" },
  "profile": "lc.vivid",
  "values": {
    "light.highlights": -35,
    "light.shadows": 28,
    "effects.clarity": 15,
    "vignette.amount": -15
  },
  "masks": [
    {
      "kind": "linear",
      "start": [0.5, 0],
      "end": [0.5, 0.45],
      "adjust": { "exposure": -0.4, "dehaze": 15 }
    }
  ],
  "formats": ["jpg", "avif"],
  "long_edge": 1920,
  "quality": 90,
  "watermark": "© Antigravity Studio",
  "output_dir": "/path/to/workspace\\lightcraft_developed"
}
```

### 2. Merging Exposure Brackets into HDR DNG + JPEG

```json
{
  "mode": "hdr",
  "input_dir": "/path/to/Photos/Brackets",
  "deghost": "low",
  "formats": ["dng", "jpg"],
  "long_edge": 2048,
  "output_dir": "/path/to/Photos/HDR_Output"
}
```

## Best Practices

- Always supply **absolute paths** (e.g. `/Users/alex/project/file.ext` on macOS/Linux or `C:\Users\alex\project\file.ext` on Windows).
- Mask coordinates, crop rectangles, and healing spots use **normalized `0..1` coordinates** from the top-left corner.
- Query `list_lightcraft_catalog` (`kind: "controls"` or `"presets"`) whenever you need exact slider names or built-in preset IDs.
- Always surface output file links using `[filename](file:///absolute/path/to/file)`.
