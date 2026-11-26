# EffectCraft Integration Rules

When interacting with motion graphics, visual effects, animated templates, `.ecproj` / `.ectemplate` files, Lottie animations, or the local EffectCraft application:

1. **Motion Graphics & VFX Operations Priority**:
   - Use `get_project_info` or `render_frame` to inspect compositions, layers, missing footage, Essential Graphics template controls, and preview frames before or after rendering.
   - Use `create_motion_graphic` to build animated intros, titles, social clips, and Lottie animations from text, shapes, solids, images, videos, entrance/exit presets (`typewriter`, `pop`, `slide_*`, `fade`, `zoom`, `spin`), keyframes, After Effects-style expressions, and 308 effects.
   - Use `apply_effects` to apply VFX, color grading, trims, speed ramps, and animated title/logo overlays onto existing videos or images (single file or batch folder).
   - Use `use_template` to populate built-in motion templates (`lower-third`, `title-card`, `logo-reveal`, `kinetic-type`, `social-square`, `vertical-story`, `slideshow`, `3d-text-orbit`) or custom `.ectemplate` files.
   - Use `render_project` to export `.ecproj` compositions to H.264 MP4, HEVC, AV1, ProRes (with alpha), WebM, GIF, PNG/JPEG/TIFF/EXR sequences, WAV/AIFF, or Lottie.
   - Use `list_effectcraft_catalog`, `run_effectcraft_script` (ExtendScript/AE-style JS), and `run_effectcraft_commands` for advanced automation across EffectCraft's 766 commands.

2. **File Paths & Safety**:
   - Always supply **absolute paths** for input media, `.ecproj` projects, output files, and output directories.
   - Never overwrite existing files unless explicitly requested (`overwrite: true`). Inputs and `.ecproj` sources are never modified in place.
   - Coordinates are in pixels from the top-left of the composition; times are in seconds; layers in `create_motion_graphic` are ordered **top to bottom**.
   - When files or folders are created or modified, always surface clickable Markdown links formatted with the `file:///` scheme (using forward slashes) so the user can open them with one click.

3. **Desktop App Interaction**:
   - Headless engine commands run isolated with in-memory projects using `effectcraft-cli` without touching open windows.
   - When the user wants to visually inspect or continue editing in the desktop app, invoke `open_in_effectcraft` with the project or media path (live control port `9877`).
