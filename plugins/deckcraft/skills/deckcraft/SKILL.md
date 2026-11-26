---
name: deckcraft
description: Create, edit, inspect, and convert PowerPoint (.pptx) and .deckcraft presentations with themes, multi-level bullets, charts, tables, images, speaker notes, transitions, PDF handouts, and slide renders using the local DeckCraft desktop application and CLI engine.
---

# DeckCraft Presentation & Slide Deck Automation

This skill enables full integration with the **DeckCraft** PowerPoint-class presentation application and headless CLI engine (`deckcraft-cli`) installed on your local computer.

## Available Capabilities & Tools

DeckCraft exposes 9 high-level MCP tools:

1. **`create_presentation`**: Build 16:9 or 4:3 presentations from structured `slides` (title, subtitle, multi-level `bullets` in 1 or 2 columns, `image` kept in proportion, `chart`, `table`, custom shapes/text boxes, speaker `notes`, custom background, slide `transition`, `animate_bullets`) or an `outline`. Supports 8 built-in themes (`DeckCraft`, `Harbor`, `Ember`, `Meadow`, `Nocturne`, `Paper`, `Coral Reef`, `Slate`), color/font schemes, `slide_numbers`, and `footer`. Exports `pptx`, `pdf`, `png`, `jpeg`, `deckcraft`, and `outline` alongside visual slide previews.
2. **`edit_presentation`**: Non-destructively modify one `.pptx`/`.deckcraft` file, a list, or a folder — find/replace across titles, body text, shapes, table cells, and footers; add or delete slides; update speaker notes; change theme, color scheme, font scheme, transitions, slide numbers, and footers.
3. **`convert_presentation`**: Convert decks or folders to `pptx`, `pdf` (`pdf_layout`: `"slides"`, `"notes"`, or `"handouts"` with 1–9 slides per page), `deckcraft`, per-slide `png`/`jpeg`, and `outline`.
4. **`get_presentation_info`**: Inspect slides, layouts, shapes (IDs, kinds, bounding boxes, text), tables, charts, speaker notes, transitions, animations, theme, fonts, dimensions, and optional `review: true` spelling/accessibility checks.
5. **`render_slides`**: Render selected slides (e.g. `"1-4"`) as PNG images for visual review and optionally save them to disk.
6. **`list_deckcraft_catalog`**: Browse engine `commands` (with parameters), `themes` (plus color and font schemes), `layouts`, `shapes` presets, `transitions`, `animations`, and `formats`.
7. **`run_deckcraft_commands`**: Execute raw DeckCraft engine commands (`slide.*`, `shape.*`, `text.*`, `format.*`, `design.*`, `transition.*`, `animation.*`, `table.*`, `chart.*`) and tools (`add_slide`, `add_shape`, `insert_chart`, `inspect_slide`) using `$steps[N].field` references in headless mode or live (`live: true`, port `7990`).
8. **`open_in_deckcraft`**: Open `.pptx` or `.deckcraft` presentations in the DeckCraft desktop app (optionally enabling the live control channel on port `7990`).
9. **`get_deckcraft_status`**: Check platform, `deckcraft-cli` version, command count, available themes, executable paths, and live control port status.

## Practical Examples

### 1. Creating an Executive Pitch Deck (PPTX + PDF + PNG + .deckcraft)

```json
{
  "name": "Antigravity_Craft_Suite_Deck",
  "theme": "Harbor",
  "slide_numbers": true,
  "footer": "Craft Ecosystem · 2026",
  "transition": "fade",
  "slides": [
    {
      "title": "Antigravity Craft Suite",
      "subtitle": "10 Local Creative & Productivity Engines Connected via MCP"
    },
    {
      "title": "Architecture Highlights",
      "bullets": [
        "100% local headless execution with zero cloud upload",
        { "text": "Non-destructive file-in / file-out safety", "level": 1 },
        { "text": "Live loopback control channels for desktop apps", "level": 1 },
        "Unified Antigravity skills, rules, and lazy MCP schemas"
      ],
      "notes": "Emphasize local privacy and deterministic execution.",
      "animate_bullets": "fade"
    },
    {
      "title": "Engine Command Growth",
      "bullets": ["Over 5,500 combined native commands across the suite"],
      "chart": {
        "type": "column",
        "categories": ["Word/PDF", "Grid/Deck", "Vector/Photo", "Film/Effect/Sound"],
        "series": [
          { "name": "Commands", "values": [887, 745, 2439, 1910] }
        ],
        "legend": "bottom"
      }
    },
    {
      "title": "Visual Showcase",
      "image": {
        "path": "/path/to/workspace/artwork.png"
      }
    },
    {
      "title": "Ready for Production",
      "layout": "sectionHeader",
      "subtitle": "Questions & Live Demo",
      "background": "#0F172A"
    }
  ],
  "formats": ["pptx", "pdf", "png", "deckcraft"],
  "output_dir": "/path/to/workspace"
}
```

### 2. Exporting 3-per-Page Speaker Handouts PDF

```json
{
  "input_path": "/path/to/workspace\\Antigravity_Craft_Suite_Deck.pptx",
  "formats": ["pdf"],
  "pdf_layout": "handouts",
  "handouts_per_page": 3,
  "output_dir": "/path/to/workspace"
}
```

## Best Practices

- Always supply **absolute paths** (e.g. `/Users/alex/project/file.ext` on macOS/Linux or `C:\Users\alex\project\file.ext` on Windows).
- Standard 16:9 slide coordinates are **`960 × 540` points** from the top-left corner; omit manual coordinates on `image`, `chart`, and `table` to let DeckCraft place them cleanly inside layout placeholders.
- Always surface output file links using `[filename](file:///absolute/path/to/file)`.
