# TypeLab

An offline-friendly typing platform and personal developer utility suite deployed automatically using GitHub Pages.

## Features

- Timed typing practice with live WPM, raw WPM, accuracy, errors, backspaces, and persistent history
- Typing records, performance summaries, keyboard analytics, and portable JSON backups
- Hash-routed tool pages with a global Ctrl/Cmd+K command palette
- Text analysis, case/naming conversion, find-and-replace, and text diff
- JSON validation/formatting, regex testing, Base64/URL encoding, and a local JavaScript playground
- Timestamp, unit, percentage, color, contrast, palette, file, random, and CS experiment tools
- Dark/light theme, responsive layout, keyboard navigation, and toast feedback

Everything runs locally in the browser. Files, pasted content, and typing history are not uploaded.
The versioned export format is:

```json
{
  "schemaVersion": 1,
  "exportedAt": "...",
  "settings": {},
  "typingHistory": [],
  "favorites": [],
  "recent": []
}
```

## Deployment

GitHub Actions deploys the site to GitHub Pages whenever changes land on `main`.

## Adding New Tools

The page is intentionally dependency-free. Add a metadata entry to `toolMeta`, a renderer
to `views`, and a binder to `bindView` in `app.js`. Reuse the existing cards, fields, result
panels, `go()`, `copy()`, `download()`, and `toast()` helpers so the new tool participates
in routing, search, share links, and the shared visual system.
