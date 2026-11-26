# WordCraft Integration Rules

When interacting with documents or the local WordCraft application:

1. **Document Operations Priority**:
   - Use `create_document` to author new documents (letters, reports, resumes) with rich block structures (headings, paragraphs, lists, tables, images, table of contents, footnotes).
   - Use `edit_document` for targeted modifications, search & replace, adding comments, or tracking changes.
   - Use `convert_document` for format conversions between DOCX, PDF, ODT, RTF, HTML, Markdown, LaTeX, and TXT.
   - Use `mail_merge` for templated documents combined with spreadsheets (CSV, XLSX, ODS).
   - Use `get_document_info` or `extract_text` to inspect document structure and contents before editing.

2. **File Paths & Safety**:
   - Always supply **absolute paths** for input files, output files, images, and directories.
   - Never overwrite existing files unless the user explicitly requests it (`overwrite: true`). By default, WordCraft tools automatically append `_2`, `_3`, etc., if an output file exists.
   - When files are created or modified, always surface clickable Markdown links formatted with the `file:///` scheme (using forward slashes) so the user can open them with one click.

3. **Desktop App Interaction**:
   - Headless engine commands run isolated in memory without opening the graphical UI.
   - When the user wants to visually inspect or continue editing in the desktop app, invoke `open_in_wordcraft` with the document path.
