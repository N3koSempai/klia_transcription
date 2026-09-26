# klia transcribe ★

**100% local** call transcription with speaker diarization. klia records your system's output audio during your calls (Google Meet and similar) and produces a speaker-separated transcription — entirely on your machine. No browser extensions, no tracking, no accounts, no cloud, no audio sent to any service.

## Features

- **Local system audio recording** via PipeWire — captures the audio output during your calls, without touching your microphone or installing anything in your browser.
- **Local transcription and diarization** with MOSS-Transcribe-Diarize — separates speakers ("Speaker 01", "Speaker 02"...) directly on your machine.
- **Automatic summaries, task and decision extraction** — reuses the local language model of [hetairos-ai](https://flathub.org/en/apps/io.github.N3kosempai.hetairos-ai) when installed (D-Bus integration).
- **Call Q&A** — ask questions about the transcript: "What did Ana decide?", "Which date did Carlos mention?".
- **One-click transcript translation**.
- **Privacy by design** — recordings are stored **encrypted** on your disk. Storage in Opus (audio) + SQLite (metadata).
- **Multilingual UI** — available in Spanish, English, Portuguese, Japanese, Russian and Chinese.
- **Flatpak distribution** — sandboxed packaging for Linux x86_64.

## Installation

Download the latest `.flatpak` bundle from the [Releases](https://github.com/N3koSempai/klia_transcription/releases) page and install it:

```bash
flatpak install ./klia-transcribe-<version>.flatpak
```

## Usage

1. Start klia and hit record before joining your call.
2. When you hang up, klia generates the transcript with separated speakers.
3. From the same call: summary, tasks, Q&A or translation — whatever you need.

## Requirements

- Linux x86_64
- PipeWire (for system audio capture)

## How it works

klia uses the PipeWire API to capture the system's audio output (what you hear), stores it encrypted in Opus format, and processes it with a local transcription + diarization model. The generative AI layer (summary, tasks, Q&A, translation) is delegated to [hetairos-ai](https://flathub.org/en/apps/io.github.N3kosempai.hetairos-ai), a companion app that serves the model over D-Bus — also on your machine.

## Community

- Found a bug? Open an [issue](https://github.com/N3koSempai/klia_transcription/issues).
