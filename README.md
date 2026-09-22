# Lilian Bialokozowicz — personal writing hub

A professional website + blog built as a [Jekyll](https://jekyllrb.com/) site,
designed to be hosted for free on **GitHub Pages**. Following GitHub's
[Pages quickstart](https://docs.github.com/en/pages/quickstart).

Once deployed it will live at: **https://drlilian.github.io**

---

## What's in here

| Path | What it is |
|------|-----------|
| `_config.yml` | Site settings — title, tagline, your links. **Edit this first.** |
| `index.html` | Homepage: your intro + list of posts. |
| `about.md` | Your About page. Edit the bio. |
| `_posts/` | Your blog posts (one Markdown file each). |
| `_layouts/` | Page templates (default, post, page). Rarely need editing. |
| `assets/css/style.css` | The site's styling. |
| `Gemfile` | Only for optional local preview. Not needed to deploy. |

---

## Deploy to GitHub Pages (one time, ~10 min)

1. **Create the repository.** On GitHub, click **＋ → New repository**.
   Name it **exactly** `DrLilian.github.io` (this exact name is what makes it a
   personal site served at the root URL). Set it to **Public**. You can leave
   "Add a README" unchecked since this folder already has one.

2. **Upload these files to the repo.** Two easy options:

   - **Web upload:** on the empty repo page, click *"uploading an existing file"*
     and drag in everything from this folder (including the `_config.yml`,
     `_posts`, `_layouts`, `assets`, etc.), then **Commit**.

   - **Command line** (from this `Website` folder):
     ```bash
     git init
     git add .
     git commit -m "Initial site"
     git branch -M main
     git remote add origin https://github.com/DrLilian/DrLilian.github.io.git
     git push -u origin main
     ```

3. **Enable Pages.** In the repo, go to **Settings → Pages**. Under **Source**,
   choose **Deploy from a branch**, pick branch **`main`** and folder **`/ (root)`**,
   then **Save**.

4. **Wait ~1–10 minutes**, then open **https://drlilian.github.io**. Done.

> After the first deploy, every time you push a change (or edit a file on
> github.com), the site rebuilds and republishes automatically.

---

## Write a new post

Add a file to `_posts/` named `YYYY-MM-DD-a-short-slug.md`, starting with:

```yaml
---
layout: post
title: "Your post title"
date: 2026-10-01
tags: [software, research]
---
```

Write the body in Markdown below that block. Commit/push and it appears on the
homepage automatically, newest first.

---

## Before you go live — quick checklist

- [ ] `_config.yml`: fill in `email`, `linkedin_username`, `scholar_url` (or
      leave `""` to hide them). `github_username` is already set to `DrLilian`.
- [ ] `about.md`: replace the placeholder bio with your own.
- [ ] Delete or rewrite the two sample posts in `_posts/`.

---

## Optional: preview locally before pushing

You only need this if you want to see changes on your own machine first.
Requires [Ruby](https://jekyllrb.com/docs/installation/windows/). Then:

```bash
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000. GitHub Pages does the real build for you, so this
step is entirely optional.
