# Awesome Audio Processing

> A curated list of audio processing tools, libraries, and resources — organized by **equalizer**, **visualization**, **lyrics/subtitle synchronization**, and **audio analysis**.

---

## Table of Contents

- [Equalizer](#equalizer)
- [Visualization](#visualization)
- [Lyrics & Subtitle Synchronization](#lyrics--subtitle-synchronization)
- [Audio Processing & Analysis](#audio-processing--analysis)
- [Web Audio API](#web-audio-api)
- [DSP & Plugin Development](#dsp--plugin-development)

---

## Equalizer

> Tools and libraries that provide frequency band control (graphic/parametric EQ), filtering, and gain adjustment.

### Python

| Project | Language | What it does | License | Link |
|---------|----------|--------------|---------|------|
| **pedalboard** (Spotify) | Python + C++ | VST3/AU plugin host with 40+ built-in effects including EQ, compressor, reverb. | BSD-3 | [GitHub](https://github.com/spotify/pedalboard) |
| **awesome-audio-equalizer** | Python | Processes audio stream from input device, applies filtering, streams to output device. | MIT | [GitHub](https://github.com/Hyper5phere/awesome-audio-equalizer) |

### JavaScript / Web

| Project | Language | What it does | License | Link |
|---------|----------|--------------|---------|------|
| **equalizer** (0xba1a) | JavaScript | Web Audio API-based EQ using `AudioContext` and cascaded `BiquadFilterNode`. | — | [GitHub](https://github.com/0xba1a/equalizer) |
| **equalizer.js** | JavaScript + Canvas | Audio analysis tool with FFT visualization. Visualizations synced to playback. | MIT | [GitHub](https://github.com/jonobr1/equalizer.js) |
| **Waviz** | React + TypeScript | Audio visualization library with waveforms and frequency bars. Published on npm. | MIT | [GitHub](https://github.com/Waviz-Team/Waviz) |

### C / C++ (VST/AU Plugins)

| Project | Language | Plugin Formats | What it does | License | Link |
|---------|----------|----------------|--------------|---------|------|
| **ZLEqualizer** | C++ (JUCE) | VST3, AU, LV2 | Dynamic EQ with customizable bands, spectrum display, equalization match feature. | GPL-3.0 | [GitHub](https://github.com/ZL-Audio/ZLEqualizer) |
| **FreeEQ8** | C++ (JUCE) | VST3, AU, LV2 | 8-band parametric EQ plugin for macOS, Linux, Windows. Linear phase, dynamic EQ, match EQ. | GPL-3.0 | [GitHub](https://github.com/webprofusion/FreeEQ8) |
| **equalize_it** | C++ (JUCE) | VST3 | 12-band parametric EQ. | GPL-3.0 | [GitHub](https://github.com/egoracle/equalize_it) |
| **RBJ Audio EQ Cookbook** | C++ | — | Implementation of Robert Bristow-Johnson's EQ filter coefficient formulas. | — | [GitHub](https://github.com/bartoszsh/RBJ-Audio-EQ-Cookbook) |

### Desktop Applications

| Project | Platform | What it does | License | Link |
|---------|----------|--------------|---------|------|
| **eqMac** | macOS | System-wide audio equalizer with volume mixer. Swift-based. | GPL-3.0 | [GitHub](https://github.com/bitgapp/eqmac) |
| **Equalizer APO** | Windows | Parametric/graphic equalizer. Uses Windows Audio Processing Object (APO) interface. | GPL-2.0 | [SourceForge](https://sourceforge.net/projects/equalizerapo/) |

---

## Visualization

> Tools that render audio data as visual output: waveforms, spectrograms, frequency bars, and audio-reactive graphics.

### JavaScript Libraries (Browser)

| Project | Language | What it does | License | Link |
|---------|----------|--------------|---------|------|
| **wavesurfer.js** | TypeScript | Interactive audio waveform rendering and playback. Plugins: Regions, Timeline, Envelope, Minimap, Record, Spectrogram, Hover. | BSD-3 | [GitHub](https://github.com/katspaugh/wavesurfer.js) |
| **peaks.js** (BBC) | JavaScript | Audio waveform display with zoom/pan interaction. | MIT | [GitHub](https://github.com/bbc/peaks.js) |
| **audioMotion-analyzer** | JavaScript | Real-time spectrum analyzer. CQT, FFT, octave bands. Multiple scales: linear, log, Mel, ERB, Bark. | ISC | [GitHub](https://github.com/hvianna/audioMotion-analyzer) |
| **Clubber.js** | JavaScript | Music theory concepts applied to audio-reactive visualization. | MIT | [GitHub](https://github.com/lo-th/clubber) |
| **Pulse Visualizer** | C++ | Audio visualizer inspired by MiniMeters. Cross-platform via CMake. | GPL-3 | [GitHub](https://github.com/Audio-Solutions/pulse-visualizer) |

### React Ecosystem

| Project | Platform | What it does | Link |
|---------|----------|--------------|------|
| **react-voice-visualizer** | React Web | Web Audio API for audio recording and visualization. Waveform and amplitude bars. | [GitHub](https://github.com/YZarytskyi/react-voice-visualizer) |
| **react-audio-visualizer-pro** | React Web | Multiple visualization types: waveform, frequency bars, circular. Customizable themes. | [GitHub](https://github.com/SujalXplores/react-audio-visualizer-pro) |
| **r3f-audio-visualizer** | React + THREE.js | THREE.js 3D visualization synced to audio frequency data. | [GitHub](https://github.com/dcyoung/r3f-audio-visualizer) |
| **audio-ui** | React | Component library for building audio software UIs. Faders, knobs, meters. | [GitHub](https://github.com/cutoff/audio-ui) |
| **react-audio-visualize** (samhirtarif) | React | Audio visualizer with separate components for live audio and audio blobs. | [GitHub](https://github.com/samhirtarif/react-audio-visualize) |
| **Spectro** | React + WebGL | Real-time audio spectrogram generator. | [GitHub](https://github.com/calebjoseph/spectro) |

### Desktop & Standalone Visualizers

| Project | Language | Platform | What it does | License | Link |
|---------|----------|----------|--------------|---------|------|
| **cava** | C | Linux, macOS, Windows (WSL) | Terminal frequency bars. Uses ALSA, PulseAudio, PipeWire, or PortAudio input. Color-coded. | MIT | [GitHub](https://github.com/karlstav/cava) |
| **GLava** | C | Linux | OpenGL-based audio spectrum visualizer for desktop environments. | MIT | [GitHub](https://github.com/jarcode-foss/glava) |
| **MilkDrop 3** | C++ | Windows | Updated MilkDrop music visualizer with beat detection and double-preset loading. | — | [GitHub](https://github.com/milkdrop2077/milkdrop3) |
| **ModV** | JavaScript + GLSL | Desktop (Electron) | Modular, shader-based audio visualizer/VJ software. Vue-based. | GPL-3.0 | [GitHub](https://github.com/vcync/modv) |
| **Euphonica** | Rust + GTK4 | Linux (GNOME) | MPD client with spectrum visualizer. Built with Rust, GTK4, Libadwaita. | MIT | [GitHub](https://github.com/hvianna/euphonica) |
| **XR3Player** | Java + JavaFX | Cross-platform | Media player with built-in spectrum analyzer and audio visualization. | — | [GitHub](https://github.com/goxr3plus/xr3player) |

### OBS & Video Integration

| Project | Language | What it does | Link |
|---------|----------|--------------|------|
| **Waveform (OBS)** | C++ | Audio spectral analysis plugin for OBS Studio. Renders waveform overlay in OBS scenes. | [GitHub](https://github.com/phandasm/waveform) |
| **videojs-wavesurfer** | JavaScript | Video.js plugin that adds navigable audio/video waveforms and visualization. | [GitHub](https://github.com/collab-project/videojs-wavesurfer) |

| Project | Language | What it does | Link |
|---------|----------|--------------|------|
| **ShowCQTBar** | — | Real-time CQT (Constant-Q Transform) bar visualization for audio files. | [GitHub](https://github.com/ChenLX233/ShowCQTBar) |

### Mobile (Flutter / Swift)

| Project | Language | Platform | What it does | Link |
|---------|----------|----------|--------------|------|
| **flutter_soloud** | Dart (Flutter) + C++ (FFI) | Mobile/Desktop | Flutter plugin for low-level audio processing and visualization using the SoLoud C++ library via FFI. | [GitHub](https://github.com/alnitak/flutter_soloud) |

### Web Audio Editors

| Project | Language | What it does | License | Link |
|---------|----------|--------------|---------|------|
| **Waveform Playlist** | TypeScript | Multitrack Web Audio editor/player with canvas waveform preview, cue/fade editing, WAV/AudioBuffer export. | MIT | [GitHub](https://github.com/naomiaro/waveform-playlist) |

---

## Lyrics & Subtitle Synchronization

> Tools for parsing, generating, aligning, and converting timed text (LRC, SRT, ASS) to match audio playback.

### LRC (Lyrics) — Parsers & Libraries

| Project | Language | What it does | License | Link |
|---------|----------|--------------|---------|------|
| **syncedlyrics** | Python | Fetches and parses synchronized lyrics in LRC format from online sources. | MIT | [GitHub](https://github.com/moehmeni/syncedlyrics) |
| **openlrc** | Python | Transcribes audio with OpenAI Whisper, translates with LLM (GPT/Claude), outputs LRC files. | GPL-3.0 | [GitHub](https://github.com/zh-plus/openlrc) |
| **lrcget** | Vue + Rust | Utility for mass-downloading LRC synced lyrics for offline music library. | MIT | [GitHub](https://github.com/tranxuanthang/lrcget) |
| **syrics** | Python | CLI tool to fetch lyrics from Spotify and save to lrc file. | GPL-3.0 | [GitHub](https://github.com/akashrchandran/syrics) |
| **Lyrica** | Python | Tool to fetch lyrics (synced and non-synced) and print as JSON. | — | [GitHub](https://github.com/Wilooper/Lyrica) |
| **lrxy** | Python | Synced lyrics downloader, converter and embedder tool. | GPL-3.0 | [GitHub](https://github.com/pxeemo/lrxy) |
| **Lyricsync** | Python | Auto-sync via VAD + WhisperX + segment alignment. CLI and Web UI. | — | [GitHub](https://github.com/sparksthedragon0101/Lyricsync) |
| **lrc-kit** (reteps) | Python | Library for searching, downloading, and parsing song lyrics in LRC format. | — | [GitHub](https://github.com/reteps/lrc-kit) |
| **lrc-kit** (weirongxu) | TypeScript | Lyric parser, maker, and runner. JavaScript/TypeScript ecosystem. | MIT | [GitHub](https://github.com/weirongxu/lrc-kit) |
| **lrc-file-parser** | JavaScript | JavaScript-based LRC file parser. | — | [GitHub](https://github.com/lyswhut/lrc-file-parser) |
| **liricle** | TypeScript | JS/TS library to synchronize lyrics with audio playback position. | — | [GitHub](https://github.com/mcanam/liricle) |
| **lrctoolbox** | Python | CLI tool for .lrc files: edit, convert, analyze. | — | [GitHub](https://github.com/Dr-Blank/lrctoolbox) |

### LRC — Tools & Editors

| Project | Language | What it does | Link |
|---------|----------|--------------|------|
| **LySy** | Web (JS) | Web app for timestamp-based LRC lyric creation with download. | [GitHub](https://github.com/pxeemo/LySy) |
| **EasyLRC** | Web | Web-based LRC lyric editing interface. | [GitHub](https://github.com/landeyucc/EasyLRC) |

### LRC — Specifications & Extensions

| Resource | Format | What it does | Link |
|----------|--------|--------------|------|
| **LRCv2** (draft) | LRC v2 | Spec draft for synced lyrics with translation support, metadata fields, and chord annotations. | [GitHub](https://github.com/marz1877/LRCv2) |
| **lyrsync** | JavaScript + CSS | Uses CSS custom properties and timers to display synced lyrics with styling. | [GitHub](https://github.com/YoshiWalsh/lyrsync) |
| **Accompanist-Lyrics** | Kotlin | Parse, convert, export lyrics. Supports Apple Music format and LRC. For Android/JVM. | [GitHub](https://github.com/6xingyv/Accompanist-Lyrics) |

### Subtitle Synchronization

| Project | Language | Method | What it does | License | Link |
|---------|----------|--------|--------------|---------|------|
| **ffsubsync** | Python + C | Audio fingerprinting | Automatic subtitle sync using audio fingerprint alignment. Supports SRT, ASS, VTT. | MIT | [GitHub](https://github.com/smacke/ffsubsync) |
| **autosubsync** (oseiskar) | Python | AI/ML shift + speed correction | Resynchronizes subtitles without human input. Detects time shift and playback speed drift. | MIT | [GitHub](https://github.com/oseiskar/autosubsync) |

---

## Audio Processing & Analysis

> Core libraries for loading, decoding, analyzing, and transforming audio data.

### Python

| Project | What it does | Language / Backend | License | Link |
|---------|--------------|--------------------|---------|------|
| **librosa** | Audio/music analysis. Feature extraction (MFCC, chroma, tempo), onset detection, beat tracking, STFT. | Python + NumPy, SciPy | ISC | [GitHub](https://github.com/librosa/librosa) |
| **pydub** | Audio manipulation. Slice, concatenate, format conversion, volume adjustment, effects. Uses ffmpeg for decoding. | Python | MIT | [GitHub](https://github.com/jiaaro/pydub) |
| **python-soundfile** | Audio file I/O. Read/write WAV, FLAC, OGG, and other formats via libsndfile. | Python + libsndfile | BSD-3 | [GitHub](https://github.com/bastibe/python-soundfile) |
| **pyAudioAnalysis** | Audio ML. Feature extraction, classification, segmentation, speaker diarization. | Python + scikit-learn | Apache-2.0 | [GitHub](https://github.com/tyiannak/pyAudioAnalysis) |
| **torchaudio** | Deep learning audio. Audio I/O, transforms (Mel, MFCC, SpecAugment), datasets, pre-trained models (Wav2Vec2, HuBERT). | Python + PyTorch | BSD-2 | [GitHub](https://github.com/pytorch/audio) |
| **essentia** | MIR / audio analysis. 400+ algorithms: rhythm, tonality, timbre, loudness, speech/music detection. | C++ + Python | AGPL-3.0 / Commercial | [GitHub](https://github.com/MTG/essentia) |
| **audioFlux** | Audio feature extraction. 60+ audio features (FFT, STFT, MFCC, chroma, wavelet). GPU-accelerated. | C + Python | MIT | [GitHub](https://github.com/libaudioflux/audioflux) |
| **SoundCard** | Python audio I/O. Works with ALSA, CoreAudio, WASAPI. | Python + C | BSD-3 | [GitHub](https://github.com/bastibe/SoundCard) |
| **aubio** | Audio labeling. Tempo, beat, pitch, onset, silence detection. | C | GPL-3.0 | [GitHub](https://github.com/aubio/aubio) |

### JavaScript / TypeScript

| Project | What it does | License | Link |
|---------|--------------|---------|------|
| **meyda** | Audio feature extraction: MFCC, spectral centroid, zero-crossing rate, chroma, loudness. Web Audio API-based. | MIT | [GitHub](https://github.com/meyda/meyda) |
| **web-audio-beat-detector** | Detects BPM and beat positions from audio via Web Audio API. | MIT | [GitHub](https://github.com/chrisguttandin/web-audio-beat-detector) |
| **waveform-data-generator** (BBC) | Resample, offset, and segment waveform peak data. | MIT | [GitHub](https://github.com/bbc/waveform-data-generator) |

### C / C++

| Project | What it does | License | Link |
|---------|--------------|---------|------|
| **libsndfile** | Audio file I/O. Read/write WAV, AIFF, FLAC, OGG, and more. | LGPL-2.1 | [GitHub](https://github.com/libsndfile/libsndfile) |
| **SoX** | Format conversion, effects, analysis. CLI tool. | GPL-2.0 / LGPL | [SourceForge](https://sourceforge.net/projects/sox/) |

### Rust

| Project | What it does | License | Link |
|---------|--------------|---------|------|
| **hound** | WAV encoding and decoding. | MIT | [GitHub](https://github.com/ruuda/hound) |
| **rodio** | Audio playback. WAV, OGG, FLAC, MP3 with effects. | Zlib | [GitHub](https://github.com/RustAudio/rodio) |

### Go

| Project | What it does | Link |
|---------|--------------|------|
| **audio** | Audio processing interface. Decoding, encoding, resampling, effects pipeline. | [GitHub](https://github.com/gopxl/audio) |

---

## Web Audio API

> Wrappers, utilities, and higher-level abstractions built on the browser's native Web Audio API.

| Project | What it does | License | Link |
|---------|--------------|---------|------|
| **standardized-audio-context** | Cross-browser `AudioContext` implementation following the Web Audio API spec. | MIT | [GitHub](https://github.com/chrisguttandin/standardized-audio-context) |
| **web-audio-analyser** | Thin wrapper around `AnalyserNode` for waveform and frequency data access. | — | [GitHub](https://github.com/mmckegg/web-audio-analyser) |
| **Pizzicato.js** | Oscillators, samples, effects (delay, reverb, distortion). Chainable API. | MIT | [GitHub](https://github.com/alexbikfalvi/Pizzicato.js) |
| **p5.sound** | Extension to p5.js: amplitude, FFT, filters, oscillators, soundfile playback, spatial audio. | LGPL | [GitHub](https://github.com/processing/p5.js-sound) |
| **Tone.js** | Music composition. Synths, effects, transport control, scheduling. | MIT | [GitHub](https://github.com/Tonejs/Tone.js) |

---

## DSP & Plugin Development

> Frameworks and tools for building audio plugins (VST, AU, AAX) and digital signal processing.

| Project | Language | Plugin Formats | What it does | License | Link |
|---------|----------|----------------|--------------|---------|------|
| **JUCE** | C++17 | VST, VST3, AU, AUv3, AAX, LV2 | Cross-platform framework. Includes Projucer IDE, CMake build, DSP module (IIR, FIR, convolution, FFT). | BSD/Commercial | [GitHub](https://github.com/juce-framework/JUCE) |
| **iPlug2** | C++11 | VST2, VST3, AU, AUv3, AAX, WAM | Alternative to JUCE. CMake build, iOS/Android support, web-based plugin support. | zlib | [GitHub](https://github.com/iPlug2/iPlug2) |
| **DISTRHO** | C++ | LV2, VST2, VST3 | Plugin framework for Linux. Focus on LV2 ecosystem. | ISC | [GitHub](https://github.com/DISTRHO/DISTRHO-Ports) |
| **NIH-Plug** | Rust | VST3, CLAP | Rust-based audio plugin framework. | MIT | [GitHub](https://github.com/robbert-vdh/nih-plug) |
| **Web Audio Modules (WAM)** | JavaScript | Web Audio | Specification for running Web Audio API-based plugins in the browser. | — | [GitHub](https://github.com/webaudiomodules) |

---

## Contributing

Contributions are welcome. Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

To add a resource:
1. Check existing entries to avoid duplicates
2. Include technical details (language, license, what it does)
3. Add to the most relevant section
4. Submit a Pull Request

---

## License

This list is dedicated to the public domain under [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/).
