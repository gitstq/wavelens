<p align="center">
  <img alt="WaveLens" src="https://raw.githubusercontent.com/gitstq/wavelens/main/demo/spectrogram.png" width="720">
</p>

<h1 align="center">WaveLens</h1>

<p align="center">
  <b>Local-first · Offline · Zero-dependency browser audio spectrogram & sound analysis lab</b><br>
  零依赖、离线、本地优先的浏览器音频频谱分析实验室
</p>

<p align="center">
  <img alt="MIT" src="https://img.shields.io/badge/license-MIT-blue.svg">
  <img alt="Zero Dep" src="https://img.shields.io/badge/dependencies-0-brightgreen.svg">
  <img alt="Platform" src="https://img.shields.io/badge/platform-browser-lightgrey.svg">
  <img alt="PRs Welcome" src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg">
</p>

---

## 🌐 Language / 语言

[English](#english) · [中文](#中文)

---

## English

**WaveLens** is a fully client-side, offline-first audio spectrum analysis laboratory. It turns your audio files or live microphone input into a rich set of scientific visualizations — **spectrogram, waveform, frequency spectrum — plus real-time acoustic metrics** (RMS, Peak, Crest Factor, integrated Loudness / LUFS, Spectral Centroid, Zero-Crossing Rate).

Everything runs **100% in your browser**. No backend, no tracking, no uploads — your audio never leaves your device.

### ✨ Features

- **🔬 Real spectrogram** — true FFT-based time–frequency heatmap with 7 scientific colormaps (Magma, Viridis, Inferno, Plasma, Turbo, Ocean, Grayscale).
- **🎛 DSP engine** — selectable FFT size (512–8192) and 6 window functions (Hann, Hamming, Blackman, Blackman-Harris, Welch, Rectangular).
- **📊 Audio metrics** — real-time RMS, Peak, Crest Factor, K-weighted loudness estimate (LUFS), Spectral Centroid, Zero-Crossing Rate.
- **🎤 Microphone live analysis** — real-time spectrogram & waveform from your mic input.
- **▶ Full-file spectrogram** — one-click render of a complete spectrogram for any loaded file, with a progress bar.
- **📦 Audio playback** — play/pause with position tracking and spacebar shortcut.
- **⬇ PNG export** — download the current spectrogram as a high-resolution PNG.
- **🖥 Responsive dark UI** — polished, modern interface that adapts to any screen.
- **🔒 Private by design** — zero network requests, zero dependencies, works fully offline.

### 🚀 Quick Start

Open the app directly (no build step):

```bash
# Option 1 — just open the file
open index.html

# Option 2 — local static server
npx serve . -l 8080
# then open http://localhost:8080
```

Drag & drop any audio file (WAV, MP3, FLAC, OGG, M4A, AAC) onto the page, or click **⬆ Load Audio**. Or click **🎤 Mic** to start live analysis.

### 🖼 Screenshots

| Spectrogram | Full UI |
|:---:|:---:|
| <img src="https://raw.githubusercontent.com/gitstq/wavelens/main/demo/spectrogram.png" width="360"> | <img src="https://raw.githubusercontent.com/gitstq/wavelens/main/demo/ui.png" width="360"> |

### 🧠 How it works

- **Radix-2 Cooley–Tukey FFT** implemented from scratch (no library).
- Signal is windowed, transformed, and mapped to a decibel scale, then projected through a configurable colormap LUT.
- Acoustic metrics are derived from the time-domain buffer and the FFT magnitude spectrum.

### 🧰 Browser support

Chrome, Edge, Firefox, Safari (latest versions). Requires Web Audio API and `Float32Array`.

### 🤝 Contributing

PRs and issues are welcome. See [CONTRIBUTING](https://docs.github.com/en/get-started/quickstart) for the general flow.

### 📄 License

[MIT](./LICENSE) © WaveLens

---

## 中文

**WaveLens** 是一款完全在浏览器端运行、离线优先的音频频谱分析实验室。它将本地音频文件或麦克风实时输入转化为一整套科学可视化 —— **频谱图、波形、频率谱**，并提供**实时声学指标**（RMS 均方根、峰值、峰值因数、加权响度估算 LUFS、频谱质心、过零率）。

一切处理**都在你的浏览器内完成**。无后端、无追踪、无上传 —— 音频永远不会离开你的设备。

### ✨ 功能特性

- **🔬 真实频谱图** — 基于 FFT 的时频热力图，支持 7 套科学配色（Magma、Viridis、Inferno、Plasma、Turbo、Ocean、灰度）。
- **🎛 数字信号处理引擎** — 可选 FFT 尺寸（512–8192）与 6 种窗函数（Hann、Hamming、Blackman、Blackman-Harris、Welch、矩形）。
- **📊 音频指标** — 实时 RMS、峰值、峰值因数、K 加权响度估算（LUFS）、频谱质心、过零率。
- **🎤 麦克风实时分析** — 从麦克风输入实时生成频谱图与波形。
- **▶ 全文件频谱图** — 一键渲染任意已加载文件的完整频谱图，带进度条。
- **📦 音频播放** — 播放/暂停与进度追踪，支持空格键快捷键。
- **⬇ PNG 导出** — 将当前频谱图下载为高清 PNG。
- **🖥 响应式暗色界面** — 精致现代的界面，适配各种屏幕。
- **🔒 隐私优先** — 零网络请求、零依赖、完全可离线运行。

### 🚀 快速开始

直接打开应用（无需构建步骤）：

```bash
# 方式一 —— 直接打开文件
open index.html

# 方式二 —— 本地静态服务器
npx serve . -l 8080
# 然后访问 http://localhost:8080
```

将任意音频文件（WAV、MP3、FLAC、OGG、M4A、AAC）拖放到页面，或点击 **⬆ 载入音频**。也可以点击 **🎤 麦克风** 开始实时分析。

### 🖼 界面预览

| 频谱图 | 完整界面 |
|:---:|:---:|
| <img src="https://raw.githubusercontent.com/gitstq/wavelens/main/demo/spectrogram.png" width="360"> | <img src="https://raw.githubusercontent.com/gitstq/wavelens/main/demo/ui.png" width="360"> |

### 🧠 工作原理

- **基-2 Cooley–Tukey FFT** 从零手写实现（无任何库）。
- 信号经过加窗、变换，映射到分贝刻度，再通过可配置的配色 LUT 投影为图像。
- 声学指标由时域缓冲与 FFT 幅度谱推导得出。

### 🧰 浏览器支持

Chrome、Edge、Firefox、Safari（最新版本）。需要 Web Audio API 与 `Float32Array`。

### 🤝 参与贡献

欢迎提交 PR 与 Issue。

### 📄 开源协议

[MIT](./LICENSE) © WaveLens