# compress-video

An interactive FFmpeg wrapper for video compression — with codec selection, quality presets, optional trimming, and a before/after size report. No GUI required.

![bash](https://img.shields.io/badge/shell-bash-4EAA25?logo=gnubash&logoColor=white)
![license](https://img.shields.io/badge/license-MIT-blue)

```
  ██╗   ██╗██╗██████╗ ███████╗ ██████╗ ██████╗ ███╗   ███╗██████╗
  ██║   ██║██║██╔══██╗██╔════╝██╔════╝██╔═══██╗████╗ ████║██╔══██╗
  ██║   ██║██║██║  ██║█████╗  ██║     ██║   ██║██╔████╔██║██████╔╝
  ╚██╗ ██╔╝██║██║  ██║██╔══╝  ██║     ██║   ██║██║╚██╔╝██║██╔═══╝
   ╚████╔╝ ██║██████╔╝███████╗╚██████╗╚██████╔╝██║ ╚═╝ ██║██║
    ╚═══╝  ╚═╝╚═════╝ ╚══════╝ ╚═════╝ ╚═════╝ ╚═╝     ╚═╝╚═╝
```

## Install

```bash
curl -fsSL get.notvc.to/install/compress-video | bash
```

Prefer to inspect the script before running it? [View it here](https://get.notvc.to/compress-video), then run the command above.

## Usage

Just run it — it walks you through everything interactively:

```bash
compress-video
```

Or see the full reference:

```bash
compress-video --help
```

## Features

- **Input analysis** — shows resolution, codec, duration, bitrate, and file size via `ffprobe` before you commit
- **Three codec options:**
  - H.265 / HEVC (CPU) — best balance of size and compatibility
  - AV1 (CPU) — smallest files; slower encode
  - HEVC NVENC (NVIDIA GPU) — fast hardware encoding, auto-detects GPU availability
- **Three quality presets** — High / Med / Low, each mapped to sane CRF values
- **Optional trimming** — accepts `HH:MM:SS` or plain seconds; start-only, end-only, or both
- **Before/after report** — shows exactly how much space you saved once encoding completes

## Dependencies

| Tool | Required | Purpose |
|---|---|---|
| `ffmpeg` | ✅ Yes | Encoding |
| `ffprobe` | Optional | Input file analysis |
| `bc` | Optional | Human-readable size formatting |

Install on Debian/Ubuntu:
```bash
sudo apt install ffmpeg bc
```

Install on Arch:
```bash
sudo pacman -S ffmpeg bc
```

## License

MIT — see [LICENSE](LICENSE)
