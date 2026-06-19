---
title: "OpenEBench Embeddable Benchmarking Widget"
date: 2018-05-01
summary: "Sole-author d3.js radial arc widget for the ELIXIR European scientific benchmarking platform, embeddable on any scientific tool website."
---

Sole author of the embeddable benchmarking widget for **OpenEBench**, the ELIXIR European scientific benchmarking platform at **BSC**. Any scientific tool registered in OpenEBench can embed the widget on its own website to display live performance metrics with a single `<script>` tag.

## Key Contributions

- **Widget Design:** Built a configurable radial arc widget displaying scientific tool benchmarking metrics from the OpenEBench API — supports configurable size (50–500 px), tooltips, uptime plot, radial gradient arcs, and a "benchmarking not available" badge.
- **7-Iteration Evolution:** Iterated through 7 design versions (each as a git branch): from basic arc visualization → library isolation and cross-browser fixes → full Webpack build system → real JSON API integration and radial gradients.
- **Bundle Optimization:** Introduced Webpack 4 to tree-shake d3.js from 30 submodules down to 3 (d3-hierarchy, d3-selection, d3-shape), reducing the production bundle from 1.5 MB to 216 KB (UglifyJS).
- **Zero-friction Embedding:** A website integrates it with one `<div class="opeb" data-id="tool-id">` + one `<script>` tag — no build step required by consumers.

**Technologies:** JavaScript · d3.js · Webpack 4 · Yarn · UglifyJS · AGPL-3.0.
