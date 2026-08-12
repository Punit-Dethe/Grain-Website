# GRAIN-01 — Official Website & Landing Page

<div align="center">

![GRAIN-01 Banner](https://raw.githubusercontent.com/Punit-Dethe/Grain-Website/main/preview.png)

[![License: MIT](https://img.shields.io/badge/License-MIT-orange.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Grain Repository](https://img.shields.io/badge/Grain-App_Repository-blue?style=flat&logo=github)](https://github.com/Punit-Dethe/Grain)

**[Visit Grain Website](https://punit-dethe.github.io/Grain-Website/)** | **[Main Grain Application](https://github.com/Punit-Dethe/Grain)**

</div>

---

## ⚡ Overview

This repository contains the source code for the official landing page of **GRAIN-01**, an open-source, near real-time voice layer for Windows desktop.

The website is engineered as a zero-dependency, ultra-lightweight web experience designed with a cyberpunk industrial design system featuring interactive signal path visualizations, real-time latency simulation benchmarks, dynamic RAM footprint gauges, and Web Audio synth integration.

---

## ✨ Features

- **Industrial & Retro-Futuristic Aesthetic**: Built with custom typography (Syne, JetBrains Mono, Inter), high-contrast dark palette, hardware-inspired rack modules, and glowing status LEDs.
- **Interactive Latency Benchmark**: Live comparative simulation demonstrating Grain's streaming transcription vs traditional record-first tools.
- **Signal Path Visualizer**: Interactive module breakdown for Audio Capture, Transcription, and LLM Processing layers.
- **Dynamic Memory Gauge**: Interactive RAM allocation preview showing idle (~100 MB) vs active peak states.
- **Web Audio Synth Engine**: Sound feedback on key interactions using native Web Audio API oscillators.
- **Particle Canvas Field**: Interactive background particle field responding to mouse cursor movement.
- **Zero Build Dependencies**: Pure HTML5, Vanilla CSS3, and ES6 JavaScript. No framework overhead.

---

## 📂 Repository Structure

```
website/
├── index.html     # Semantic page structure & landing page content
├── style.css      # Design system, layout grid, variables & animations
├── main.js        # Canvas canvas field, audio synth, interactive benchmarks
└── README.md      # Project documentation
```

---

## 🚀 Quick Start / Local Development

Since this project uses plain static files, no build step or node installation is required.

### Method 1: Direct File Opening
Double-click `index.html` or open it directly in any modern web browser.

### Method 2: Local HTTP Server (Recommended)
Using Python:
```bash
python -m http.server 8000
```
Using Node / `npx`:
```bash
npx serve .
```
Then navigate to `http://localhost:8000` in your web browser.

---

## 📄 Related Projects

- **[Grain Application Repository](https://github.com/Punit-Dethe/Grain)**: The main Rust (Tauri 2.0) + React desktop application codebase.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE) — free for personal and commercial use.
