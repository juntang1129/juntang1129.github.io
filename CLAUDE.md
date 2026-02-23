# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Academic portfolio website for Juntang Wang, built with Jekyll using the Academic Pages template (forked from Minimal Mistakes). Deployed to GitHub Pages at `www.qqgjyx.com`. Repository: `juntang1129/juntang1129.github.io`.

## Build & Development Commands

```bash
# Install Ruby dependencies (run first, or after Gemfile changes)
bundle install

# Local development server (auto-rebuilds on change, serves at localhost:4000)
bundle exec jekyll serve -l -H localhost

# Docker alternative
docker compose up

# Rebuild minified JavaScript (after editing JS in assets/js/)
npm run build:js
```

**Note:** `_config.yml` changes require restarting the Jekyll server.

## Architecture

### Static Site Generator
- **Jekyll** with Liquid templating, kramdown Markdown, Rouge syntax highlighting
- **SCSS** compiled to CSS (compressed), no CSS framework — custom SCSS based on Minimal Mistakes
- **JavaScript**: jQuery + FitVids + custom scripts, minified via uglify-js into `assets/js/main.min.js`

### Content Collections
Three Jekyll collections, each in its own `_<name>/` directory with markdown files containing YAML frontmatter:

| Collection | Directory | Output | Key Frontmatter |
|---|---|---|---|
| Publications | `_publications/` | `false` | `category` (books/manuscripts/conferences), `venue`, `paperurl`, `citation`, `anchor`, `featured`, `display_authors` |
| Teaching | `_teaching/` | `false` | `type`, `dateC`, `location` |
| Talks | `_talks/` | `true` | `venue`, `date`, `location` |

Publication categories are defined in `_config.yml` under `publication_category` (books, manuscripts, conferences). Publications and teaching entries are rendered inline on their respective pages (no individual entry pages).

### Layout Hierarchy
`_layouts/default.html` is the base. Other layouts (`single`, `talk`, `homepage`, `archive`) extend it. Reusable components live in `_includes/` (author-profile, header, footer, navigation, sidebar). The homepage, publications, projects, and more pages all use `layout: homepage` for consistent Palatino serif styling at 820px max-width.

### Styling
SCSS lives in `_sass/` with this structure:
- `vendor/` — breakpoint mixins, susy grid, font-awesome
- `layout/` — component styles (masthead, navigation, sidebar, page, archive, etc.)
- `theme/` — theme variants (default_light, default_dark)
- `include/` — mixins and utilities

Entry point: `assets/css/main.scss`. Theme configured via `site_theme` in `_config.yml` (currently "default").

### Navigation
Header links are controlled by `_data/navigation.yml`. Currently active: Publications, Projects, More. Others (Teaching, Talks, Blog) are commented out.

### Key Configuration
- `_config.yml` — site metadata, author info, collection definitions, plugin list, defaults
- `_data/navigation.yml` — header navigation links
- `_data/authors.yml` — author metadata
- `CNAME` — custom domain (`www.qqgjyx.com`)

### Theme System
Supports light/dark mode with localStorage persistence. Theme variants are in `_sass/theme/`. Toggle logic is in `assets/js/theme.js` and `assets/js/_main.js`.

## Known Gotchas

- `_includes/base_path` resolves to `site.baseurl` (empty string for root-hosted site), giving root-relative asset paths like `/images/foo.webp`. Do NOT revert to `site.url | append: site.baseurl` — that hardcodes the production domain and breaks local dev.
- MathJax, Plotly, and Mermaid are **opt-in per page** via frontmatter (`mathjax: true`, `plotly: true`, `mermaid: true`). Do not add them globally — they are ~2MB of JS loaded on every page.
- OneDrive may silently convert `.webp` files to `.jpg`. If `images/profile.webp` disappears, regenerate: `magick ~/Downloads/profile.png -strip -quality 85 -define webp:method=6 images/profile.webp`

## Redesign Tracking

- `TODO.md` — phased redesign roadmap (Phases 0–8), check off items as completed
- `CUSTOMIZATIONS.md` — tracks all changes from upstream AcademicPages template
