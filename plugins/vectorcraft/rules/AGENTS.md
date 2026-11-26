# VectorCraft Integration Rules

When interacting with vector graphics, illustrations, or the local VectorCraft application:

1. **Vector Operations Priority**:
   - Use `vectorize_image` to trace bitmap images (PNG, JPG, WebP) into scalable vector formats (SVG, PDF, EPS).
   - Use `create_design` to generate vector compositions with shapes, text, placed images, and styled charts.
   - Use `edit_vector` for recoloring, applying effects (drop shadows, blur, glow), transforming objects, or outlining fonts.
   - Use `convert_vector` for conversions across 20 formats (SVG, PDF, EPS, DXF, EMF, PNG, JPEG, PSD).
   - Use `get_vector_info` and `render_preview` to inspect artboards, color modes, and preview rendering before or after editing.
   - Use `list_vector_catalog` and `run_vector_commands` for advanced engine tools and pathfinder operations.

2. **File Paths & Safety**:
   - Always supply **absolute paths** for input files, output files, images, and output directories.
   - Never overwrite existing files unless explicitly requested (`overwrite: true`). By default, tools generate safe sequential outputs (`_2`, `_3`, etc.).
   - When files are created or modified, always surface clickable Markdown links formatted with the `file:///` scheme (using forward slashes) so the user can open them with one click.

3. **Desktop App Interaction**:
   - Headless engine commands run isolated in memory using `vectorcraft-cli`.
   - When the user wants to visually inspect or continue editing in the desktop app, invoke `open_in_vectorcraft` with the artwork path.
