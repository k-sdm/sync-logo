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
- **Letter paths — vector edit** — the bundled `eurostile-bold-extended.otf` auto-loads (file picker overrides it; picked fonts cache in `localStorage`). Vectorize outlines the wordmark into editable Bézier paths: drag anchor and control nodes to reshape glyphs (e.g. to break up a blob where two letters fuse), per letter or **All** at once. **Mirror bezier arms** keeps joints smooth (Angle) or fully symmetric (+Length) while dragging a handle. **Undo** (⌘Z) steps back through drags and re-vectorizes. Turn edit off to preview the effect; re-vectorize to bake a new size/kerning.
- **Export SVG / PNG** — vector (live text references the font by name; vectorized paths export as true outlines) or @2x raster.

> The wordmark font must also be installed locally for live-text mode to render it.

Uses [opentype.js](https://github.com/opentypejs/opentype.js) (vendored, `opentype.min.js`) for glyph outline extraction.
