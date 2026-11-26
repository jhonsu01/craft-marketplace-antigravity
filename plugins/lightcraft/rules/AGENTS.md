# LightCraft Integration Rules

When interacting with RAW photography (`DNG`, `CR2`, `CR3`, `ARW`, `NEF`, `RAF`, `RW2`, `ORF`, `PEF`), batch photo developing, Lightroom `.xmp` presets, HDR/panorama merges, photo culling, or the local LightCraft application:

1. **RAW Development & Photography Workflow Priority**:
   - Use `get_photo_info` to inspect camera, lens, exposure settings, capture time, GPS, dimensions, RAW status, and full EXIF/XMP metadata.
   - Use `analyze_photos` to cull photo shoots or bursts by sharpness/focus and highlight/shadow clipping scores, optionally copying the sharpest selects to a target folder.
   - Use `develop_photos` for non-destructive single-photo or batch-folder developing: `auto` tone, white balance, any of the 125 develop sliders, built-in or `.xmp`/`.lrtemplate` presets, profiles, tone curves, crop/straighten, spot healing, and local masks (`linear`, `radial`, `luminance`, `color`, `brush`, `subject`, `sky`, `background`), exporting with custom color space, bit depth, sharpening, and watermarks.
   - Use `merge_photos` to combine exposure brackets into `hdr`, stitch overlapping shots into `panorama`, or build `hdr_panorama` as editable DNG + rendered JPEG/TIFF.
   - Use `convert_photos` for fast batch conversion and resizing to `jpg`, `png`, `tiff`, `webp`, `avif`, or `dng`, and `render_preview` to test trial looks visually before exporting.
   - Use `list_lightcraft_catalog` and `run_lightcraft_commands` to inspect exact slider IDs/ranges, presets, profiles, and automate across LightCraft's 392 engine commands.

2. **File Paths, Normalized Coordinates & Safety**:
   - Always supply **absolute paths** for input photos/folders, preset files, output files, and output directories.
   - Never overwrite existing files unless explicitly requested (`overwrite: true`). Originals are only read in a throwaway catalog — no XMP sidecars or merged files are written next to input photos.
   - Crop boxes, spot-healing coordinates, and mask coordinates are **normalized `0..1` from the top-left corner**.
   - Note: DNG export (`formats: ["dng"]`) requires RAW inputs; use `tiff`, `png`, `avif`, `webp`, or `jpg` when developing non-RAW inputs. Also note that `avif` is write-only in LightCraft's pure-Rust engine (do not pass `.avif` files as inputs to `analyze_photos` or `develop_photos`; pass `input_paths` with RAW/JPEG/PNG/TIFF/WebP instead).
   - When files or folders are created or modified, always surface clickable Markdown links formatted with the `file:///` scheme (using forward slashes) so the user can open them with one click.

3. **Desktop App Interaction**:
   - Headless engine commands run isolated with a temporary library using `lightcraft-cli` without touching the user's personal LightCraft catalog.
   - When the user wants to visually inspect or continue developing in the desktop app, invoke `open_in_lightcraft` with the photo paths (live control port `7980`).
