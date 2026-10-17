# Audio Visualizer Studio

A client-side audio visualizer built with vanilla HTML, CSS and JavaScript. Designed for GitHub Pages — no build step, backend, or account required.

## Features

- Spectrum bars, waveform, radial spectrum, pulsing dots, full-canvas fireflies, cyberpunk grid and neon ring.
- Frequency range controls, bass boost, FFT size, sensitivity, smoothing, density, glow and animation speed.
- Aspect ratios: 16:9, 9:16, 1:1, 4:3, 21:9 and custom dimensions.
- PNG frame export, WebM recording, color controls, transparent canvas and chroma-green backgrounds.
- Audio files stay in the browser; no upload service is used.

## Run locally

Open `index.html` in a modern browser, or serve the folder with any static HTTP server.

## Publish with GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Choose branch **main** and folder **/(root)**, then save.
4. Wait for the deployment status/link to appear.

## Export notes

PNG snapshots preserve alpha transparency. Video recording uses the browser's MediaRecorder and WebM support varies by browser and editor; alpha-channel preservation is not guaranteed. For a dependable transparent video workflow, verify the exported codec in your editor or use a chroma-green background. Video is recorded in real time, so audio duration determines export duration.

## Privacy

Audio is loaded with a local object URL and processed through the Web Audio API. The app does not upload tracks to a server.
