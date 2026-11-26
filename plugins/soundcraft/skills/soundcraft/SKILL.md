---
name: soundcraft
description: Compose multitrack music and audio sessions, program synths and drums in MIDI beats, mix with 30 built-in effects and aux busses, measure LUFS/true peak loudness, process/convert audio (WAV, FLAC, AIFF), and export stems, MIDI, and .scraft sessions using the local SoundCraft DAW and CLI engine (483 commands).
---

# SoundCraft Digital Audio Workstation (DAW) Automation

This skill enables full integration with the **SoundCraft** Pro Tools-class digital audio workstation and headless CLI engine (`soundcraft-cli`) installed on your local computer.

## Available Capabilities & Tools

SoundCraft exposes 10 high-level MCP tools:

1. **`create_session`**: Build complete multitrack sessions with audio tracks (files placed at seconds, clip gain, fades), MIDI instrument tracks (`subtractive_synth`, `drum_synth`, or sampler with notes in beats and bar loops), MIDI file imports, mixer controls (`volume_db`, `pan`, `mute`, `solo`), insert effects, aux busses and sends, tempo, meter, key, and markers. Exports mixdowns (`wav`, `flac`, `aiff`), `stems`, `mid`, and editable `.scraft` sessions alongside integrated LUFS, peak dB, and a visual waveform preview.
2. **`edit_session`**: Non-destructively update an existing `.scraft` session — change tempo, meter, key, markers, busses, add or remove tracks, rename tracks, or adjust volume, pan, effects, and sends — saving a new `.scraft` copy and mixdown.
3. **`export_session`**: Bounce one `.scraft` session, a list, or an entire folder to `wav`, `aiff`, or `flac` mixdowns (custom time range, normalization, bit depth), `stems`, and `mid` with loudness metrics.
4. **`process_audio`**: Process one audio file, a list, or a folder with trim, `normalize_db`, gain, `fade_in`/`fade_out`, `pitch_semitones` (pitch shift), `stretch` (time stretch without changing pitch), varispeed, reverse, polarity invert, and any of the 30 built-in effect plugins.
5. **`convert_audio`**: Convert audio files or folders (reads WAV, AIFF, FLAC, MP3, OGG, M4A/AAC, ALAC, CAF) to `wav`, `aiff`, or `flac` with custom `sample_rate`, `bit_depth` (`16`, `24`, `32f`), and normalization.
6. **`get_audio_info`**: Inspect format, channels, sample rate, bit depth, and duration of audio files or `.scraft` track layouts, plus optional `loudness` (`peak_db`, `true_peak_db`, `lufs`) and `waveform` image rendering.
7. **`list_soundcraft_catalog`**: Browse 483 engine commands, all 30 built-in audio/instrument plugins with parameter IDs, ranges, and units, `drum_synth` note names (`kick`, `snare`, `clap`, `hat`, `open_hat`, `low_tom`, `mid_tom`, `high_tom`, `crash`, `ride`), and supported formats.
8. **`run_soundcraft_commands`**: Execute raw SoundCraft engine commands (`track.new`, `midi.new_clip`, `midi.note_add`, `import_audio`, `inspect_session`, `bounce_mix`) with `$steps[N].field` references in headless mode or live (`live: true`, port `7801`).
9. **`open_in_soundcraft`**: Open a `.scraft` session in the SoundCraft desktop application (optionally enabling the live control channel on port `7801`).
10. **`get_soundcraft_status`**: Check platform, `soundcraft-cli` version, command and plugin counts, executable paths, and live control port status.

## Practical Examples

### 1. Creating a Synthwave Multitrack Session (WAV + FLAC + Stems + MIDI + .scraft)

```json
{
  "name": "Miami_Night_Drive",
  "tempo": 112,
  "key": "A minor",
  "busses": [
    { "name": "Verb", "effects": [{ "plugin": "room_reverb" }] }
  ],
  "markers": [
    { "name": "Intro", "at": 0 },
    { "name": "Groove", "at": 4.28 }
  ],
  "tracks": [
    {
      "type": "instrument",
      "name": "Drums",
      "instrument": "drum_synth",
      "bars": 1,
      "repeat": 4,
      "notes": [
        { "pitch": "kick", "start": 0, "length": 0.5 },
        { "pitch": "hat", "start": 0.5, "length": 0.25 },
        { "pitch": "snare", "start": 1, "length": 0.5 },
        { "pitch": "hat", "start": 1.5, "length": 0.25 },
        { "pitch": "kick", "start": 2, "length": 0.5 },
        { "pitch": "hat", "start": 2.5, "length": 0.25 },
        { "pitch": "snare", "start": 3, "length": 0.5 },
        { "pitch": "open_hat", "start": 3.5, "length": 0.5 }
      ]
    },
    {
      "type": "instrument",
      "name": "Bass",
      "instrument": "subtractive_synth",
      "volume_db": -3,
      "notes": [
        { "pitch": "A1", "start": 0, "length": 2 },
        { "pitch": "F1", "start": 2, "length": 2 }
      ],
      "bars": 1,
      "repeat": 4,
      "effects": [{ "plugin": "compressor", "params": { "threshold": -18 } }]
    },
    {
      "type": "instrument",
      "name": "Lead",
      "instrument": "subtractive_synth",
      "volume_db": -5,
      "pan": 0.2,
      "sends": [{ "bus": "Verb", "level_db": -10 }],
      "notes": [
        { "pitch": "A4", "start": 0, "length": 1 },
        { "pitch": "C5", "start": 1, "length": 1 },
        { "pitch": "E5", "start": 2, "length": 1.5 },
        { "pitch": "G4", "start": 3.5, "length": 0.5 }
      ],
      "bars": 1,
      "repeat": 4,
      "effects": [{ "plugin": "chorus" }]
    }
  ],
  "formats": ["wav", "flac", "stems", "mid", "scraft"],
  "normalize": true,
  "output_dir": "/path/to/workspace"
}
```

### 2. Mastering & Time/Pitch Processing an Audio File

```json
{
  "input_path": "/path/to/workspace\\Miami_Night_Drive.wav",
  "fade_in": 0.2,
  "fade_out": 0.8,
  "normalize_db": -1,
  "effects": [
    { "plugin": "compressor", "params": { "threshold": -16 } }
  ],
  "format": "flac",
  "bit_depth": "24",
  "output_dir": "/path/to/workspace"
}
```

## Best Practices

- Always supply **absolute paths** (e.g. `/Users/alex/project/file.ext` on macOS/Linux or `C:\Users\alex\project\file.ext` on Windows).
- Audio positions (`at`, trims, fades, markers) are in **seconds**; MIDI `start` and `length` are in **quarter-note beats** from the start of the clip.
- Query `list_soundcraft_catalog` (`kind: "plugins"`) when you need exact plugin parameter IDs and value ranges.
- Always surface output file links using `[filename](file:///absolute/path/to/file)`.
