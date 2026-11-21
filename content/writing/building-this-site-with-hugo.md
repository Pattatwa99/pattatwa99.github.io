---
title: "Building This Site with Hugo and GitHub Pages"
date: 2026-11-21
tags: ["Hugo", "GitHub Pages", "Web", "Static Site"]
summary: "How I set up a minimal, fast, and maintainable personal site using Hugo and PaperMod."
---

When setting up this site, I wanted an environment that was fast to build, simple to write in, and devoid of unnecessary web bloat.

### Goals

1. **Speed & Simplicity:** Compiling Markdown in milliseconds using Hugo.
2. **Readability:** Clean typography and native dark/light modes using the PaperMod theme.
3. **Automated Deployment:** Committing changes directly publishes to GitHub Pages via GitHub Actions with zero manual build steps.

### Architecture

The site uses:
- **Hugo Extended** as the static site engine.
- **PaperMod** for responsive, content-first presentation.
- **GitHub Actions** for CI/CD triggered on git pushes to the master branch.

By keeping dependencies minimal and avoiding complex front-end pipelines, writing and publishing stays focused purely on content.
