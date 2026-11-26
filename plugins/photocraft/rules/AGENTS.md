# PhotoCraft Integration Rules

When interacting with raster images, photos, layered PSD/.pcraft files, or the local PhotoCraft application:

1. **Image Operations Priority**:
   - Use `get_image_info` or `render_preview` to inspect image dimensions, color mode, bit depth, resolution, and layer trees before or after editing.
   - Use `edit_image` for photo manipulation pipelines (resize, crop, canvas size, auto tone/contrast, 21 adjustments, Camera Raw, 123 filters, selections, text, shapes, placed logos, and layer styles), either on single files or batch folders.
   - Use `remove_background` to cut out subjects to transparent PNG/WebP, trimmed bounds, solid background colors, or editable masked PSDs.
   - Use `create_image` to compose new banners, social posts, thumbnails, and collages from fill/gradient layers, shapes, styled text, and placed images.
   - Use `convert_image` for single or batch conversions across PSD, PSB, TIFF, PNG, JPEG, WebP, GIF, BMP, TGA, ICO, QOI, OpenEXR, HDR, and `.pcraft`.
   - Use `list_photo_catalog` and `run_photo_commands` for advanced headless or live engine automation across PhotoCraft's 1000+ commands.

2. **File Paths & Safety**:
   - Always supply **absolute paths** for input files, output files, placed images, and output directories.
   - Never overwrite existing files unless explicitly requested (`overwrite: true`). By default, tools generate safe sequential outputs (`_2`, `_3`, etc.).
   - Apply pixel adjustments and filters before adding text or vector shape layers (or insert `{"op": "flatten"}` beforehand), since filters require an active pixel layer.
   - When files are created or modified, always surface clickable Markdown links formatted with the `file:///` scheme (using forward slashes) so the user can open them with one click.

3. **Desktop App Interaction**:
   - Headless engine commands run isolated on private copies using `photocraft-cli` without touching open windows.
   - When the user wants to visually inspect or continue editing in the desktop app, invoke `open_in_photocraft` with the image path.
