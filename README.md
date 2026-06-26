# sync-logo

A browser playground for building a wordmark logo: type a word in **Eurostile Bold Extended** (or Helvetica Bold), then run it through an adjustable **gaussian blur → threshold** filter to get an ink-bloom / "exposure" effect.

Single self-contained `index.html` — no build step. Open it locally or visit the deployed version.

## Controls
- **Text / Font / Weight / Style / Size / Letter spacing** — the wordmark itself.
- **Per-letter spacing** — a slider for each gap between letters (kerning), applied before the filter so letters still fuse.
- **Gaussian blur / Threshold / Edge hardness** — the core effect: blur softens, threshold re-sharpens, hardness sets how crisp the cut is.
- **Colours / Background** — ink + background, with a transparent option.
- **Trademark ™** — an optional ™ with its own blur + threshold, plus size, distance, and raise.
- **Export SVG / PNG** — vector (font referenced by name) or @2x raster.

> Fonts must be installed locally for the browser to render them.
