# Thinking in Genomes

A custom Jekyll theme for the Thinking in Genomes blog.

## Writing new posts

Create files in `_posts/` with the format `YYYY-MM-DD-title.md`:

```markdown
---
title: "Your post title"
date: 2026-03-01
categories: [comparative-genomics]
tags: [selection, fst]
excerpt: "A short summary shown on the homepage..."
---

Your post content here in Markdown.
```

Posts are automatically numbered in reverse chronological order.

## Local development

```bash
bundle install
bundle exec jekyll serve
# Visit http://localhost:4000/ThinkInGenome/
```
