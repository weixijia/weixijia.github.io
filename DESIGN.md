# Site design notes

Redesigned 2026. This file records where the design comes from and the rules it
follows, so future edits stay consistent.

## References

The design is deliberately borrowed from established, human-made conventions
rather than invented from scratch:

- **Structure** — [jonbarron.info](https://jonbarron.info/): the de-facto
  standard single-page research index used across the ML community. One page,
  bio at top, then a dense scannable list of publications with author lists
  (own name emphasized), venues, and small inline links. Content first, zero
  decoration.
- **Typography & restraint** — [pascalmichaillat.org](https://pascalmichaillat.org/)
  and his minimalist Hugo academic template: strong typographic hierarchy,
  generous whitespace, one accent color, no imagery beyond a single portrait.
- **Type trend** — serif body text is the dominant 2025–26 direction for
  personal/editorial sites (Newsreader, Source Serif, EB Garamond revival).
  We use [Newsreader](https://fonts.google.com/specimen/Newsreader) (variable,
  optical sizing) for all text, with the system monospace stack for dates,
  labels, and metadata.
- **Anti-slop constraints** — informed by 2025–26 writeups on spotting
  AI-generated sites (925studios "AI Slop Web Design", sikora.software):
  no purple/indigo gradients, no glassmorphism or card shadows, no emoji as
  icons, no Inter-by-default, no scroll animations, no hero section.

## Design system

Layout
- Multi-page with a small monospace top nav (about / publications / talks /
  teaching / experience), keeping the old site's URL structure.
- Single centered column, `max-width: 44rem`.
- Sections separated by hairline rules, not boxes or cards.
- Interactive elements: native `<details>` disclosures (news, citations) and
  a light/dark toggle in the nav. The toggle is the site's only JavaScript
  (~20 lines inline in the layout): it sets `data-theme` on the root element
  and remembers the choice in `localStorage`; with no stored choice the site
  follows `prefers-color-scheme`.

Type
- Body: Newsreader (400/500/600 + italic), fallback Georgia/serif, 17px, 1.6.
- Metadata (dates, section labels, link buttons): system monospace,
  ~0.75rem, uppercase section labels with letter-spacing.
- Hierarchy by weight and size contrast between serif text and mono labels,
  not by color blocks.

Color
- Warm paper background, near-black ink, one accent (burnt sienna) for links.
- Dark scheme via `prefers-color-scheme` with the same relationships.
- All colors defined as CSS custom properties in `assets/css/main.css`.

Content rules
- Publications: authors in natural reading order, own name set in medium
  weight; venue + year in italic; links as small mono `[PDF]` / `[DOI]`.
- Grouped by year, newest first.
- News: mono date column + serif text, latest handful visible, the rest
  collapsed.
- No self-promotional adjectives; entries state facts (title, venue, date).

## Architecture

Plain Jekyll on GitHub Pages (no theme, no SCSS, no vendor JS):
- `_layouts/default.html` — the only real layout (includes the top nav).
- `index.html` — about + news + service; section pages live in `_pages/`
  (`publications.html`, `talks.html`, `teaching.html`, `experience.html`)
  and loop over collections.
- Collections (`_publications`, `_talks`, `_teaching`, `_experience`) keep
  content as markdown front matter. Items render only as redirects: each
  keeps its legacy `permalink` and carries `redirect_to` pointing at its
  anchor on the list page, so no pre-redesign URL breaks.
- `_data/news.yml` — news items.
- `_layouts/redirect.html` + `_pages/cv.md` / `_pages/resume.md` send the
  legacy `/cv/` and `/resume/` URLs to the homepage; `/about/` too.
