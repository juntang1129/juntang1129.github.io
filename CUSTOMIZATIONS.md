# Customizations vs. Upstream AcademicPages

This document tracks all changes made to the AcademicPages template during the website redesign. Use this when merging upstream updates (`git merge --squash`) to understand what was intentionally changed.

---

## Removed Files

### Phase 1 — Collections & Posts
- `_portfolio/` (2 sample files) — portfolio collection removed entirely
- `_posts/` (5 sample posts) — blog removed entirely
- `_drafts/` (1 draft) — drafts removed

### Phase 1 — Sample Data
- `_data/comments/` (7 yml files) — comment sample data removed

### Phase 1 — Pages
- `_pages/cv.md` — replaced by PDF-only CV (see Phase 7)
- `_pages/cv-json.md` — removed
- `_pages/portfolio.html` — portfolio collection removed
- `_pages/year-archive.html` — blog removed
- `_pages/talkmap.html` — talkmap feature removed
- `_pages/markdown.md` — upstream demo page, irrelevant
- `_pages/non-menu-page.md` — upstream demo page, irrelevant
- `_pages/archive-layout-with-content.md` — upstream demo page, irrelevant
- `_pages/terms.md` — upstream boilerplate, irrelevant

### Phase 1 — Includes
- `_includes/analytics.html` — no analytics provider configured
- `_includes/analytics-providers/` (directory) — no analytics provider configured
- `_includes/comments.html` — comments disabled
- `_includes/comment.html` — comments disabled
- `_includes/comments-providers/` (directory) — comments disabled
- `_includes/browser-upgrade.html` — IE upgrade prompt, unnecessary
- `_includes/post_pagination.html` — blog/post pagination removed
- `_includes/read-time.html` — read-time feature not used

### Phase 1 — SCSS Theme Variants
All non-default theme variants removed (only `default_light` + `default_dark` kept):
- `_sass/theme/air_light.scss`
- `_sass/theme/air_dark.scss`
- `_sass/theme/contrast_light.scss`
- `_sass/theme/contrast_dark.scss`
- `_sass/theme/dirt_light.scss`
- `_sass/theme/dirt_dark.scss`
- `_sass/theme/mint_light.scss`
- `_sass/theme/mint_dark.scss`
- `_sass/theme/sunrise_light.scss`
- `_sass/theme/sunrise_dark.scss`

### Phase 1 — Root Files
- `talkmap.ipynb` — talkmap notebook removed
- `talkmap.py` — talkmap script removed
- `talkmap/` — talkmap output directory removed
- `sitemap.xml` — manual sitemap removed (jekyll-sitemap plugin generates one)

### Capstone Review — Layouts & Assets
- `_layouts/cv-layout.html` — no pages use it; referenced non-existent `assets/css/cv-layout.css`
- `_layouts/archive-taxonomy.html` — no pages or config reference this layout
- `assets/css/collapse.css` — orphaned, never imported or referenced
- `assets/js/collapse.js` — orphaned, never referenced in any template
- `CONTRIBUTING.md` — AcademicPages upstream boilerplate
- `talkmap_out.ipynb` — auto-generated artifact (also added to `.gitignore`)

### Capstone Review — Placeholder Talk Files
All 4 AcademicPages template stubs deleted (dates 2012–2014, fake UC San Francisco venue):
- `_talks/2012-03-01-talk-1.md`
- `_talks/2013-03-01-tutorial-1.md`
- `_talks/2014-02-01-talk-2.md`
- `_talks/2014-03-01-talk-3.md`

### Template Cleanup
- `markdown_generator/` (entire directory) — template TSVs, notebooks, Python scripts; all content was "Your Name" placeholder
- `scripts/cv_markdown_to_json.py`, `scripts/update_cv_json.sh` — dead scripts for deleted `cv.md` workflow
- `_data/cv.json` — 100% placeholder data ("Your Sidebar Name", "GitHub University")
- `_includes/cv-template.html` — 310-line include for cv.json, not referenced by any active page
- `_includes/archive-single-cv.html` — CV-archive variant, not referenced
- `_includes/archive-single-CUSTOM-cv.html` — custom CV variant, not referenced
- `_includes/archive-single-talk-cv.html` — talk-CV variant, not referenced
- `_sass/layout/_json_cv.scss` — 240-line CV SCSS, compiled but unused (import removed from `main.scss`)
- `_pages/page-archive.html`, `collection-archive.html` — template utility pages
- `_layouts/splash.html` — no page uses `layout: splash`

