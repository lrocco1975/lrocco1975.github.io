# Memory — Personal Website (lrocco1975.github.io)

## Project overview
Academic personal website for Lorenzo Rocco, Professor of Economics, University of Padova.
- **Live site**: https://lrocco1975.github.io
- **Source files**: `/Users/lorenzorocco/Library/CloudStorage/OneDrive-UniversitàdegliStudidiPadova/Documenti/_personal website/`
- **GitHub repo**: https://github.com/lrocco1975/lrocco1975.github.io (public)
- **Stack**: Pure HTML + CSS, no build tools. One shared `css/style.css`.
- **Deploy**: `git push` to `main` → live within ~1 min via GitHub Pages.

## File structure
```
index.html                        # Home page (bio, recent publications)
consulting.html                   # Consulting / research with organisations
research/
  articles.html                   # Journal articles, book chapters, research reports
  working-papers.html             # Recent working papers (6 entries)
  data.html                       # Data page
teaching/
  index.html                      # Teaching history (two sections)
  development-economics.html      # Dev Econ sub-page
  scuola-galileiana.html          # Scuola Galileiana sub-page
hobbies/
  books.html                      # Books list
css/style.css                     # All styles
```

## Standing editorial rules
1. **Publications ordered by year descending** within each section (journal articles, chapters, reports, working papers).
2. **All article/working-paper titles are clickable** — link to DOI (`https://doi.org/...`) or publisher page; use `target="_blank" rel="noopener"`. Wrap only the quoted title in `<a>`.
3. **Research report titles** use `<em>` for the title; wrap `<em>` inside `<a>` when a link is available.
4. **No workshop or social-capital-book links** anywhere (removed from footer).

## CSS notes
- `.pub-text em` sets `color: #4b5563` (grey) for italic journal names.
- `.pub-text a em { color: inherit; }` overrides this so linked report titles show in link-blue — **do not remove this rule**.
- External links: `target="_blank" rel="noopener"` on all.

## Content status (as of 2026-03-13)

### research/articles.html
- **Journal Articles**: 44 entries, 2007–2026, all with DOI/publisher links.
  - Topmost: "Bipartisan Firms" (2026), *Economics & Politics* 38(1):18–45, DOI 10.1111/ecpo.70010
- **Chapters in Books**: 7 entries, 2005–2018, no links.
- **Research Reports**: 6 entries, 2006–2024, 5 with links (2006 Chronic Disease has no surviving free URL).
  - Topmost: UNESCO 2024 "The price of inaction..." → https://www.unesco.org/en/articles/price-inaction-global-private-fiscal-and-social-costs-children-and-youth-not-learning

### research/working-papers.html
- 6 recent working papers (2023–2025), all with IZA/GLO links.
- "Older Working Papers & Mimeos" section removed.

### index.html (home)
- Recent publications teaser: 5 entries (2025–2026).
- Footer: email only (no workshop/book links).

### consulting.html
- 20 entries, 2005–2026, ordered year descending.
- Topmost: 2026 INVALSI — "Impact Evaluation of the PN Scuola 2021-2027"

### teaching/index.html
- Two sections: University of Padova (8 courses) and Other Institutions (7 entries).
- Uses `.pub-list` / `.pub-year` / `.pub-text` CSS classes.

## Git workflow
```bash
cd '/Users/lorenzorocco/Library/CloudStorage/OneDrive-UniversitàdegliStudidiPadova/Documenti/_personal website'
git add <files>
git commit -m "message"
git push
```
If push is rejected (remote ahead): `git pull --rebase && git push`

## Local preview server
Configured in `.claude/launch.json` — run via `mcp__Claude_Preview__preview_start`.
Serves on port 3000 from the `_personal website` directory.
