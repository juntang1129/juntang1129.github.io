# juntang1129.github.io

Personal academic portfolio for Juntang Wang. Live at [www.qqgjyx.com](https://www.qqgjyx.com).

Built with [Jekyll](https://jekyllrb.com/) + [AcademicPages](https://github.com/academicpages/academicpages.github.io).

## Development

```bash
bundle install
bundle exec jekyll serve -l -H localhost  # http://localhost:4000
```

## Content

- `_publications/` — Publication markdown files
- `_teaching/` — Teaching entries
- `_talks/` — Talk entries
- `_pages/` — Static pages (about, CV, projects)
- `_data/navigation.yml` — Header nav links

## Notes

- `_config.yml` changes require server restart
- MathJax/Plotly/Mermaid are opt-in per page: add `mathjax: true` etc. to frontmatter
- Profile image: `images/profile.webp` (regenerate if OneDrive converts it to jpg)
