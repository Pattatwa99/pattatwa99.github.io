# Isaac Fischer — Personal Portfolio & Blog

Personal website and blog built with [Hugo](https://gohugo.io/) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, deployed to GitHub Pages at **[pattatwa99.github.io](https://pattatwa99.github.io)**.

## 🚀 Features

- **Profile Mode Landing Page:** Showcasing avatar (`forg.gif`), bio, quick navigation, and social links.
- **Dark / Light Mode:** Automatic system preference detection with a manual toggle button.
- **Projects Showcase:** Dedicated `/projects/` section for software, tools, and experiments.
- **Blog & Articles:** Markdown-based blogging with syntax highlighting, copy code buttons, and reading time.
- **Client-Side Search:** Instant fuzzy search powered by Fuse.js at `/search/`.
- **Chronological Archive:** Tagged and dated posts index at `/archives/`.
- **Automated CI/CD:** GitHub Actions workflow in `.github/workflows/deploy.yml` automatically builds and deploys to GitHub Pages on push.

## 💻 Local Development

Hugo is installed locally. To preview the site:

```bash
# Start local Hugo development server with drafts included
hugo server -D
```

Then open `http://localhost:1313/` in your browser.

## 🛠️ Building

To generate the static production site:

```bash
hugo --gc --minify
```

The compiled static files are generated in the `./public` directory.

## 🚢 Deployment to GitHub Pages

1. In your GitHub repository settings under **Settings > Pages**:
   - Set **Source** to **GitHub Actions**.
2. Commit and push your changes:
   ```bash
   git add .
   git commit -m "Update site content"
   git push origin master
   ```
3. GitHub Actions will automatically run the build and publish the site.
