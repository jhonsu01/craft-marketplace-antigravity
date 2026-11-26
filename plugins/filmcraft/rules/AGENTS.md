# FilmCraft Integration Rules

When interacting with video/audio files, timelines (`.fcproj`, FCPXML, OTIO), or the local FilmCraft application:

1. **Video & Timeline Operations Priority**:
   - Use `get_media_info` or `render_frame` to inspect video/audio codecs, duration, resolution, frame rate, and preview frames before or after editing.
   - Use `split_video` and `trim_video` for frame-accurate splitting into segments or trimming time ranges with optional fades.
   - Use `edit_video` to apply 131 video effects (with parameters and keyframes), 18 Lumetri color looks, burned-in titles, speed/reverse changes, and 58 audio effects, optionally saving editable projects (`save_project: true`) or interchange timelines (`otio`, `fcpxml`, `xml`, `edl`, `aaf`).
   - Use `concat_videos` to join clips, still images, and audio tracks with any of 112 video transitions.
   - Use `convert_media` to transcode between H.264 MP4, ProRes, DNxHR, MXF, animated GIF, image sequences, or extract WAV/AIFF audio using 45 export presets.
   - Use `list_catalog` and `run_commands` for advanced engine automation across FilmCraft's 660+ commands.

2. **File Paths & Safety**:
   - Always supply **absolute paths** for input files, output files, and output directories.
   - Never overwrite existing files unless explicitly requested (`overwrite: true`). Inputs are never modified in place.
   - When files or folders are created or modified, always surface clickable Markdown links formatted with the `file:///` scheme (using forward slashes) so the user can open them with one click.

3. **Desktop App Interaction**:
   - Headless engine commands run isolated in temporary workspaces using `filmcraft-cli` without touching open windows.
   - When the user wants to visually inspect or continue editing in the desktop app, invoke `open_in_filmcraft` with the project or media path (live control port `9876`).
