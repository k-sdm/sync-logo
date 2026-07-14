# sync-logo

A browser playground for building a wordmark logo: type a word in **Eurostile Bold Extended** (or Helvetica Bold), then run it through an adjustable **gaussian blur → threshold** filter to get an ink-bloom / "exposure" effect.

Single self-contained `index.html` — no build step. Open it locally or visit the deployed version.

## Controls
- **Text / Font / Weight / Style / Size / Letter spacing** — the wordmark itself.
- **Per-letter spacing** — a slider for each gap between letters (kerning), applied before the filter so letters still fuse.
- **Gaussian blur / Threshold / Edge hardness** — the core effect: blur softens, threshold re-sharpens, hardness sets how crisp the cut is.
- **Colours / Background** — ink + background, with a transparent option.
- **Animate** — Blur, Threshold, and Size can oscillate between min/max bounds (eased ping-pong), with global speed + play/pause.
- **Trademark ™** — an optional ™ with its own blur + threshold, plus size, distance, and raise.
- **Letter paths — vector edit** — load the `.otf`/`.ttf` once (cached in `localStorage`) to outline the wordmark into editable Bézier paths, then drag anchor and control nodes per letter to reshape glyphs (e.g. to break up a blob where two letters fuse). Turn edit off to preview the effect; re-vectorize to bake a new size/kerning.
- **Export SVG / PNG** — vector (live text references the font by name; vectorized paths export as true outlines) or @2x raster.

> Fonts must be installed locally for live text to render, and loaded via the file picker for vector editing. Font files are gitignored — not redistributed.

Uses [opentype.js](https://github.com/opentypejs/opentype.js) (vendored, `opentype.min.js`) for glyph outline extraction.
