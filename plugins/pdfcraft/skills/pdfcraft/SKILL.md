---
name: pdfcraft
description: Read, split, merge, organize, watermark, protect, redact, fill, sign, convert, compress and OCR PDFs with the local PdfCraft desktop application and CLI engine. Use when the user wants to inspect PDFs, combine or split files, add watermarks, header/footers, redact sensitive information, fill forms, or convert PDFs to Word or images.
---

# PdfCraft PDF Automation & Manipulation

This skill enables full integration with the **PdfCraft** desktop application and headless CLI engine (`pdfcraft-cli`) installed on your local computer.

## Available Capabilities & Tools

PdfCraft exposes 21 high-level MCP tools:

1. **`get_pdf_info`**: Inspect pages, dimensions, metadata, security, form fields, fonts, bookmarks, and digital signatures.
2. **`extract_text`**: Extract plain text from all or specific pages in reading order, optionally saving to a `.txt` file.
3. **`render_pages`**: Render specific pages as PNG, JPEG, or TIFF images with previews.
4. **`split_pdf`**: Split PDF every N pages, before specific pages, by bookmarks, or by target file size.
5. **`merge_pdfs`**: Combine multiple PDFs with flexible page ranges (e.g. `"1-3, 6"`).
6. **`extract_pages`**: Extract selected pages into a new PDF or separate into single-page files.
7. **`edit_pages`**: Insert blank or file pages, rotate, move, delete, crop, set page labels, and edit metadata.
8. **`create_pdf`**: Generate a new PDF from text, images, or blank pages.
9. **`add_content`**: Add text or image watermarks, headers/footers (page numbers, dates, Bates numbering), backgrounds, text boxes, and links.
10. **`protect_pdf`**: Encrypt with open/owner passwords (AES-256), restrict permissions (printing, copying, modifying), or remove protection.
11. **`redact_pdf`**: Permanently redact text, patterns (emails, phone numbers, SSNs, credit cards, dates), specific rectangular areas, or entire pages.
12. **`fill_form`**: Detect, list, populate, and flatten interactive PDF form fields (AcroForms).
13. **`sign_pdf`**: Digitally sign PDF using a PKCS#12 (.p12/.pfx) digital ID or generate a self-signed certificate.
14. **`convert_pdf`**: Convert PDF to Word (DOCX), HTML, RTF, TXT, images (PNG, JPEG, TIFF), or archive formats (PDF/A-2b, PDF/A-3b).
15. **`optimize_pdf`**: Reduce file size through stream recompression, subsetting, and stripping hidden metadata.
16. **`ocr_pdf`**: Perform OCR on scanned PDFs to generate searchable text layers.
17. **`compare_pdfs`**: Compare two PDF versions and generate a difference report or marked copy.
18. **`list_pdf_tools`**: List all 131 low-level engine tools and their parameter schemas.
19. **`run_pdf_tools`**: Execute multiple low-level engine commands in a single orchestrated session.
20. **`open_in_pdfcraft`**: Launch the PdfCraft desktop GUI to view or edit the document interactively.
21. **`get_pdfcraft_status`**: Verify installation paths, CLI version, and OCR model availability.

## Practical Examples

### 1. Merging PDFs with Custom Page Ranges & Header

```json
{
  "inputs": [
    { "path": "/path/to/Documentos/parte1.pdf", "pages": "1-5" },
    { "path": "/path/to/Documentos/parte2.pdf", "pages": "2, 4-6" }
  ],
  "output_path": "/path/to/Documentos/documento_unificado.pdf",
  "header_footer": {
    "header_right": "CONFIDENCIAL",
    "footer_center": "<<Page 1 of n>>"
  }
}
```

### 2. Redacting Sensitive Data & Adding a Watermark

```json
{
  "input_path": "/path/to/Contratos/acuerdo.pdf",
  "patterns": ["email", "phone"],
  "watermark": {
    "text": "COPIA CONTROLADA",
    "opacity": 0.2
  },
  "output_dir": "/path/to/Contratos"
}
```

### 3. Converting Scanned PDF to Word with OCR

```json
{
  "input_path": "/path/to/Escaneos/factura.pdf",
  "ocr": true,
  "to": "docx",
  "output_dir": "/path/to/Escaneos"
}
```

## Best Practices

- Always supply **absolute paths** (e.g. `/Users/alex/project/file.ext` on macOS/Linux or `C:\Users\alex\project\file.ext` on Windows).
- Coordinates and dimensions are specified in **points** (1/72 inch) starting from the top-left corner of the page.
- Always provide clickable Markdown links formatted as `[filename](file:///absolute/path/to/file)` when returning generated files.
