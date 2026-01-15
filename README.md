# Blog

Personal blog powered by Hugo + PaperMod theme.

## Dodanie nowego posta

1. Stwórz plik `content/posts/nazwa-posta.md`
2. Dodaj frontmatter:
```yaml
---
title: 'Tytuł posta'
date: 2026-01-15
draft: false
tags: ['tag1', 'tag2']
---
```
3. Push do main → automatyczny deploy

## Lokalne preview

```bash
hugo server -D
```

## Deploy

Automatyczny via GitHub Actions → GitHub Pages

URL: https://beardless.github.io/blog/