---

## Modified Layouts

### `_layouts/default.html`
- Removed `{% include browser-upgrade.html %}` call

### `_layouts/single.html`
- Removed `{% include post_pagination.html %}` call
- Removed `{% include comments.html %}` call
- **Phase 2:** Removed `{% include sidebar.html %}` call
- **Phase 2:** Removed dead `read_time` guard block

### `_layouts/archive.html`
- **Phase 2:** Removed `{% include sidebar.html %}` call

### `_layouts/talk.html`
- Removed `{% include post_pagination.html %}` call
- Removed `{% include comments.html %}` call
- **Phase 2:** Removed `{% include sidebar.html %}` call
- **Phase 2:** Removed dead `read_time` guard block

---

## Modified Includes

### `_includes/masthead.html`
- Home link label: `{{ site.title }}` → `"Home"` (hardcoded string)

### `_includes/scripts.html`
- Removed `{% include analytics.html %}` call

### `_includes/archive-single.html`
- **Phase 2:** Removed dead `read_time` guard block

### `_includes/archive-single-talk.html`
- **Phase 2:** Removed dead `read_time` guard block

### `_includes/archive-single-cv.html`
- **Phase 2:** Removed dead `read_time` guard block
- **Template Cleanup:** File deleted (CV-archive variant, not referenced)

### `_includes/page__hero.html`
- **Phase 2:** Removed dead `read_time` guard block

---

## New Files

### Phase 3 — Homepage Redesign
- `_pages/about.html` — Min Liu–style homepage (renamed from `.md` to skip kramdown wrapping)

### Phase 2 — Layouts & SCSS
- `_layouts/homepage.html` — single-column skeleton for homepage (extends `default`)
- `_sass/layout/_homepage.scss` — `.homepage` wrapper: `max-width: 820px`, centered

### Phase 0 — Images & Favicon
- `images/profile.webp` — 800×800px, ~21KB, WebP q85, EXIF stripped
- `images/favicon.ico` — multi-size ICO (16×16, 32×32, 48×48)
- `images/favicon-192x192.png` — PWA icon
- `images/favicon-512x512.png` — PWA icon
- `images/apple-touch-icon-180x180.png` — iOS home screen icon
- `images/manifest.json` — PWA web app manifest

### Phase 1 — Pages
- `_pages/more.md` — "More" hub placeholder page

### Tracking Docs
- `TODO.md` — phased redesign roadmap (Phases 0–8)
- `CUSTOMIZATIONS.md` — this file

---

## Configuration Changes

### `_config.yml`
**Phase 2:**
- Changed all `author_profile: true` → `author_profile: false` in defaults (pages, teaching, publications, talks)

**Phase 1:**
- Removed `portfolio` collection definition
- Removed `_posts` and `_portfolio` entries from `defaults:`

