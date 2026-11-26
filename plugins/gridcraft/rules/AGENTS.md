# GridCraft Integration Rules

When interacting with spreadsheets or the local GridCraft application:

1. **Spreadsheet Operations Priority**:
   - Use `get_workbook_info` or `read_workbook` to inspect structure, sheets, tables, and formula calculations before editing.
   - Use `create_workbook` to build rich workbooks with data, live formulas, tables, charts, PivotTables, and formatting.
   - Use `edit_workbook` for targeted cell modifications, find & replace, sorting, row/column operations, and sheet management.
   - Use `convert_workbook` for format conversions (XLSX, CSV, ODS, JSON, HTML, PDF).
   - Use `list_gridcraft_catalog` and `run_gridcraft_commands` for advanced engine automation.

2. **File Paths & Safety**:
   - Always supply **absolute paths** for input files, output files, and output directories.
   - Never overwrite existing files unless explicitly requested (`overwrite: true`). By default, tools generate safe sequential outputs (`_2`, `_3`, etc.).
   - When files are created or modified, always surface clickable Markdown links formatted with the `file:///` scheme (using forward slashes) so the user can open them with one click.

3. **Desktop App Interaction**:
   - Headless engine commands run isolated in memory using `gridcraft-cli`.
   - When the user wants to visually inspect or continue editing in the desktop app, invoke `open_in_gridcraft` with the workbook path.
