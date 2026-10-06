# GRAIN— Official Landing Page & Web Portal

[![License: MIT](https://img.shields.io/badge/License-MIT-000000.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Grain Repository](https://img.shields.io/badge/Grain-Core_Repository-blue?style=flat-square&logo=github)](https://github.com/Punit-Dethe/Grain)

[Experimental Vercel Website](https://usegrain.vercel.app/) | [Main Application Repository](https://github.com/Punit-Dethe/Grain)

---

## Overview

This repository houses the source code for the official landing page of **GRAIN-01**, an open-source, near real-time voice layer designed for desktop environments.

The site is built as a zero-dependency, lightweight web application implementing an industrial hardware-inspired interface. It features interactive signal routing visualizers, real-time streaming latency benchmarks, dynamic memory utilization gauges, and native Web Audio synthesis.

---

## Technical Highlights

- **Industrial UI & Layout Architecture**: Built using a dark high-contrast design system, typography optimized for code and technical data (Syne, JetBrains Mono, Inter), modular rack component panels, and status indicators.
- **Streaming vs. Batch Latency Simulation**: An interactive benchmark comparing streaming audio processing against conventional record-and-transcribe workflows.
- **Modular Signal Path Visualization**: Interactive breakdown of the capture, transcription, and post-processing pipeline layers.
- **Resource Footprint Preview**: Interactive gauge rendering low-idle memory allocation profiles (~100 MB idle).
- **Web Audio Signal Feedback**: Direct synthesizer feedback implemented using standard Web Audio API audio nodes.
- **Interactive Particle Field**: Canvas-based reactive particle renderer.
- **Framework-Independent**: Pure HTML5, CSS3, and ES6 JavaScript with zero external runtime or build dependencies.

---

## Repository Structure

```
Grain-Website/
├── index.html     # Semantic page structure and core copy
├── style.css      # Design system tokens, layout system, typography, and styling
├── main.js        # Canvas background mechanics, benchmark engine, synth logic
└── README.md      # Repository documentation
```

---

## Local Development

Because the site relies exclusively on standard Web APIs and static assets, no build steps or dependencies are required.

### Direct Execution
Open `index.html` directly in any web-standard compliant browser.

### Static HTTP Server

Using Python 3:
```bash
python -m http.server 8000
```

Using Node.js:
```bash
npx serve .
```

Access the local instance at `http://localhost:8000`.

---

## Public MCP client document (provisional hosting)

`oauth/client.json` is public OAuth application metadata for the native Grain
client. It contains no credentials, tokens or account information. Its candidate
identity is exactly `https://usegrain.vercel.app/oauth/client.json`; a Vercel
commit/branch preview URL is not that identity. The local loopback callback stays
inside Grain, and this website is not a token exchange server or MCP gateway.

`vercel.json` sets JSON content type, a five-minute revalidation cache policy and
`nosniff` on this path only. No landing-page code, routing rewrite, function,
database or website build dependency is added. The endpoint must be public without
Vercel login/challenges and must return direct HTTP 200, without redirects.

From the co-located Grain checkout, validate the exact candidate and, after
production deployment, the actual public endpoint:

```powershell
node scripts/check-mcp-client-metadata.mjs https://usegrain.vercel.app/oauth/client.json --file website/oauth/client.json
node scripts/check-mcp-client-metadata.mjs https://usegrain.vercel.app/oauth/client.json --live
```

Publishing this file does not enable it in Grain: its host-owned client metadata
URL remains disabled until separate endpoint verification and provider acceptance.
The user approved the existing site as provisional hosting on 6 October 2026; it
is not an official permanent domain decision.

Move the same static file to another host without changing the document URL if
possible. A stable Grain-owned domain would permit changing the hosting behind
it. Replacing this `vercel.app` identity with a new domain changes `client_id`:
update the document and Grain together, verify provider support, and expect that
some providers may require new consent/registration. Keep the old document and
old registrations available during transition rather than redirecting/removing
the endpoint. Provider behavior and refresh continuity need actual acceptance;
no transparent migration is promised.

The signed extension registry belongs to a separate deployment with its own
reviewed snapshots and release controls; landing-page deployments do not publish
catalogues or hold registry signing keys. See Grain's
`docs/Extensions 2.0/EXTENSION-HOSTING-DECISION.md` for the hosting/migration plan.

## Related Repositories

- **[Grain Desktop Application](https://github.com/Punit-Dethe/Grain)**: The primary Rust (Tauri) and React codebase for the GRAIN-01 application.

---

## License

Distributed under the [MIT License](LICENSE).
