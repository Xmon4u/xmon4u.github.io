# XMON4U — Interactive Audio-Visual Portfolio

[![Live Site](https://img.shields.io/badge/Live-xmon4u.github.io-blue.svg)](https://xmon4u.github.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

The official interactive web portfolio of **XMON4U**. An in-browser audio-visual experience combining real-time Web Audio API FFT frequency analysis with procedural Canvas2D and WebGL graphics.

## Features

- **Audio-Reactive Visualizers**: 12 selectable visualizer themes (Cyber, Neon Rain, Thunderstorm, Sakura, Frost, Solar Fire, and more) reacting dynamically to audio frequencies.
- **Soundtrack Integration**: 12 synchronized audio tracks with live spectrum analysis.
- **Dynamic Cursors & Shaders**: Hardware-accelerated particle effects and interactive pointer dynamics.
- **Zero External Frameworks**: Built using pure vanilla JavaScript, HTML5 Canvas2D, WebGL, and the Web Audio API.

## Running Locally

Because the Web Audio API and audio decoding require proper CORS headers, run the project through a local HTTP server rather than opening `index.html` via the `file://` protocol:

```bash
# Clone the repository
git clone https://github.com/Xmon4u/xmon4u.github.io.git
cd xmon4u.github.io

# Start a lightweight local server (Python 3)
python -m http.server 8080
```

Open [http://localhost:8080](http://localhost:8080) in any modern Chromium, Firefox, or Safari browser.

## Browser Support

Requires a modern browser with Web Audio API and HTML5 Canvas support (Google Chrome, Microsoft Edge, Mozilla Firefox, or Apple Safari).

## License

This project is licensed under the [MIT License](LICENSE).
