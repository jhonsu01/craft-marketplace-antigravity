# DesignCraft Integration Rules

When interacting with desktop publishing layouts, print-ready PDFs (PDF/X-4), brochures, flyers, badges, data merge, `.designcraft` or Adobe InDesign `.idml` files, or the local DesignCraft application:

1. **Page Layout & Desktop Publishing Priority**:
   - Use `get_document_info` or `render_pages` to inspect pages, frames, stories, overset text, paragraph styles, swatches, fonts, linked images, and preflight issues before or after editing.
   - Use `create_layout` to compose multi-page flyers, brochures, posters, menus, certificates, and books with custom units (`mm`, `cm`, `in`, `pt`, `px`), margins, columns, bleed, paragraph styles, text frames, placed images, shapes, lines, and tables. Always check `overset_text` in the response so no copy is clipped.
   - Use `data_merge` to populate templates or item layouts from CSV/TSV files or row arrays (`<<Field>>` text and image placeholders), either one page per record (badges, certificates) or multiple records per page (`per_page: true` for labels/cards).
   - Use `edit_document` for non-destructive find/replace (including GREP), story updates, font replacements, frame image swaps, and adding pages/items to existing `.designcraft` or `.idml` documents.
   - Use `export_document` to convert single files or entire folders to print-ready PDF (`pdf_standard: "x4"` or `"a2b"`, `include_bleed`, `crop_marks`), PNG/JPG pages, InDesign `.idml`, reflowable/fixed EPUB, HTML, booklet PDF, or packaged archives.
   - Use `list_designcraft_catalog` and `run_designcraft_commands` for advanced automation across DesignCraft's 568 commands.

2. **File Paths, Units & Safety**:
   - Always supply **absolute paths** for input documents, CSVs, placed images, output files, and output directories.
   - Never overwrite existing files unless explicitly requested (`overwrite: true`). Original documents, images, and CSVs are only read; edits write to a new copy.
   - Sizes default to `pt` unless `units` specifies `mm`, `cm`, `in`, or `px`; coordinates (`x`, `y`) are measured from the **top-left corner of each page**. Bundled fonts (`Inter`, `Source Sans 3`, `Source Serif 4`) are guaranteed available across systems.
   - When files or folders are created or modified, always surface clickable Markdown links formatted with the `file:///` scheme (using forward slashes) so the user can open them with one click.

3. **Desktop App Interaction**:
   - Headless engine commands run isolated with in-memory documents using `designcraft-cli` without touching open windows.
   - When the user wants to visually inspect or continue editing in the desktop app, invoke `open_in_designcraft` with the document path (live control port `7981`).
