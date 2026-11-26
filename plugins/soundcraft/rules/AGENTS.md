# SoundCraft Integration Rules

When interacting with audio files, music composition, podcasts, stems, MIDI, `.scraft` DAW sessions, loudness analysis, or the local SoundCraft application:

1. **Audio & DAW Operations Priority**:
   - Use `get_audio_info` to inspect sample rate, bit depth, channels, duration, session track layouts, loudness (`peak_db`, `true_peak_db`, `lufs`), and waveform renders before or after editing.
   - Use `create_session` to build multitrack sessions combining audio files (`at` in seconds, `clip_gain_db`, fades) and MIDI instrument tracks (`subtractive_synth`, `drum_synth`, sampler; notes in quarter-note beats) with insert effects, aux busses/sends, tempo, key, markers, mixdowns, stems, MIDI, and `.scraft` project files.
   - Use `edit_session` to non-destructively modify existing `.scraft` sessions (tempo, meter, key, markers, busses, adding/removing/renaming tracks, changing mixer levels, effects, and sends).
   - Use `export_session` to bounce `.scraft` sessions (single file, list, or folder) to WAV, AIFF, or FLAC mixdowns, stems, and MIDI with optional normalization.
   - Use `process_audio` for AudioSuite-style processing on audio files or folders (trim, normalize, gain, fades, pitch shift in semitones, time stretch, reverse, polarity invert, and insert effects).
   - Use `convert_audio` for batch format, sample-rate, and bit-depth conversions (`wav`, `aiff`, `flac` at 16-bit, 24-bit, or 32-bit float).
   - Use `list_soundcraft_catalog` and `run_soundcraft_commands` to inspect the 30 built-in plugins (and exact parameter IDs/ranges) and automate across SoundCraft's 483 engine commands.

2. **File Paths, Timing Units & Safety**:
   - Always supply **absolute paths** for input audio/MIDI/sessions, output files, and output directories.
   - Never overwrite existing files unless explicitly requested (`overwrite: true`). Inputs are only read; edits write to a new copy.
   - Audio timeline positions (`at`, trims, fades, markers) are in **seconds**; MIDI note `start` and `length` inside instrument clips are in **beats** (quarter notes).
   - When files or folders are created or modified, always surface clickable Markdown links formatted with the `file:///` scheme (using forward slashes) so the user can open them with one click.

3. **Desktop App Interaction**:
   - Headless engine commands run isolated with `soundcraft-cli` without touching open SoundCraft windows or audio hardware.
   - When the user wants to listen, visually inspect, or continue mixing in the desktop app, invoke `open_in_soundcraft` with the `.scraft` path (live control port `7801`).