**Capstone Review:**
- Fixed `analytics.provider: "false"` (truthy string) → `analytics.provider: false` (boolean)
- Removed `analytics.google.tracking_id` sub-keys (no provider set)
- Removed `comments:` block (all sub-keys empty, no provider)
- Removed `staticman:` block (16 lines, provider never set)
- Removed `read_more: "disabled"` (unused feature string)
- Removed `google_site_verification`, `bing_site_verification`, `alexa_site_verification`, `yandex_site_verification` (all empty)
- Removed `twitter: username:` block (empty; OG/social cards won't use it)
- Removed `social: type/name/links` block (all empty; JSON-LD won't fire)

**Kept intentionally:**
- `atom_feed:` block — feed.xml generated by jekyll-feed

**Capstone Review 2:**
- Removed `talkmap_link: false` (talkmap deleted in Phase 1, no longer referenced)
- Removed `jekyll-paginate` from `plugins:` and `whitelist:` (no blog)

### `assets/css/main.scss`
**Phase 2:** Added `@import "layout/homepage"` after `layout/page`

### `_sass/layout/_page.scss`
**Phase 2:**
- Replaced `.page` Susy `span(10 of 12)` grid block with `max-width: 820px; margin: auto`
- Removed `.page__related` `@include pre(2.5 of 12)` (sidebar offset, no longer needed)

### `_sass/layout/_archive.scss`
**Phase 2:**
- Replaced `.archive` Susy `span(12/10 of 12)` breakpoint blocks with `max-width: 820px; margin: auto`
- Removed `.list__item` sidebar padding breakpoints (`$right-sidebar-width-*`)

### `_sass/layout/_masthead.scss`
**Phase 2:**
- Replaced `.masthead__menu-item.selected` underline style with Yueqian-inspired pill buttons
- Inner nav items (not `--lg`, not `.tail`) get bordered pill with hover/active states via CSS vars

### `_pages/about.html` (was `about.md`)
**Phase 2:** Added `layout: homepage` to frontmatter
**Phase 3:** Renamed `.md` → `.html` (avoids kramdown `<p>` wrapping of block HTML). Full rewrite:
centred name, flex profile row (photo + bio), news list, Liquid-pulled featured publications
(`featured: true` in pub frontmatter), education row, footer credit.

### `_publications/*.md` (all 5)
**Phase 3:** Added `featured:`, `display_authors:` (HTML author list, self bolded), `award:` fields.

### `_layouts/homepage.html`
**Phase 3:** Added `{% include base_path %}` so `{{ base_path }}` resolves in `about.html` content.

### `_sass/layout/_homepage.scss`
**Phase 3:** Full expansion — profile flex, section headings, news, publication cards, education,
gradient HR divider, footer credit, responsive stack at ≤640px. All colors via CSS vars (dark-mode safe).

### `_data/navigation.yml`
- Trimmed to three active links: **Publications | Projects | More**
- Removed: Teaching, CV, Talks, Portfolio, Blog links

### `.gitignore`
- Added `talkmap_out.ipynb`

---

## Content Changes

### `README.md`
- Replaced AcademicPages template boilerplate with personal site content

### `_pages/about.html`
- Title links changed from external URLs (`paperurl`/`arxivurl`) to internal publication entry pages (`pub.url`)

### `_pages/publications.html`
- Added `redirect_from: /publications.html` to frontmatter

---

## Capstone Review 2 — Cleanup + Hover Color Fix

### Unified Harvard Crimson Hover
All link hover states now use Harvard Crimson (`$primary-color`) instead of a mix of darker Duke Blue, dark gray, and hardcoded `#000`.

**Theme variable changes:**
- `_sass/theme/_default_light.scss`: `--global-link-color-hover` → `#{$primary-color}` (was `mix(#000, #003087, 20%)`)
- `_sass/theme/_default_light.scss`: `--global-masthead-link-color-hover` → `#{$primary-color}` (was `mix(#000, $gray, 25%)`)
- `_sass/theme/_default_dark.scss`: `--global-link-color-hover` → `#{$primary-color}` (was `#{$link-dark}`)

**Added missing hover color** (`color: var(--global-link-color-hover)`) to selectors that only had underline:
- `_sass/layout/_homepage.scss`: `.hp-pub-links a:hover`
- `_sass/layout/_page.scss`: `.page__content a:hover`
- `_sass/layout/_footer.scss`: `.page__footer a:hover`
- `_sass/layout/_archive.scss`: `.archive a:hover`
- `_sass/layout/_sidebar.scss`: `.toc .toc__menu a:hover`, `.author__urls a:hover`

**Fixed hardcoded `#000` dark-mode bugs:**
- `_sass/layout/_navigation.scss`: `.toc__menu a:hover` color `#000` → `var(--global-bg-color)`
- `_sass/layout/_base.scss`: `figcaption a:hover` color/border `#000` → `var(--global-link-color-hover)`

### Bug Fix — Image Case Mismatch
- `_publications/2025-07-07-LK99-MC17.md`: `tRAMAN.png` → `tRaman.png` (matches actual filename on disk)

### Deleted Orphaned Files
- `_includes/feature_row` — never referenced by any layout or page
- `_includes/gallery` — never referenced by any layout or page
- `_includes/toc` — never referenced (sidebar TOC is inline in `_sidebar.scss`)
- `_includes/paginator.html` — never referenced (blog removed in Phase 1)
- `images/themes/homepage-air-dark.png` — air theme removed in Phase 1
- `images/themes/homepage-air-light.png` — air theme removed in Phase 1

### Config Cleanup
- `_config.yml`: Removed `talkmap_link: false` (talkmap deleted in Phase 1)
- `_config.yml`: Removed `jekyll-paginate` from `plugins:` and `whitelist:` (no blog)

### Data Cleanup
- `_data/authors.yml`: Removed template placeholder entries ("Name Name", "Name2 Name2")

### Footer Fix
- `_includes/footer/custom.html`: `/sitemap/` → `{{ base_path }}/sitemap/` (consistent with rest of site)

---

## Codebase Audit Fixes

### Critical — JS Bug Fix
- `assets/js/_main.js:19`: `userPref` (undefined) → `window.matchMedia` — crashed on any page with `plotly: true`

### Performance — Plotly Unbundled
- `package.json`: Removed `plotly.js-dist-min` from dependencies and uglify command
- `assets/js/main.min.js`: Bundle reduced from ~4.4 MB to ~93 KB
- Plotly is still available via CDN on pages with `plotly: true` frontmatter (loaded in `footer/custom.html`)

### High — Config + Security + A11y
- `Gemfile`: Removed orphaned `jekyll-paginate` gem (blog deleted in Phase 1)
- `_config.yml`: Removed deprecated `whitelist:` block (duplicated `plugins:` list)
- `_pages/projects.md`: Added `rel="noopener"` to 3 `target="_blank"` links
- `_sass/layout/_base.scss`: Added `@media (prefers-reduced-motion: reduce)` global query
- `_includes/masthead.html`: Added `aria-label="Toggle navigation"` and `aria-expanded="false"` to hamburger button

### Medium — Template + Markup Cleanup
- `_layouts/single.html`: Replaced 14 `style="font-size: smaller"` with `class="page__citation"`
- `_sass/layout/_page.scss`: Added `.page__citation { font-size: $type-size-6; }`
- `_includes/category-list.html`: Removed duplicate `{% include base_path %}`
- `_sass/layout/_sidebar.scss`: Removed duplicate `position: relative` in `.author__urls-wrapper`
- `_sass/layout/_base.scss`: Moved orphans/widows rules into `@media print` block (were applying globally)

---

## Constitution Enforcement

### New CSS Variables
Added to both `_default_light.scss` and `_default_dark.scss`:
- `--global-toc-bg-color` — TOC panel background (`#fff` light / `$background` dark)
- `--global-selection-color` — text selection foreground (`#fff` both themes)
- `--global-selection-bg` — text selection background (`$primary-color` both themes — Harvard Crimson)

### Selection Color Fix
- `_sass/layout/_reset.scss`: `::selection` and `::-moz-selection` changed from hardcoded `color: #fff; background: #000` to `color: var(--global-selection-color); background: var(--global-selection-bg)` — now white-on-Crimson in both themes

### TOC Background Fix
- `_sass/layout/_navigation.scss:388`: `.toc` `background-color: #fff` → `var(--global-toc-bg-color)` — was invisible white-on-white in dark mode

### Social Icons Fix
- `_sass/include/_utilities.scss:200`: `.social-icons .fa` `color: #000` → `var(--global-text-color)` — icons were invisible on dark backgrounds

### Sidebar Arrow Fix
- `_sass/layout/_sidebar.scss:299`: `.author__urls:after` `border-color: #fff transparent` → `var(--global-bg-color) transparent` — arrow matched light bg only

### Focus-Visible Upgrade
- `_sass/include/_mixins.scss`: `%tab-focus` body replaced — old `outline: 5px auto $warning-color` → `outline: 2px solid var(--global-link-color); outline-offset: 2px` (Duke Blue ring)
- `_sass/layout/_reset.scss:75`: `a:focus` → `a:focus-visible` — keyboard-only focus ring
- `_sass/layout/_base.scss:118`: `a:focus` → `a:focus-visible` — keyboard-only focus ring

---

## Phase 4 — Publications Page Redesign

### Design Decision
Dropped individual publication entry pages in favor of a flat bibliography list. Titles link directly to `paperurl` (arXiv/venue), matching the Barron/He/Liu pattern.

### New Files
- `_includes/pub-bib-entry.html` — bibliography-style entry include (authors, linked title, venue, year, award, resource links)
- `_sass/layout/_publications.scss` — SCSS for `.pub-bib`, `.pub-list-header`, award/link styling

### Modified Files

#### `_config.yml`
- `collections.publications.output`: `true` → `false` (no individual pages)
- `defaults.publications.share`: `true` → `false`
- `defaults.publications.comments`: `true` → `false`

#### `_pages/publications.html`
- Rewritten: removed category-grouped `archive-single.html` loop, replaced with flat reverse-chronological bibliography list using `pub-bib-entry.html`
- Header: dagger footnote + Google Scholar link
- `author_profile`: `true` → `false`

#### `_pages/about.html`
- Selected Publications: title links changed from `pub.url` (internal pages) → `pub.paperurl` (external); plain `<span>` fallback when no `paperurl`
- News section: internal `/publication/...` links → external `paperurl` URLs; MartianClock link removed (no `paperurl` yet)

#### `_publications/*.md` (×3)
- Stripped `permalink:` and `excerpt:` from frontmatter (unused with `output: false`)
- Stripped markdown body content (abstracts, figures, references) — frontmatter-only

#### `assets/css/main.scss`
- Added `@import "layout/publications"` after `layout/archive`

---

## Phase 4 Polish — Style Consistency + Anchor Links + MartianClock

### Design Decision
Switched `/publications/` from `layout: archive` (sans-serif system font) to `layout: homepage` (Palatino serif, 820px max-width) for visual consistency with homepage. Entries reuse `hp-pub-*` classes from `_homepage.scss`. Added anchor links so homepage paper titles navigate to exact entries on `/publications/`.

### Deleted Files
- `_includes/pub-bib-entry.html` — bib-style include replaced by inline card loop in `publications.html`

### Modified Files

#### `_pages/publications.html`
- `layout: archive` → `layout: homepage`
- Replaced `pub-bib-entry.html` include loop with inline card markup using `hp-pub-*` classes
- Each entry gets `id="{{ pub.anchor }}"` for anchor navigation
- Header uses `hp-section-heading` and `hp-note` classes (consistent with homepage)

#### `_pages/about.html`
- News: removed MartianClock item; InfantConfig + TempLK99 links changed from external URLs to `/publications/#anchor`
- Selected Publications: title links changed from `pub.paperurl` → `/publications/#{{ pub.anchor }}`
- Uncommented "only first and co-first authored papers are listed" note

#### `_publications/*.md` (×3)
- Added `anchor:` frontmatter field: `lk99`, `martianclock`, `infantconfig`

#### `_publications/2025-09-25-TamKwok-CNS2025.md`
- `featured: true` → `featured: false` (hidden from homepage Selected Publications; still listed on `/publications/`)

#### `_sass/layout/_publications.scss`
- Gutted `.pub-list-header`, `.pub-bib-*` classes (entries now use `hp-pub-*` from `_homepage.scss`)
- Added `.hp-pub[id] { scroll-margin-top }` for fixed-masthead anchor offset

---

## Phase 5 — Projects Page Redesign

### Design Decision
Switched from markdown (`projects.md` with `layout: archive`) to HTML (`projects.html` with `layout: homepage`) for Palatino serif consistency. Dropped shields.io badges and star history chart in favor of clean `docs / code / pypi` link rows matching publication card style. Archived projects rendered as compact list.

### Deleted Files
- `_pages/projects.md` — replaced by `projects.html`

### New Files
- `_pages/projects.html` — two featured project cards (mheatmap, pysgtsnepi) using `hp-pub-*` classes, archived section using `hp-list`

### Key Decision: Zero New SCSS
Project cards reuse `hp-pub` / `hp-pub-title` / `hp-pub-authors` / `hp-pub-links` from `_homepage.scss`. The `hp-pub-authors` class is repurposed for description text (same font size/weight works well). Archived list reuses `hp-list`.

---

## Phase 6 — More Hub Page

### Design Decision
Replaced placeholder `more.md` with `more.html` using `layout: homepage`. Surfaces teaching entries inline from `_teaching/*.md` frontmatter (course title, role + instructor, dates, location). Added Resources links section (CV PDF, Google Scholar, GitHub).

### Deleted Files
- `_pages/more.md` — placeholder replaced by full page

### New Files
- `_pages/more.html` — Teaching section (Liquid loop over `site.teaching`, sorted reverse by date) + Resources links

### Modified Files

#### `_sass/layout/_homepage.scss`
- Added `.hp-teaching-row` class (margin, font-size, line-height for compact teaching entries)

#### `_config.yml`
- `collections.teaching.output`: `true` → `false` (no individual teaching pages; content rendered inline from frontmatter)

---

## Phase 8 — Cleanup & Documentation

### Modified Files
- `TODO.md` — checked off Phases 5, 6, 8
- `CUSTOMIZATIONS.md` — documented all Phase 5, 6, 8 changes (this section)
- `CLAUDE.md` — updated architecture: Projects + More use `layout: homepage`; `teaching.output: false`; removed stale `markdown_generator/` reference; removed deleted layouts from hierarchy
