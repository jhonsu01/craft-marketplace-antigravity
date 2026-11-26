# PdfCraft Integration Rules

When interacting with PDF files or the local PdfCraft application:

1. **Document Operations Priority**:
   - Use `get_pdf_info` or `extract_text` to inspect document structure, pages, security, and contents before editing.
   - Use `merge_pdfs`, `split_pdf`, and `extract_pages` for page organization, rearrangement, and extraction.
   - Use `add_content` for watermarks, headers/footers, backgrounds, and annotations.
   - Use `redact_pdf` and `protect_pdf` for security, redaction of sensitive patterns, and permission management.
   - Use `fill_form` to inspect, populate, and flatten interactive PDF forms.
   - Use `convert_pdf` for format conversions (Word, HTML, RTF, images, PDF/A).
   - Use `ocr_pdf` to make scanned documents searchable.
   - Use `optimize_pdf` to compress file sizes and remove unnecessary metadata.

2. **File Paths & Safety**:
   - Always supply **absolute paths** for input files, output files, images, and output directories.
   - Never overwrite existing files unless explicitly requested (`overwrite: true`). By default, tools generate safe sequential outputs.
   - When files are created or modified, always surface clickable Markdown links formatted with the `file:///` scheme (using forward slashes) so the user can open them with one click.

3. **Desktop App Interaction**:
   - Headless engine commands run isolated in memory using `pdfcraft-cli`.
   - When the user wants to visually inspect or continue editing in the desktop app, invoke `open_in_pdfcraft` with the document path.
