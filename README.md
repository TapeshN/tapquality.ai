# tapquality.ai

Landing site for **TapQuality LLC** — software, AI, and quality engineering built to a higher bar.

Static site, no build step. Implemented from a Claude Design export: the page is a
React component rendered client-side by `app.js` (the dc-runtime, which loads
React / ReactDOM / Babel from unpkg and transpiles the JSX in `index.html`),
styled with self-hosted Instrument Serif fonts.

## Structure

| Path | Purpose |
|---|---|
| `index.html` | Page shell + SEO head + the `<x-dc>` template and JSX component (Signal Green theme) |
| `app.js` | dc-runtime — parses `<x-dc>`, transpiles the JSX, mounts React |
| `fonts/` | Self-hosted woff2 (Instrument Serif + UI) |
| `favicon.svg` | Brand mark |

## Deploy

Hosted on Vercel, auto-deploys on push to `main`. Production domain: tapquality.ai.

## Local preview

    python3 -m http.server 8765

Then open http://127.0.0.1:8765
