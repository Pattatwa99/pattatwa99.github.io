# Isaac F — Personal Blog

Minimalist personal blog and technical notebook built with [Hugo](https://gohugo.io/) and [PaperMod](https://github.com/adityatelange/hugo-PaperMod), deployed to GitHub Pages at **[pattatwa99.github.io](https://pattatwa99.github.io)**.

## ✍️ Writing a Post

To start a new blog post, simply create a Markdown file in `content/posts/`:

```bash
# Using Hugo CLI
hugo new posts/my-first-post.md
```

Or manually create a `.md` file inside `content/posts/` with standard front matter:

```markdown
---
title: "My First Post"
date: 2026-11-21
draft: false
tags: ["computing", "linux"]
summary: "A brief summary of the post."
---

Your post content here in Markdown.
```

When you publish a post in `content/posts/`, it automatically appears on the homepage feed, in the Posts list, in the chronological Archives, and in the fuzzy Search index.

## 💻 Local Preview

Run the local Hugo development server:

```bash
hugo server -D
```

Open `http://localhost:1313/` in your browser. Live reload is enabled automatically.

## 🚢 Deploying to GitHub Pages

Commit and push your changes to `master`:

```bash
git add .
git commit -m "Publish new post"
git push origin master
```

GitHub Actions will build and deploy the update to `pattatwa99.github.io` within seconds.
