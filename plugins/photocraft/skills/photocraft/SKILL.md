---
name: photocraft
description: Edit photos (resize, crop, 21 adjustments, Camera Raw, 123 filters, remove background, text, shapes, layer styles), create raster/layered designs, and convert between PSD, TIFF, PNG, JPEG, WebP, EXR, and .pcraft using the local PhotoCraft desktop application and CLI engine.
---

# PhotoCraft Photo Editing & Layered Design Automation

This skill enables full integration with the **PhotoCraft** desktop application and headless CLI engine (`photocraft-cli`) installed on your local computer.

## Available Capabilities & Tools

PhotoCraft exposes 10 high-level MCP tools:

1. **`edit_image`**: Run ordered editing operations on a single image, list of images, or an entire folder: resize, crop, canvas size, rotate/flip, trim, auto tone/contrast/color, 21 adjustments (levels, curves, exposure, hue/saturation, black & white, vibrance...) as pixels or non-destructive adjustment layers, Camera Raw, 123 filters, selections, fills, styled text, shapes, placed images/watermarks, and layer styles.
2. **`create_image`**: Build new designs (social posts, banners, thumbnails, collages) of any size with solid/gradient backgrounds, shapes, styled text, placed images, and layer effects (drop shadow, stroke, outer/inner glow, bevel), exporting to PNG, JPEG, WebP, PSD, or `.pcraft`.
3. **`remove_background`**: Cut out the main subject into a transparent PNG/WebP, optionally trimmed to bounds, placed over a solid background color, or saved as a PSD with an editable layer mask. Supports batch processing.
4. **`convert_image`**: Convert single files or entire folders across PSD, PSB, layered/flat TIFF, PNG, JPEG, WebP, GIF, BMP, TGA, ICO, QOI, PPM, OpenEXR, HDR, and `.pcraft` (also reads HEIC/HEIF, SVG, and Affinity files), with optional max dimension scaling.
5. **`get_image_info`**: Inspect pixel dimensions, color mode, bit depth, DPI resolution, full layer hierarchy (text content, fonts, shapes, masks, styles), and import warnings.
6. **`render_preview`**: Render any image or multi-layer PSD/`.pcraft` document to PNG for visual inspection.
7. **`list_photo_catalog`**: Browse PhotoCraft's 1009 engine commands, 123 filters, 21 adjustments, 10 layer styles, presets, and supported file formats with their exact parameters.
8. **`run_photo_commands`**: Execute raw PhotoCraft engine commands sequentially in a session (supporting `$steps[N].layer` references), either headless or against a live PhotoCraft window (`live: true`, port 7878).
9. **`open_in_photocraft`**: Launch the PhotoCraft desktop application to view or edit files interactively (optionally enabling the live control channel).
10. **`get_photocraft_status`**: Check installation paths, `photocraft-cli` version, available command count, and live control port status.

## Practical Examples

### 1. Editing a Photo & Exporting to JPEG + Layered PSD

```json
{
  "input_path": "/path/to/Fotos/producto.jpg",
  "operations": [
    { "op": "resize", "width": 1600 },
    { "op": "auto", "kind": "contrast" },
    { "op": "camera_raw", "params": { "vibrance": 25, "clarity": 15 } },
    { "op": "filter", "id": "sharpen.unsharpMask", "params": { "amount": 60, "radius": 1.2 } },
    {
      "op": "text",
      "text": "Colección 2026",
      "x": 800,
      "y": 1000,
      "size": 72,
      "color": "#ffffff",
      "align": "center",
      "effects": [{ "kind": "dropShadow", "distance": 6, "size": 10 }]
    }
  ],
  "formats": ["jpg", "psd"],
  "quality": 88,
  "output_dir": "/path/to/Fotos/editadas"
}
```

### 2. Removing Background & Placing on White

```json
{
  "input_path": "/path/to/Fotos/retrato.jpg",
  "background_color": "#FFFFFF",
  "trim": true,
  "formats": ["png", "psd"],
  "output_dir": "/path/to/Fotos/recortes"
}
```

### 3. Creating a Social Media Banner with Layers

```json
{
  "name": "Banner_Lanzamiento",
  "width": 1200,
  "height": 630,
  "background": "#0F172A",
  "operations": [
    {
      "op": "fill_layer",
      "gradient": {
        "colors": ["#1E1B4B", "#312E81", "#0F172A"],
        "angle": 135
      }
    },
    {
      "op": "shape",
      "kind": "rounded_rect",
      "x": 80,
      "y": 80,
      "width": 1040,
      "height": 470,
      "fill": "#1E293B",
      "radius": 24,
      "opacity": 80
    },
    {
      "op": "text",
      "text": "PhotoCraft en Antigravity",
      "x": 600,
      "y": 290,
      "size": 64,
      "color": "#38BDF8",
      "align": "center",
      "effects": [{ "kind": "dropShadow", "distance": 4, "size": 12 }]
    }
  ],
  "formats": ["png", "psd"],
  "output_dir": "/path/to/workspace"
}
```

## Best Practices

- Always supply **absolute paths** (e.g. `/Users/alex/project/file.ext` on macOS/Linux or `C:\Users\alex\project\file.ext` on Windows).
- Coordinates are in **pixels from the top-left corner**.
- Pixel filters and adjustments require an active pixel layer: apply them **before** adding text/shape layers, or add `{"op": "flatten"}` first.
- When returning generated files to the user, always provide clickable links formatted as `[filename](file:///absolute/path/to/file)`.
