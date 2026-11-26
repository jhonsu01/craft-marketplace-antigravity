---
name: gridcraft
description: Build, edit, analyze, and convert spreadsheets (XLSX, CSV, ODS, JSON, HTML, PDF) with the local GridCraft desktop application and CLI engine. Use when the user wants to create financial models, budget sheets, data tables, evaluate formulas, generate charts, or inspect workbooks.
---

# GridCraft Spreadsheet Automation & Analysis

This skill enables full integration with the **GridCraft** desktop application and headless CLI engine (`gridcraft-cli`) installed on your local computer.

## Available Capabilities & Tools

GridCraft exposes 9 high-level MCP tools:

1. **`create_workbook`**: Build workbooks from scratch with multiple sheets, live Excel formulas (513 functions, dynamic arrays), styled tables with filters, charts (17 types), PivotTables, conditional formatting, data validation dropdowns, notes, frozen panes, and print setup.
2. **`edit_workbook`**: Modify existing workbooks (XLSX, ODS, CSV): write cells/formulas, find & replace, insert/delete rows and columns, sort, remove duplicates, add/rename/delete sheets, and update charts.
3. **`read_workbook`**: Read computed values, raw formulas, or formatted display text from any cell range. Can evaluate formulas on the fly without modifying the original file.
4. **`convert_workbook`**: Convert files between supported input formats (XLSX, XLSM, XLS, XLSB, ODS, CSV, TSV, JSON) and output formats (XLSX, CSV, TSV, JSON, HTML, PDF).
5. **`get_workbook_info`**: Inspect workbook structure: sheet names, table definitions, charts, named ranges, previews of first rows, and formula syntax errors.
6. **`list_gridcraft_catalog`**: List all 385 engine commands, 515 worksheet functions, chart types, and number formatting codes.
7. **`run_gridcraft_commands`**: Execute raw GridCraft engine commands in headless or live GUI mode.
8. **`open_in_gridcraft`**: Launch the GridCraft desktop application to view or edit the workbook interactively.
9. **`get_gridcraft_status`**: Verify installation paths, CLI version, and engine status.

## Practical Examples

### 1. Creating a Financial Workbook with Formulas & Summary

```json
{
  "name": "Presupuesto_Mensual",
  "sheets": [
    {
      "name": "Ingresos",
      "data": [
        ["Concepto", "Categoría", "Monto"],
        ["Sueldo", "Fijo", 3500],
        ["Consultoría", "Variable", 1200],
        ["Rendimientos", "Inversión", 150]
      ],
      "tables": [
        { "name": "TablaIngresos", "range": "A1:C4", "total_row": true }
      ]
    },
    {
      "name": "Resumen",
      "data": [
        ["Métrica", "Total"],
        ["Total Ingresos", "=SUM(Ingresos!C2:C4)"],
        ["Promedio", "=AVERAGE(Ingresos!C2:C4)"]
      ]
    }
  ],
  "formats": ["xlsx", "pdf"],
  "output_dir": "/path/to/workspace"
}
```

### 2. Reading & Evaluating Formulas in a Workbook

```json
{
  "input_path": "/path/to/Datos/ventas.xlsx",
  "sheet": "Ventas",
  "range": "A1:D10",
  "evaluate": ["SUM(D2:D10)", "AVERAGE(D2:D10)"]
}
```

### 3. Converting Spreadsheets

```json
{
  "input_path": "/path/to/Datos/reporte.xlsx",
  "to": ["csv", "pdf", "html"],
  "output_dir": "/path/to/Datos/exportados"
}
```

## Best Practices

- Always supply **absolute paths** (e.g. `/Users/alex/project/file.ext` on macOS/Linux or `C:\Users\alex\project\file.ext` on Windows).
- Formula names should follow standard Excel syntax (e.g. `=SUM(...)`, `=SUMIFS(...)`, `=VLOOKUP(...)`).
- When returning generated files to the user, always provide the file link as `[filename](file:///absolute/path/to/file)`.
