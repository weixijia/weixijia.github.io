# xijiawei.com

Personal academic website of Xijia Wei, built with plain Jekyll (no theme) and
served by GitHub Pages. Design rationale and rules live in [DESIGN.md](DESIGN.md).

## Structure

- `index.html` — about, news, and academic service (the homepage)
- `_pages/*.html` — publications, talks, teaching, and experience pages
- `_layouts/default.html` — HTML skeleton and nav; `_layouts/redirect.html` — legacy URL stubs
- `assets/css/main.css` — all styling (plain CSS, no build step)
- `_publications/`, `_talks/`, `_teaching/`, `_experience/` — content as front matter
- `_data/news.yml` — news items
- `files/` — paper PDFs; `images/` — portrait and favicons

## Editing content

- **New publication**: add a file to `_publications/` with `title`, `date`,
  `authors` (natural order, full names), `venue_short`, and optional `pdf` /
  `link` front matter.
- **News**: add an entry to the top of `_data/news.yml`; mark items `old: true`
  to collapse them under "older news".
- **Talks / teaching / experience**: add a file to the matching collection.

## Local preview

```sh
bundle install
bundle exec jekyll serve
```
