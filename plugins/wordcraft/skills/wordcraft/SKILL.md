---
name: wordcraft
description: Create, edit, mail-merge, convert, and inspect documents (DOCX, PDF, ODT, RTF, HTML, Markdown, LaTeX) with the local WordCraft desktop application and CLI engine. Use when the user wants to generate reports, letters, or resumes, convert document formats, edit text with track changes and comments, or open documents in WordCraft.
---

# WordCraft Document Automation & Editing

This skill enables full integration with the **WordCraft** desktop application and headless CLI engine installed on your local computer.

## Available Capabilities & Tools

WordCraft exposes 11 high-level MCP tools:

1. **`create_document`**: Create a new document (blank or from template: `blank`, `letter`, `resume`, `report`, `sample`) composed of structured blocks:
   - `heading`: `level` (1-9), `text`
   - `paragraph`: `text`, formatting (`bold`, `italic`, `underline`, `strikethrough`, `color`, `font`, `size`, `align`, `style`)
   - `bullets` / `numbered`: list of string `items`
   - `table`: `caption`, `rows` (2D array of strings), header row styling
   - `image`: `path` (absolute path to image file), `width`, `caption`, `alt`
   - `toc`: `levels` (e.g. 2 or 3)
   - `page_break`: breaks to a new page
   - `footnote`: footnote reference and text
   - Page setup: `page_size` (`A4`, `Letter`, etc.), `margins` (`normal`, `narrow`, `wide`), `orientation` (`portrait`, `landscape`), `header`, `footer`, `page_numbers` (`top`, `bottom`), `formats` (`docx`, `pdf`, `odt`, `rtf`, etc.).

2. **`edit_document`**: Modify existing documents safely:
   - Find and replace with case sensitivity, whole-word matching, wildcards.
   - Add comments attached to specific text ranges.
   - Track changes (`track_changes: true`) so all edits can be reviewed.
   - Accept or reject revisions.
   - Append or prepend blocks.
   - Strip personal information / metadata.

3. **`convert_document`**: Convert files between supported formats:
   - Input: DOCX, DOC, DOTX, DOCM, ODT, RTF, Markdown, LaTeX, HTML, TXT, JSON.
   - Output: DOCX, PDF, ODT, RTF, HTML, Markdown, LaTeX, TXT, PNG page images.
   - Option to include or bake in revision marks / comments into exported PDFs.

4. **`mail_merge`**: Generate personalized letters and documents:
   - Data source: CSV, TSV, XLSX, ODS.
   - Template: existing document with merge fields or body text with `{{Field}}` placeholders.
   - Output: single combined document or individual files.

5. **`get_document_info`**: Inspect page count, word count, styles, headings, tables, images, comments, and tracked revisions.

6. **`extract_text`**: Extract plain text from any supported document format.

7. **`render_pages`**: Render specific pages as PNG images for visual inspection.

8. **`open_in_wordcraft`**: Launch the WordCraft desktop application to view or edit the document interactively.

9. **`list_wordcraft_catalog`**: List all 615 internal commands, styles, and templates.

10. **`run_wordcraft_commands`**: Execute raw engine commands in headless or live mode.

11. **`get_wordcraft_status`**: Check installation directory, CLI version, and engine status.

## Practical Examples

### 1. Creating a Professional Report

```json
{
  "name": "Informe_Trimestral",
  "template": "blank",
  "page_size": "Letter",
  "margins": "normal",
  "header": "Confidencial - Reporte Financiero",
  "page_numbers": "bottom",
  "title": "Informe Q4",
  "author": "Equipo de Finanzas",
  "blocks": [
    { "type": "paragraph", "text": "Informe Financiero Q4", "style": "Title" },
    { "type": "toc", "levels": 2 },
    { "type": "heading", "text": "Resumen Ejecutivo", "level": 1 },
    { "type": "paragraph", "text": "El rendimiento superó las proyecciones en un 15%." },
    { "type": "heading", "text": "Resultados por Región", "level": 1 },
    {
      "type": "table",
      "caption": "Métricas Q4",
      "rows": [
        ["Región", "Objetivo", "Logrado"],
        ["Norte", "$100,000", "$115,000"],
        ["Sur", "$80,000", "$92,000"]
      ]
    }
  ],
  "formats": ["docx", "pdf"],
  "output_dir": "/path/to/workspace"
}
```

### 2. Search & Replace with Track Changes

```json
{
  "input_path": "/path/to/Contratos/contrato.docx",
  "track_changes": true,
  "find_replace": [
    {
      "find": "Empresa A",
      "replace": "Empresa B",
      "comment": "Actualización de razón social acordada"
    }
  ],
  "output_dir": "/path/to/Contratos"
}
```

### 3. Converting Documents

```json
{
  "input_path": "/path/to/Notas/documento.md",
  "to": ["docx", "pdf"],
  "output_dir": "/path/to/Notas"
}
```

## Best Practices

- Always supply **absolute paths** (e.g. `/Users/alex/project/file.ext` on macOS/Linux or `C:\Users\alex\project\file.ext` on Windows).
- When returning generated files to the user, always provide the file link as `[filename](file:///absolute/path/to/file)`.
