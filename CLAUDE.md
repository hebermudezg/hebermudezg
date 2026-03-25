# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio and educational website for **Heber E. Bermúdez** — Data Engineer, Data Architect & AI Engineer. Static HTML/CSS/JS site with no build system or backend.

**Live site:** Deployed via GitHub Pages from the `master` branch.

## Development

**No build process.** Edit HTML/CSS/JS files directly and commit. All dependencies load via CDN — no package manager needed. No test suite or linter configured.

To preview locally, open `index.html` in a browser.

## Architecture

### Page types

1. **`index.html` (portfolio)** — The primary page. All styles are inlined in a `<style>` block within the file. Uses Tailwind CSS (CDN), AOS animations, Font Awesome icons, and Google Fonts (Inter, JetBrains Mono). Sections: nav, hero (`#home`), teaching (`#teaching`), research (`#research`), projects (`#projects`), contact (`#contact`), footer.

2. **Course pages (`pyhon.html`, `sql.html`, `courses/python/pyhon.html`)** — Lightweight HTML pages linking to external resources (GitHub notebooks, Medium articles). These use external CSS from `css/` (e.g., `style-courses.css`), not inlined styles.

3. **Templates (`templates/`)** — Experimental/backup files, not part of the live site.

### CSS split

- `index.html`: all styles are **inlined** — do not create external CSS files for it
- Course pages: use external stylesheets from `css/`
- `css/style-1.css` through `style-4.css` and `style1.css` through `style4.css`: menu effect variants and legacy iterations used by templates

### Design system (index.html)

CSS custom properties define the theme:
- Primary color: `--primary: #2563eb` (blue)
- Fonts: Inter (body), JetBrains Mono (code)
- Responsive breakpoint: 768px for mobile

Key classes: `.card`, `.btn-primary`, `.btn-secondary`, `.skill-pill`, `.project-card`, `.nav-link`, `.social-icon`, `.section-card`

### JavaScript

Minimal — `js/javascript.js` exists but the main page uses inline `<script>` at the bottom of `index.html` for: mobile menu toggle, AOS initialization, and smooth scroll behavior.

## Conventions

### File naming
- HTML: lowercase (`index.html`, `sql.html`)
- CSS: kebab-case (`style-courses.css`)
- Images: underscores (`python_logo1.png`)

### Content language
- Site content is in **English**
- Some image filenames are in Spanish

### Commit messages
- Imperative mood, action-first: `Add`, `Remove`, `Simplify`, `Enhance`, `Redesign`
- Mention scope explicitly: `Add project links to README`
- No ticket numbers or conventional commit prefixes
- Keep messages concise (one line)

## Important Notes

- The filename `pyhon.html` (missing "t") is **intentional** — do not rename without explicit request
- New pages should follow the existing pattern: standalone HTML with CDN dependencies
- `README.md` serves as the GitHub profile README, not project documentation
