# Live-Code-Editor

A lightweight, client-side live HTML / CSS / JavaScript code editor. Write markup, styles, and scripts in separate editor panes and see the output rendered instantly in a live preview iframe — no build step, no server, no login.

## Features

- **Three editor panes** — HTML, CSS, and JavaScript editors side by side
- **Live preview** — output re-renders automatically as you type (`updatePreview`)
- **Resizable layout** — drag the resizer handle to adjust editor vs. preview widths
- **Load from file** — open a local file into the editor (`file-loader`)
- **Tabbed interface** — switch between editors via tabs
- **Dark slate UI** — Inter + Fira Code fonts, styled with Tailwind CSS (CDN)
- **Two variants included** — `index.html` (tabbed editor with resizable preview) and `basic.html` (simpler editor layout)
- **100% client-side** — runs entirely in the browser; nothing is sent anywhere

## Tech stack

- HTML, CSS, JavaScript (vanilla, no framework)
- Tailwind CSS via CDN (`cdn.tailwindcss.com`)
- Google Fonts (Inter, Fira Code)

## Quick start

### Option 1 — open directly

1. Download or clone this repo.
2. Open `index.html` (or `basic.html`) in any modern browser. That's it.

### Option 2 — run the live site

Visit the deployed site (see the homepage link on the repo page) — type code on the left, watch it render on the right.

## Project structure

```
Live-Code-Editor/
├── index.html    # Tabbed editor + resizable live preview (main)
├── basic.html    # Simpler single-view editor layout
└── README.md     # This file
```

## How it works

The editors feed their contents into `updatePreview()`, which composes an HTML document from the HTML / CSS / JS panes and loads it into the preview `<iframe>` (`preview-frame`). Dragging the `resizer` adjusts the editor/preview split via mouse events. The `load-file-btn` uses a hidden `<input type="file">` to load local files into the active editor.

## Deploy

The site is fully static, so it deploys to any static host: GitHub Pages, Cloudflare Pages, Netlify, or Vercel — no configuration required, just serve the repo root.

---

Built by [Girish Lade](https://ladestack.in)
