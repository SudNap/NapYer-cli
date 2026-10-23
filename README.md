# NapYer-cli

![C++](https://img.shields.io/badge/C%2B%2B-17-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Termux%20%7C%20Linux-lightgrey.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-WIP-orange.svg)

A terminal media player written in C++ for Termux and Linux. It plays audio through `mpv` and shows a live visualizer, progress bar, and hotkeys right in the terminal.

## Why NapYer?

I got tired of opening heavy apps just to play music while studying in Termux. I wanted something simple, fast, and looking cool in the terminal. That's how NapYer-cli was born.

## Features

- Plays audio via `mpv` (MP3, WAV, OGG, whatever mpv supports).
- Live visualizer (sine waves for now, working on real audio spectrum).
- Progress bar with timestamps.
- No dependencies other than `mpv` and `socat`.

## Controls

- `Left / Right` - Seek 5s backward / forward
- `Space` - Pause / Play
- `Up / Down` - Volume up / down
- `Esc` - Quit

## How to build and run

You'll need Termux (or Linux) and clang. Also, make sure you have `mpv` and `socat` installed.

```bash
pkg install mpv socat clang
```

Compile it:

```bash
clang++ -O2 -std=c++17 napyer.cpp -o napyer
```

Run it with any audio file:

```bash
./napyer song.mp3
```

## Roadmap

- [x] Basic playback via mpv IPC
- [x] Keyboard controls
- [x] Progress bar
- [ ] Real FFT visualizer (instead of fake sine waves)
- [ ] Playlist support (play whole folder)
- [ ] ID3 tags (show artist and title)
- [ ] Equalizer maybe? (not sure yet)

## License

MIT. Do whatever you want with it. See LICENSE file.
