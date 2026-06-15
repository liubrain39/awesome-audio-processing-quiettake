# Awesome Audio Processing

> A curated list of audio processing tools, libraries, and resources — organized by core development, AI intelligence, and end-user applications.

---

## Table of Contents

- [I. Core Development](#i-core-development)
  - [Audio Processing & Analysis](#audio-processing--analysis)
  - [DSP & Plugin Development](#dsp--plugin-development)
  - [Web Audio API](#web-audio-api)
- [II. AI & Voice Intelligence](#ii-ai--voice-intelligence)
  - [Speech & Voice (STT & TTS)](#speech--voice-stt--tts)
  - [Noise Reduction & Enhancement](#noise-reduction--enhancement)
  - [Audio Datasets](#audio-datasets)
- [III. Tools & Applications](#iii-tools--applications)
  - [Lyrics & Subtitle Synchronization](#lyrics--subtitle-synchronization)
  - [Equalizer](#equalizer)
  - [Visualization](#visualization)
- [IV. Learning & Community](#iv-learning--community)
  - [Resources & Learning](#resources--learning)
  - [Contributing](#contributing)

---

# I. Core Development

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

### Native & Systems (C/C++, Rust, Go)

| Project | Language | What it does | License | Link |
|---------|----------|--------------|---------|------|
| **libsndfile** | C | Audio file I/O. Read/write WAV, AIFF, FLAC, OGG, and more. | LGPL-2.1 | [GitHub](https://github.com/libsndfile/libsndfile) |
| **SoX** | C | Format conversion, effects, analysis. CLI tool. | GPL-2.0 / LGPL | [SourceForge](https://sourceforge.net/projects/sox/) |
| **hound** | Rust | WAV encoding and decoding. | MIT | [GitHub](https://github.com/ruuda/hound) |
| **rodio** | Rust | Audio playback. WAV, OGG, FLAC, MP3 with effects. | Zlib | [GitHub](https://github.com/RustAudio/rodio) |
| **audio** | Go | Audio processing interface. Decoding, encoding, resampling, effects pipeline. | — | [GitHub](https://github.com/gopxl/audio) |

## DSP & Plugin Development

> Frameworks and tools for building audio plugins (VST, AU, AAX) and digital signal processing.

| Project | Language | Plugin Formats | What it does | License | Link |
|---------|----------|----------------|--------------|---------|------|
| **JUCE** | C++17 | VST, VST3, AU, AUv3, AAX, LV2 | Cross-platform framework. Includes Projucer IDE, CMake build, DSP module (IIR, FIR, convolution, FFT). | BSD/Commercial | [GitHub](https://github.com/juce-framework/JUCE) |
| **iPlug2** | C++11 | VST2, VST3, AU, AUv3, AAX, WAM | Alternative to JUCE. CMake build, iOS/Android support, web-based plugin support. | zlib | [GitHub](https://github.com/iPlug2/iPlug2) |
| **DISTRHO** | C++ | LV2, VST2, VST3 | Plugin framework for Linux. Focus on LV2 ecosystem. | ISC | [GitHub](https://github.com/DISTRHO/DISTRHO-Ports) |
| **NIH-Plug** | Rust | VST3, CLAP | Rust-based audio plugin framework. | MIT | [GitHub](https://github.com/robbert-vdh/nih-plug) |
| **Web Audio Modules (WAM)** | JavaScript | Web Audio | Specification for running Web Audio API-based plugins in the browser. | — | [GitHub](https://github.com/webaudiomodules) |

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

# II. AI & Voice Intelligence

## Speech & Voice (STT & TTS)

### Model Comparison

| Model / Library | Primary Task | Speed | Accuracy | Best For |
|-----------------|--------------|-------|----------|----------|
| **Whisper Turbo**| STT | Fast | High | Multilingual, Production |
| **Canary** | STT | Medium | Very High | High Precision, Translation |
| **Vosk** | STT | Instant | Medium | Edge Devices, Offline |
| **Parler-TTS** | TTS | Medium | High | Natural Language Control |
| **MeloTTS** | TTS | Instant | High | Real-time, CPU Inference |

### Speech-to-Text (STT) / ASR

| Project | What it does | Language / Backend | License | Link |
|---------|--------------|--------------------|---------|------|
| **Whisper** (OpenAI) | Robust, multilingual speech recognition. Large-v3 Turbo offers high accuracy with 5x speedup. | Python / PyTorch | MIT | [GitHub](https://github.com/openai/whisper) |
| **faster-whisper** | Reimplementation of Whisper using CTranslate2. Up to 4x faster and more memory efficient. | Python / C++ | MIT | [GitHub](https://github.com/SYSTRAN/faster-whisper) |
| **Canary** (NVIDIA) | 1B parameter model for high-accuracy STT and translation in English, German, French, and Spanish. | Python / NeMo | Apache-2.0 | [GitHub](https://github.com/NVIDIA/NeMo) |
| **Vosk** | Offline, lightweight STT for edge devices (Android, iOS, Raspberry Pi). 20+ languages. | C / Python | Apache-2.0 | [GitHub](https://github.com/alphacep/vosk-api) |

### Text-to-Speech (TTS)

| Project | What it does | Language / Backend | License | Link |
|---------|--------------|--------------------|---------|------|
| **Parler-TTS** | Fully open-source TTS that generates high-quality speech based on natural language prompts. | Python / HF | Apache-2.0 | [GitHub](https://github.com/huggingface/parler-tts) |
| **MeloTTS** | Real-time TTS optimized for CPU inference. Supports multiple languages and accents. | Python | MIT | [GitHub](https://github.com/myshell-ai/MeloTTS) |
| **Piper** | Extremely fast, local neural TTS engine for low-power devices. Uses ONNX. | C++ / Python | MIT | [GitHub](https://github.com/rhasspy/piper) |
| **ChatTTS** | Optimized for conversational audio with natural prosody (laughter, pauses, "um/ah"). | Python | CC BY-NC 4.0 | [GitHub](https://github.com/2noise/ChatTTS) |

## Noise Reduction & Enhancement

| Project | What it does | Language / Tech | License | Link |
|---------|--------------|-----------------|---------|------|
| **DeepFilterNet** | State-of-the-art full-band (48kHz) audio enhancement using deep filtering. Very efficient. | Rust / PyTorch | MIT/Apache | [GitHub](https://github.com/Rikorose/DeepFilterNet) |
| **RNNoise** | Recurrent neural network for real-time noise suppression. Used in many OBS/Linux plugins. | C | BSD-3 | [GitHub](https://github.com/xiph/rnnoise) |
| **NoiseTorch** | User-friendly Linux app that creates a virtual microphone with real-time noise suppression. | Go / RNNoise | GPL-3.0 | [GitHub](https://github.com/noisetorch/NoiseTorch-ng) |
| **VoiceFixer** | Restores speech by removing noise, reverb, and clipping while increasing resolution. | Python | MIT | [GitHub](https://github.com/haoheliu/voicefixer) |

## Audio Datasets

| Dataset | Category | What it contains | Link |
|---------|----------|------------------|------|
| **AudioSet** (Google) | General / SED | 2M+ YouTube clips, 527 sound classes. The "ImageNet" of audio. | [Website](https://research.google.com/audioset/) |
| **Common Voice** (Mozilla) | Speech (ASR) | Massive, multi-language crowd-sourced speech dataset (30k+ hours). | [Website](https://commonvoice.mozilla.org/) |
| **LibriSpeech** | Speech (ASR) | 1,000 hours of English read speech from audiobooks. Standard benchmark. | [Website](https://www.openslr.org/12) |
| **MUSDB18** | Music (Source Sep) | 150 full-length tracks with isolated stems (vocals, drums, bass, other). | [Website](https://sigsep.github.io/datasets/musdb18.html) |
| **ESC-50** | Environmental | 2,000 labeled 5-second environmental recordings across 50 classes. | [GitHub](https://github.com/karolpiczak/ESC-50) |
| **FMA** (Free Music Archive) | Music / MIR | 100k+ tracks with metadata and pre-computed features. | [GitHub](https://github.com/mdeff/fma) |

---

# III. Tools & Applications

## Lyrics & Subtitle Synchronization

### Editor Comparison

| Tool | Format Support | Waveform | Styling (ASS) | Best For |
|------|----------------|----------|---------------|----------|
| **Aegisub** | High (ASS/SRT) | Yes | Advanced | Fansubbing, Karaoke |
| **Subtitle Edit** | Very High (300+) | Yes | Moderate | All-purpose, AI Tools |
| **Karaoke Lyric Editor**| Lyrics (LRC) | No | Moderate | Dedicated Lyric Sync |
| **Subtitld** | Moderate | Yes | Basic | Modern UI, Linux |

### Subtitle & Lyrics Editors

| Project | Language | Platform | What it does | License | Link |
|---------|----------|----------|--------------|---------|------|
| **Aegisub** | C++ (wxWidgets) | Linux, macOS, Windows | Advanced subtitle editor with waveform visualization, karaoke effects (KFX), ASS styling, automation scripts, and real-time video preview. | GPL-2.0 | [GitHub](https://github.com/Aegisub/Aegisub) |
| **Subtitle Edit** | C# (.NET) | Windows, Linux, macOS | Feature-rich subtitle editor with waveform/spectrogram view, auto-translation via Google/Bing, spell check, merge/split, 300+ format support, and OCR. | GPL-3.0 | [GitHub](https://github.com/SubtitleEdit/subtitleedit) |
| **Subtitle Composer** | C++ (Qt/KDE) | Linux, Windows, macOS | Video-based subtitle editor with waveform, speech recognition (via vosk/sphinx), real-time preview, and karaoke support. | GPL-2.0 | [GitHub](https://github.com/maxrd2/subtitlecomposer) |
| **Subtitld** | Python (Qt) | Linux, Windows | Modern, timeline-based subtitle editor with transcription, styling, and splitting tools. | GPL-3.0 | [GitHub](https://github.com/subtitld/subtitld) |
| **Subtitle Workshop Classic** | Pascal | Windows (Wine-compatible) | Community-driven continuation of the classic Subtitle Workshop. Supports 60+ formats and powerful batch operations. | GPL-3.0 | [GitHub](https://github.com/SubtitleWorkshop/subtitleworkshop) |
| **Jubler** | Java | Linux, macOS, Windows | Multi-format subtitle editor, translator, and timing tool with spell check, styles editor, and video preview. | GPL-2.0 | [GitHub](https://github.com/teras/Jubler) |
| **Gaupol** | Python (GTK) | Linux, macOS, Windows | Subtitle editor focused on text-based editing and batch timing adjustments. Supports speech recognition integration and multiple formats. | ISC | [GitHub](https://github.com/aegisub/gaupol) |
| **Gnome Subtitles** | C (GTK) | Linux | Lightweight subtitle editor with video preview, timing adjustments, and translation support. | GPL-2.0 | [GitHub](https://github.com/pedro-git/gnome-subtitles) |
| **Amara** | Python (Django) | Web | Collaborative subtitle and translation platform. Supports video hosting services, team workflows, and version control. | BSD | [GitHub](https://github.com/Amara-Platform/amara) |
| **Ollant** | C++ (Qt) | Linux, Windows | Subtitle editor with waveform visualization, real-time preview, and ASS styling support. | GPL-3.0 | [GitHub](https://github.com/leonardowf/ollant) |

### LRC — Tools & Editors

| Project | Language | What it does | Link |
|---------|----------|--------------|------|
| **Karaoke Lyric Editor** | C++ (Qt) | Dedicated tool for creating and testing LRC and CDG karaoke files. Real-time preview and video export. | [GitHub](https://github.com/vkrasnov/karlyriceditor) |
| **LRC Maker** | JavaScript | Web-based tool for creating LRC files with precise timing and metadata support. | [GitHub](https://github.com/mcanam/lrc-maker) |
| **LRC Editor** | Java | Simple, cross-platform desktop application for creating and editing LRC files. | [GitHub](https://github.com/fashni/lrc-editor) |
| **LySy** | Web (JS) | Web app for timestamp-based LRC lyric creation with download. | [GitHub](https://github.com/pxeemo/LySy) |
| **EasyLRC** | Web | Web-based LRC lyric editing interface. | [GitHub](https://github.com/landeyucc/EasyLRC) |

### Synchronization Tools & specs

- **[ffsubsync](https://github.com/smacke/ffsubsync)** (Python) - Automatic subtitle sync via audio fingerprinting.
- **[autosubsync](https://github.com/oseiskar/autosubsync)** (Python) - AI-powered shift and speed correction for subtitles.
- **[LRCv2 Spec](https://github.com/marz1877/LRCv2)** - Draft for synced lyrics with translation and chord support.
- **[syncedlyrics](https://github.com/moehmeni/syncedlyrics)** (Python) - Fetch and parse LRC lyrics from online sources.

## Equalizer

### Desktop Applications

- **[eqMac](https://github.com/bitgapp/eqmac)** (macOS) - System-wide audio equalizer and volume mixer.
- **[Equalizer APO](https://sourceforge.net/projects/equalizerapo/)** (Windows) - Powerful parametric/graphic equalizer using Windows APO.

### Developer Libraries

- **[pedalboard](https://github.com/spotify/pedalboard)** (Python) - Spotify's framework for VST3/AU hosting and built-in effects.
- **[ZLEqualizer](https://github.com/ZL-Audio/ZLEqualizer)** (C++) - JUCE-based dynamic EQ with spectrum display.
- **[equalizer.js](https://github.com/jonobr1/equalizer.js)** (JS) - FFT-based analysis and EQ tool.

## Visualization

### Web & React

- **[wavesurfer.js](https://github.com/katspaugh/wavesurfer.js)** - Interactive audio waveform rendering.
- **[peaks.js](https://github.com/bbc/peaks.js)** - BBC's waveform display with zoom/pan interaction.
- **[audioMotion-analyzer](https://github.com/hvianna/audioMotion-analyzer)** - High-performance real-time spectrum analyzer.
- **[react-voice-visualizer](https://github.com/YZarytskyi/react-voice-visualizer)** - Waveform and amplitude bars for recording.

### Desktop & CLI

- **[cava](https://github.com/karlstav/cava)** (C) - Terminal frequency bars for Linux, macOS, and Windows.
- **[GLava](https://github.com/jarcode-foss/glava)** (C) - OpenGL audio spectrum visualizer for Linux.
- **[ModV](https://github.com/vcync/modv)** (JS) - Modular VJ software and audio visualizer.

---

# IV. Learning & Community

## Resources & Learning

### 📺 YouTube Channels

- **[The Audio Programmer](https://www.youtube.com/@TheAudioProgrammer)** - Essential for C++ and JUCE framework.
- **[WolfSound](https://www.youtube.com/@WolfSoundAudio)** - Intuitive DSP theory and implementation.
- **[DSP Fundamentals](https://www.youtube.com/@dspfundamentals)** - Academic lectures on signals and systems.
- **[3Blue1Brown](https://www.youtube.com/@3blue1brown)** - Beautiful math visualizations (Fourier Transform).
- **[MIT DSP Lectures](https://www.youtube.com/playlist?list=PLUl4u3cNGP606x_3_Vz7X_v_8vV_v_8vV)** - Foundational signal theory by Prof. Oppenheim.

### 📚 Books & Articles

- **[The Scientist and Engineer's Guide to DSP](https://www.dspguide.com/)** - Best starting point (Free online).
- **[DAFx: Digital Audio Effects](https://www.dafx.de/)** - Standard reference for audio algorithms.
- **[Audio EQ Cookbook](https://www.w3.org/TR/audio-eq-cookbook/)** - Core formulas for biquad filters.
- **[Julius O. Smith's CCRMA Guides](https://ccrma.stanford.edu/~jos/)** - Comprehensive deep dives into filters and physical modeling.

### 🎙️ Podcasts & Blogs

- **[Tape Notes](https://tapenotes.co.uk/)** - Producers breakdown track stems.
- **[Song Exploder](https://songexploder.net/)** - Deep dives into song creation.
- **[Sound on Sound](https://www.soundonsound.com/)** - Technical articles and industry reviews.
- **[The Pro Audio Files](https://theproaudiofiles.com/)** - Mixing and production tutorials.

## Contributing

Contributions are welcome! Please read the [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

1.  **Check existing entries** to avoid duplicates.
2.  **Provide technical details** (Language, License, Feature summary).
3.  **Choose the right Pillar** (Core, AI, or Tools).

---

## License

Dedicated to the public domain under [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/).
