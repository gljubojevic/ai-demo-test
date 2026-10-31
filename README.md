# AI Demo Scene demo generation
Experiment generating Demo Scene demos using AI vibe coding

**Live site (GitHub Pages):** [https://gljubojevic.github.io/ai-demo-test/](https://gljubojevic.github.io/ai-demo-test/)

## Example 1 — Three.js 3D vibe demo

A single-file browser demo built iteratively with AI vibe coding, implemented in [`example1.html`](example1.html). Open it directly in any modern browser (no build step, no server needed — it loads Three.js 0.160.0 from a CDN via an ES module import map).

The scene contains:

- 1000 dark-red metallic rounded cubes distributed over a Fibonacci sphere (radius 9) via `RoundedBoxGeometry`.
- 3D extruded scrolling text in the Google Font **Orbitron** on a circle (XZ plane, radius 4.5) around the scene center, driven by real font metrics (opentype.js): empty-circle start, letters enter one by one at the far point in reading order, and the stream repeats seamlessly once the last letter enters.
- A bold chrome center title **"Cyberlabs"** (wght 900) with live reflections of the rotating cube shell and scrolling glyphs (two `CubeCamera` cubemaps).
- Two fast-rotating, glowing green ring bands around the title with a rapid uneven flicker, rendered through selective-bloom post-processing (`UnrealBloomPass` + EffectComposer).
- Mouse camera controls (OrbitControls: orbit, zoom, pan) with a key light that follows behind the camera.

The full specification — every feature, all parameter values, and the complete history of 32 instruction changes — is documented in [`example1.md`](example1.md).

[`index.html`](index.html) is the project landing page: a short description of Example 1, a screenshot (stored in `img/example1.png`), and links to the demo and this documentation.
