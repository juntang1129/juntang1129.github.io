# Website Redesign Roadmap

Transforming the site into a clean, Min Liu / Jon Barron-inspired academic portfolio while keeping AcademicPages (Jekyll) as the base. Work through phases sequentially.

---

## Phase 0: Icon & Profile Image
- [x] Generate favicon via GPT (JT monogram, navy blue)
- [x] Generate favicon set (ico, 192px, 512px, apple-touch-icon)
- [x] Replace existing favicons + update HTML/manifest
- [x] Swap profile photo (800x800 WebP, 21KB — images/profile.webp)
- [x] Optimize profile photo (WebP q85, stripped EXIF, was 357KB PNG)

## Phase 1: Setup & Trim
- [x] Update README.md (minimal personal README)
- [x] Trim unused pages, includes, layouts, theme variants
- [x] Delete _portfolio/, _posts/
- [x] Update _config.yml (remove portfolio collection)
- [x] Update navigation.yml (Home | Publications | Projects | More)

## Phase 2: Layout Overhaul (No Sidebar)
- [x] Create _layouts/homepage.html (Min-style single-column)
- [x] Remove sidebar from archive.html and single.html
- [x] Add _sass/layout/_homepage.scss
- [x] Style top nav as tab buttons (Yueqian-inspired)
- [x] Update page/archive SCSS for full-width centered content

## Phase 3: Homepage Redesign (Min-Style)
- [x] Rewrite about.md → about.html (Min's layout, all sections, Min content as placeholder)
- [x] Publication cards inline (flex row: thumbnail | body); no separate include needed
- [x] Add publication frontmatter: featured, display_authors, award, thumbnail (all 5 papers)
- [x] SCSS: hp-pub flex row, placeholder boxes, work/edu/logo sections, responsive stack
- [x] Footer: remove GitHub/Feed links, fix copyright, "Inspired by / Template available at"
### Phase 3 — content still TODO (adapt piece by piece)
- [x] Write your own bio + profile links (Harvard/DKU/Duke inline-linked, "completing … May 2026", "am advised")
- [x] Write Work Experience entries (NTT Data + Bank of Huaxia, with real logos)
- [x] Education section: 3 rows (Harvard, Duke, DKU) with real logos, unified 56px SCSS
- [x] Services section — commented out (no public roles yet)
- [x] Miscellanea section — real Chinese name + hometown
- [x] Write news items with real dates/events
- [x] Paper thumbnails: decided against — text-only publication list is cleaner for non-visual research

## Phase 4: Publications Page Redesign
- [x] Drop individual entry pages (`output: false`), titles link to `paperurl`
- [x] Create `pub-bib-entry.html` include (bibliography-style inline citation)
- [x] Rewrite `publications.html` with flat reverse-chronological bib list
- [x] Add `_publications.scss` (bib citation, award, links styling)
- [x] Update homepage title links → `paperurl` (not dead `pub.url`)
- [x] Fix news section links → external URLs (not dead internal pages)
- [x] Strip body content + permalink from `_publications/*.md`
- [x] Switch `/publications/` to `layout: homepage` (Palatino serif, consistent styling)
- [x] Card-style entries on publications page (reuse `hp-pub-*` classes from homepage)
- [x] Anchor links: `anchor:` frontmatter + `id` attributes, homepage titles link to `/publications/#anchor`
- [x] `scroll-margin-top` for fixed masthead offset on anchor navigation
- [x] Hide MartianClock from homepage (`featured: false`), remove from News
- [x] Uncomment "only first and co-first authored papers are listed" note
- [x] Delete `pub-bib-entry.html` include (replaced by inline card loop)

## Phase 5: Projects Page Redesign
- [x] Rewrite projects.md → projects.html (featured hero cards)
- [x] Reuse hp-pub-* classes — zero new SCSS needed

## Phase 6: More Page
- [x] Create more.html hub page (Teaching inline from _teaching/*.md, Resources links)
- [x] Add .hp-teaching-row to _homepage.scss
- [x] Set teaching.output: false in _config.yml

## Phase 7: CV as PDF
- [x] Build LaTeX resume in separate repo (Jake's template)
- [x] Compile and copy PDF into files/resume.pdf in this repo
- [x] Link PDF from homepage (Min-style, not a nav tab) — slot already live in about.html
- NOTE: LaTeX source lives in its own repo — only the compiled PDF is committed here

## Phase 8: Cleanup & Documentation
- [x] Update CUSTOMIZATIONS.md with all changes
- [x] Update CLAUDE.md for new architecture
- [x] Final testing (build, dark/light, mobile, links)
