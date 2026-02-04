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
Four Jekyll collections, each in its own `_<name>/` directory with markdown files containing YAML frontmatter:

| Collection | Directory | Layout | Key Frontmatter |
|---|---|---|---|
| Publications | `_publications/` | `single` | `category` (books/manuscripts/conferences), `venue`, `paperurl`, `citation` |
| Teaching | `_teaching/` | `single` | `type`, `venue` |
| Talks | `_talks/` | `talk` | `venue`, `date`, `location` |
| Portfolio | `_portfolio/` | `single` | standard |

Publication categories are defined in `_config.yml` under `publication_category` (books, manuscripts, conferences).

### Layout Hierarchy
`_layouts/default.html` is the base. Other layouts (`single`, `talk`, `splash`, `cv-layout`, `archive`) extend it. Reusable components live in `_includes/` (author-profile, header, footer, navigation, sidebar).

### Styling
SCSS lives in `_sass/` with this structure:
- `vendor/` — breakpoint mixins, susy grid, font-awesome
- `layout/` — component styles (masthead, navigation, sidebar, page, archive, etc.)
- `theme/` — theme variants (default_light, default_dark, air_light, air_dark)
- `include/` — mixins and utilities

Entry point: `assets/css/main.scss`. Theme configured via `site_theme` in `_config.yml` (currently "default").

### Navigation
Header links are controlled by `_data/navigation.yml`. Currently active: Publications, Teaching, CV, Projects. Others (Talks, Portfolio, Blog) are commented out.

### Key Configuration
- `_config.yml` — site metadata, author info, collection definitions, plugin list, defaults
- `_data/navigation.yml` — header navigation links
- `_data/authors.yml` — author metadata
- `CNAME` — custom domain (`www.qqgjyx.com`)

### Content Generation
`markdown_generator/` contains Python scripts and Jupyter notebooks to auto-generate publication/talk markdown from TSV files.

### Theme System
Supports light/dark mode with localStorage persistence. Theme variants are in `_sass/theme/`. Toggle logic is in `assets/js/theme.js` and `assets/js/_main.js`.
