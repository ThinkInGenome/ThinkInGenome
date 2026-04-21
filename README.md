# Thinking in Genomes — Custom Jekyll Theme

A clean, editorial Jekyll theme built for the Thinking in Genomes blog.

## Deploying to GitHub

### Step 1 — Replace files in your repo

Copy the following files/folders from this package into the root of your `ThinkInGenome` repository, **replacing** any existing versions:

```
_config.yml          ← replaces the Chirpy config
Gemfile              ← replaces the Chirpy Gemfile
_layouts/            ← new folder (or replace contents)
assets/css/main.css  ← new CSS (replaces Chirpy assets)
index.html           ← replaces existing index
about.md             ← replaces existing about page
entries.html         ← new page
topics.html          ← new page
.github/workflows/pages.yml  ← new or replace existing
```

### Step 2 — Delete Chirpy-specific files

Remove these files/folders if they exist in your repo (they belong to Chirpy and will conflict):

```
_data/
_plugins/
_tabs/
_sass/
assets/js/
assets/css/jekyll-theme-chirpy.scss (or similar)
Gemfile.lock  ← delete this so it regenerates cleanly
```

### Step 3 — Enable GitHub Actions deployment

1. Go to your repo on GitHub → **Settings** → **Pages**
2. Under "Build and deployment", set **Source** to **GitHub Actions**
3. Push your changes — the workflow will build and deploy automatically

### Step 4 — Check your existing posts

Your existing posts in `_posts/` will work as-is. The `_config.yml` sets a default layout of `post` for all posts, so you don't need `layout: post` in every file's front matter (though leaving it in won't cause problems).

Make sure each post has at least:
```yaml
---
title: "Your post title"
date: YYYY-MM-DD
categories: [category-name]
---
```

### Local development

```bash
bundle install
bundle exec jekyll serve
# Visit http://localhost:4000/ThinkInGenome/
```

## Writing new posts

Create files in `_posts/` with the format `YYYY-MM-DD-title.md`:

```markdown
---
title: "How do we detect selection acting on genomic variants?"
date: 2026-03-01
categories: [comparative-genomics]
tags: [selection, fst, population-genomics]
excerpt: "Not all variants are equal. Some are neutral passengers; others are under active selection..."
---

Your post content here in Markdown.
```

Posts are automatically numbered in reverse chronological order on the homepage and entries page.
