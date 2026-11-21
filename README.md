# Isaac F — Personal Website & Technical Notebook

Personal site and technical notebook built with [Hugo](https://gohugo.io/) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, deployed to GitHub Pages at **[pattatwa99.github.io](https://pattatwa99.github.io)**.

## 📌 Architecture & Design

- **Home Page:** Displays an introduction as a Computing Enthusiast along with the latest posts from the **Writing** section.
- **Writing:** Long-form technical explanations, development logs, and tutorials (`content/writing/`).
- **Notes:** Shorter technical observations, commands, references, and things learned (`content/notes/`).
- **About:** Personal background, technical interests, and contact information (`content/about.md`).
- **Search:** Client-side fuzzy search powered by Fuse.js at `/search/`.
- **Styling:** Technical minimalism with dark mode by default (`#171923` bg, `#222735` surface, `#4F8FA8` accent), with a light mode toggle available.
- **CI/CD:** Automated GitHub Actions workflow in `.github/workflows/deploy.yml` deploys on push to `master`.

## 💻 Local Development

Hugo is installed locally. To run the development server:

```bash
hugo server -D
```

Then visit `http://localhost:1313/` in your browser.

## 📝 Creating New Content

To create a new writing post:
```bash
hugo new writing/my-new-post.md
```

To create a new note:
```bash
hugo new notes/my-quick-note.md
```

## 🛠️ Building for Production

```bash
hugo --gc --minify
```

Outputs static files to the `./public` folder.

## 🚢 Deployment

1. Under GitHub repository **Settings > Pages**, set **Source** to **GitHub Actions**.
2. Commit and push your changes:
   ```bash
   git add .
   git commit -m "Add new post"
   git push origin master
   ```
GitHub Actions will automatically build and publish to `pattatwa99.github.io`.
