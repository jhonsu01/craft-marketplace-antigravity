---
name: vectorcraft
description: Vectorize images, convert between 20 vector and raster formats (SVG, PDF, AI, EPS, DXF, PNG, JPEG, PSD), and create artwork with shapes, text, charts, and effects using the local VectorCraft desktop application and CLI engine.
---

# VectorCraft Vector Graphics Automation & Design

This skill enables full integration with the **VectorCraft** desktop application and headless CLI engine (`vectorcraft-cli`) installed on your local computer.

## Available Capabilities & Tools

VectorCraft exposes 10 high-level MCP tools:

1. **`vectorize_image`**: Trace bitmap images (PNG, JPEG, WebP, TIFF) into clean vector graphics (SVG, PDF, EPS) with presets (`logo`, `photo`, `lineart`, `silhouette`) or custom thresholds and color limits.
2. **`create_design`**: Create vector artwork from scratch with artboards, basic shapes (rectangles, ellipses, polygons, stars), SVG path definitions, styled text, placed images, and vector charts (column, bar, line, area, pie, radar) with live effects (drop shadows, glow, blur, warp).
3. **`edit_vector`**: Modify existing vector files: global recoloring, color reduction, spatial transformations (scale, rotate, translate), live vector effects, outlining text, inserting elements, or fitting artboards.
4. **`convert_vector`**: Convert files across 20 formats: read SVG, PDF, AI, EPS, DXF, EMF, WMF, .vectorcraft; export SVG, PDF, EPS, DXF, EMF, WMF, PNG, JPEG, WebP, GIF, TIFF, BMP, TGA, and layered PSD.
5. **`get_vector_info`**: Inspect artboard dimensions, color space (RGB/CMYK), object count breakdown (paths, shapes, text, images), fonts used, and metadata.
6. **`render_preview`**: Render any artboard to high-resolution PNG for quick visual inspection.
7. **`list_vector_catalog`**: List all 685 engine commands, 132 vector effects, trace presets, artboard presets, and supported formats.
8. **`run_vector_commands`**: Execute raw VectorCraft engine commands (pathfinder union/intersect/subtract, transformations) in headless or live GUI mode.
9. **`open_in_vectorcraft`**: Launch the VectorCraft desktop application to view or edit the vector file interactively.
10. **`get_vectorcraft_status`**: Verify installation paths, CLI version, and engine status.

## Practical Examples

### 1. Vectorizing a Logo to SVG & PDF

```json
{
  "input_path": "/path/to/Diseños\\logo.png",
  "preset": "logo",
  "drop_white": true,
  "max_colors": 4,
  "formats": ["svg", "pdf"],
  "output_dir": "/path/to/Diseños\\vectorizados"
}
```

### 2. Creating an Infographic Header with Shapes and Text

```json
{
  "name": "Banner_Tecnologia",
  "width": 1200,
  "height": 400,
  "background": "#0F172A",
  "elements": [
    {
      "type": "rectangle",
      "x": 50, "y": 50, "width": 1100, "height": 300,
      "fill": "#1E293B", "radius": 16
    },
    {
      "type": "text",
      "x": 100, "y": 150,
      "text": "Ecosistema Antigravity 2026",
      "size": 42, "color": "#38BDF8"
    },
    {
      "type": "text",
      "x": 100, "y": 210,
      "text": "WordCraft · PdfCraft · GridCraft · VectorCraft",
      "size": 24, "color": "#94A3B8"
    }
  ],
  "formats": ["svg", "png"],
  "output_dir": "/path/to/workspace"
}
```

### 3. Converting AI/EPS to SVG & DXF

```json
{
  "input_path": "/path/to/Diseños\\plano_tecnico.eps",
  "to": ["svg", "dxf", "pdf"],
  "output_dir": "/path/to/Diseños\\exportados"
}
```

## Best Practices

- Always supply **absolute paths** (e.g. `/Users/alex/project/file.ext` on macOS/Linux or `C:\Users\alex\project\file.ext` on Windows).
- Use `render_preview` or export to `png` alongside `svg` when visual confirmation is helpful.
- When returning generated files to the user, always provide the file link as `[filename](file:///absolute/path/to/file)`.
