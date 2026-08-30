# TypeLab

A focused typing trainer and browser-based utility shelf deployed automatically using GitHub Pages.

## Features

- Monkeytype-inspired typing practice with configurable 30/60/120 second sessions
- Live WPM, accuracy, and completed-test stats
- Text case converter, word/character counter, and slug generator
- Local password generator, file inspector, and text-file downloader
- Live Markdown preview
- JSON formatter/minifier and Base64 encoder/decoder
- Responsive dark/light interface with no server or build step

Everything runs locally in the browser. Files and pasted content are not uploaded.

## Deployment

GitHub Actions deploys the site to GitHub Pages whenever changes land on `main`.

## Adding New Tools

The page is intentionally dependency-free. Add a navigation button and a `.tool-view`
section in `index.html`, then wire its controls in the bottom script.
