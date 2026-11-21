---
title: "Seamless Hugo Deployments with GitHub Pages and Actions"
date: 2026-11-21
tags: ["GitHub Actions", "Hugo", "CI/CD", "WebDev"]
summary: "How to configure automated, friction-free static site deployment using GitHub Actions."
---

Deploying a Hugo site to GitHub Pages is as straightforward as it gets. With GitHub's native `actions/deploy-pages`, you don't even need third-party push tokens or complicated branches.

### The Deployment Pipeline

Here is the GitHub Actions workflow running behind this site:

```yaml
name: Deploy Hugo site to Pages

on:
  push:
    branches: ["master", "main"]
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
        with:
          submodules: recursive
          fetch-depth: 0

      - name: Setup Hugo
        uses: peaceiris/actions-hugo@v3
        with:
          hugo-version: 'latest'
          extended: true

      - name: Build with Hugo
        run: hugo --gc --minify

      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./public

  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

Whenever changes are committed and pushed, GitHub Actions handles the rest in under 30 seconds.
