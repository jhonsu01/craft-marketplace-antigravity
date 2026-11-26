# DeckCraft Integration Rules

When interacting with slide decks, PowerPoint files (`.pptx`, `.pptm`, `.potx`), `.deckcraft` presentations, or the local DeckCraft application:

1. **Presentation & Slide Operations Priority**:
   - Use `get_presentation_info` or `render_slides` to inspect slide count, layouts, shapes, tables, charts, speaker notes, transitions, animations, themes, and optional spelling/accessibility reviews before or after editing.
   - Use `create_presentation` to build structured decks from slide definitions (titles, multi-level bullets, proportional images, charts, tables, custom shapes, speaker notes, transitions, bullet animations, themes, slide numbers, and footers) or text outlines.
   - Use `edit_presentation` for non-destructive find & replace across text/tables/footers, inserting or deleting slides, updating speaker notes, and changing themes or color/font schemes.
   - Use `convert_presentation` to export single decks or batch folders to `.pptx`, `.pdf` (`slides`, `notes`, or `handouts` 1–9 per page), `.deckcraft`, per-slide `png`/`jpeg`, or text `outline`.
   - Use `list_deckcraft_catalog` and `run_deckcraft_commands` for advanced engine automation across DeckCraft's commands, themes, layouts, shapes, transitions, and animations.

2. **File Paths, Slide Coordinates & Safety**:
   - Always supply **absolute paths** for input decks, placed images, output files, and output directories.
   - Never overwrite existing files unless explicitly requested (`overwrite: true`). Inputs are only read; edits write to a new copy.
   - Slide coordinates are in **points** (`960 × 540 pt` for standard 16:9 slides); images, charts, and tables without an explicit bounding box automatically fill the free content placeholder area proportionally.
   - When files or folders are created or modified, always surface clickable Markdown links formatted with the `file:///` scheme (using forward slashes) so the user can open them with one click.

3. **Desktop App Interaction**:
   - Headless engine commands run isolated with `deckcraft-cli` without touching open windows.
   - When the user wants to present, visually inspect, or continue editing in the desktop app, invoke `open_in_deckcraft` with the presentation path (live control port `7990`).
