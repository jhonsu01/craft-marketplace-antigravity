---
name: designcraft
description: Lay out flyers, posters, brochures, menus, cards, certificates, and book pages, data-merge CSVs, edit .designcraft and InDesign .idml files, and export print-ready PDF (PDF/X-4), PNG, IDML, EPUB, and HTML using the local DesignCraft desktop publishing application and CLI engine (568 commands).
---

# DesignCraft Desktop Publishing & Page Layout Automation

This skill enables full integration with the **DesignCraft** InDesign-class desktop publishing application and headless CLI engine (`designcraft-cli`) installed on your local computer.

## Available Capabilities & Tools

DesignCraft exposes 10 high-level MCP tools:

1. **`create_layout`**: Build single- or multi-page documents (presets like `A4`, `A5`, `Letter` or custom dimensions, facing pages, margins, columns, bleed, background color, and reusable paragraph styles) from items placed per page: text frames (font, style, size, leading, tracking, alignment, multi-column, vertical alignment), placed images (`fill`, `fit`, `stretch`, `center`, rounded corners, drop shadow), shapes (`rect`, `ellipse`, `polygon`, `line` with gradients, strokes, text wrap, rotation), and styled tables. Automatically reports any `overset_text`.
2. **`data_merge`**: Merge a CSV/TSV file or array of `rows` into an existing `.designcraft`/`.idml` template or an inline item layout using `<<Field>>` text placeholders and image `field` bindings — either one page per record (badges, certificates) or multiple records per page (`per_page: true` for address labels and cards).
3. **`export_document`**: Export one document, a list, or an entire folder to PDF (`pdf_standard: "x4"` or `"a2b"`, `include_bleed`, `crop_marks`, `spreads`, `export_pages`), PNG/JPG pages at custom `dpi`, Adobe InDesign `.idml`, reflowable or fixed-layout `epub`, `html`, `booklet` PDF, or full `package` folder.
4. **`edit_document`**: Non-destructively edit `.designcraft` or `.idml` documents — text/GREP `find_replace`, story text replacement, `replace_images` in frames, `replace_font`, adding pages, and placing new items — saving as a new copy.
5. **`get_document_info`**: Inspect page count, items and bounds per page, stories (including overset status), paragraph/character styles, color swatches, fonts (including missing fonts), linked assets (missing or low-DPI), and preflight checks.
6. **`render_pages`**: Render document pages as PNG previews for visual inspection and optionally save them to disk.
7. **`list_designcraft_catalog`**: Browse 568 engine commands (with parameters), page presets, font availability (including bundled `Inter`, `Source Sans 3`, and `Source Serif 4`), and supported formats.
8. **`run_designcraft_commands`**: Execute raw DesignCraft engine commands (`frame.create`, `text.select`, `type.char`, `inspect_document`, `get_story`, `place_image`) with `$steps[N].field` references in headless mode or live against the desktop app (`live: true`, port `7981`).
9. **`open_in_designcraft`**: Open `.designcraft` or `.idml` documents in the DesignCraft desktop app (optionally enabling the live control channel on port `7981`).
10. **`get_designcraft_status`**: Check platform, `designcraft-cli` version, command count, executable paths, and live control port status.

## Practical Examples

### 1. Creating a Two-Page Print-Ready A5 Brochure (PDF/X-4 + IDML + PNG)

```json
{
  "name": "Cafe_Brochure",
  "units": "mm",
  "preset": "A5",
  "page_count": 2,
  "margins": 12,
  "bleed": 3,
  "background": "#FDF6EC",
  "styles": [
    { "name": "Title", "font": "Source Serif 4", "font_style": "Bold", "size": 32, "color": "#FFFFFF", "align": "center" },
    { "name": "Body", "font": "Inter", "size": 10.5, "color": "#2D2A26", "space_after": 4 }
  ],
  "items": [
    { "type": "rect", "x": 0, "y": 0, "width": 148, "height": 42, "gradient": ["#7B2FF7", "#C0661F"] },
    { "type": "text", "x": 12, "y": 10, "width": 124, "height": 22, "text": "DesignCraft Studio", "style": "Title", "vertical_align": "center" },
    { "type": "image", "path": "/path/to/workspace/artwork.png", "x": 12, "y": 50, "width": 124, "height": 70, "corner_radius": 4, "shadow": true },
    { "type": "text", "x": 12, "y": 128, "width": 124, "height": 36, "text": "Editorial typography, print-ready PDF/X-4 preflight, and full Adobe InDesign IDML interchange.", "style": "Body", "columns": 2, "gutter": 5 },
    { "type": "table", "page": 2, "x": 12, "y": 20, "width": 124, "height": 55, "header": true, "header_fill": "#F2B134", "font": "Inter", "size": 10, "rows": [["Edition", "Format", "Bleed"], ["Print Master", "PDF/X-4", "3 mm"], ["Interchange", "InDesign IDML", "3 mm"], ["Digital Book", "EPUB 3", "None"]] }
  ],
  "formats": ["pdf", "png", "idml", "designcraft"],
  "pdf_standard": "x4",
  "include_bleed": true,
  "crop_marks": true,
  "output_dir": "/path/to/workspace"
}
```

### 2. Data-Merging Event Badges from CSV

```json
{
  "csv_path": "/path/to/workspace\\team.csv",
  "units": "mm",
  "width": 90,
  "height": 55,
  "margins": 6,
  "items": [
    { "type": "image", "field": "Photo", "x": 6, "y": 8, "width": 24, "height": 24, "fit": "fill", "corner_radius": 12 },
    { "type": "text", "x": 34, "y": 10, "width": 50, "height": 12, "text": "<<Name>>", "font": "Inter", "font_style": "Bold", "size": 13 },
    { "type": "text", "x": 34, "y": 23, "width": 50, "height": 10, "text": "<<Role>>", "font": "Inter", "size": 9.5, "color": "#555555" }
  ],
  "formats": ["pdf", "designcraft"],
  "name": "VIP_Badges",
  "output_dir": "/path/to/workspace"
}
```

## Best Practices

- Always supply **absolute paths** (e.g. `/Users/alex/project/file.ext` on macOS/Linux or `C:\Users\alex\project\file.ext` on Windows).
- Specify `units` (`"mm"`, `"cm"`, `"in"`, `"pt"`, `"px"`) explicitly when working with physical print sizes; `x` and `y` are measured from the **top-left corner of each page**.
- Check `overset_text` in `create_layout` / `get_document_info` results and enlarge text frames or adjust font size if any text overflows.
- Always surface output file links using `[filename](file:///absolute/path/to/file)`.
