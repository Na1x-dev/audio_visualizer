# Audio Visualizer Studio

A client-side audio visualizer built with vanilla HTML, CSS and JavaScript. Designed for GitHub Pages — no build step, backend, or account required.

## Project structure

```text
audio_visualizer/
├── index.html          # Page markup and UI structure
├── css/
│   └── styles.css      # Theme, layout, responsive styles
├── js/
│   └── app.js          # Audio analysis, effects, controls and export
├── .github/
│   └── workflows/
│       └── pages.yml   # GitHub Pages deployment workflow
└── README.md
```

Keep responsibilities separate when extending the project:
- **HTML** — add or rearrange interface elements in `index.html`.
- **CSS** — change appearance and responsive behavior in `css/styles.css`.
- **JavaScript** — update visualizer behavior and interactions in `js/app.js`.

## Features

- Spectrum bars, waveform, radial spectrum, pulsing dots, full-canvas fireflies, cyberpunk grid and neon ring.
- Frequency range controls, bass boost, FFT size, sensitivity, smoothing, density, glow and animation speed.
- Aspect ratios: 16:9, 9:16, 1:1, 4:3, 21:9 and custom dimensions.
- PNG frame export, WebM recording, color controls, transparent canvas and chroma-green backgrounds.
- Audio files stay in the browser; no upload service is used.

## Run locally

Open `index.html` in a modern browser, or serve the folder with any static HTTP server. For example, with Python installed, run `python -m http.server` from the project directory and open `http://localhost:8000`.

## Publish with GitHub Pages

The repository includes a GitHub Actions workflow at `.github/workflows/pages.yml`.

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.
3. Open the **Actions** tab and wait for the Pages workflow to complete successfully.
4. The site should then be available at https://na1x-dev.github.io/audio_visualizer/.

## Export notes

PNG snapshots preserve alpha transparency. Video recording uses the browser's MediaRecorder and WebM support varies by browser and editor; alpha-channel preservation is not guaranteed. For a dependable transparent video workflow, verify the exported codec in your editor or use a chroma-green background. Video is recorded in real time, so audio duration determines export duration.

## Privacy

Audio is loaded with a local object URL and processed through the Web Audio API. The app does not upload tracks to a server.
