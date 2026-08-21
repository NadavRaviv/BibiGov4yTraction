# AGENTS.md

## Cursor Cloud specific instructions

This repository is a **single-file static HTML dashboard** — `israel-dashboard-artifact2.html`
("ישראל במבט אחד" / "Israel at a Glance"), a Hebrew RTL data dashboard with inline CSS/JS
and hard-coded data. There is **no build system, package manager, backend, database, tests,
or lint config**, so there is nothing to install and no update script work to do.

### Running it
- Serve statically from the repo root and open in a browser, e.g.
  `python3 -m http.server 8000` then visit
  `http://localhost:8000/israel-dashboard-artifact2.html`.
- It also opens directly via `file://` — a server is only a convenience for `http://`.

### Notes
- All metric data is hard-coded in a JS array (`const M = [...]`) inside the HTML; there is
  no API or data fetching.
- The only external dependency is the Google Fonts CDN (Heebo font), which is purely cosmetic;
  the page renders fine offline with fallback system fonts.
- Interactive features: category filter chips, free-text search, a time-range selector
  (1/2/4 years), and in-browser SVG sparkline charts.
