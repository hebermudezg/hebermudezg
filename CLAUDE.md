# CLAUDE.md

## Project Overview

Personal portfolio and educational website for **Heber E. Bermúdez** — a Data Engineer, Data Architect, and AI Engineer. This is a static HTML/CSS/JS site with no build system or backend.

**Live site:** Deployed via GitHub Pages from the `master` branch.

## Repository Structure

```
/
├── index.html              # Main portfolio page (primary file)
├── pyhon.html              # Python course overview (note: intentional filename)
├── sql.html                # SQL course overview
├── README.md               # GitHub profile README
├── courses/
│   └── python/
│       └── pyhon.html      # Detailed Python course content
├── css/
│   ├── style.css           # Main site styles
│   ├── style-courses.css   # Course page styles
│   ├── style-1.css … style-4.css   # Menu effect variants
│   └── style1.css … style4.css     # Legacy/alternate style iterations
├── js/
│   └── javascript.js       # Minimal JS (mobile menu, AOS init)
├── templates/
│   ├── menus.html           # Menu navigation examples
│   └── index copy.html      # Previous version backup
├── img/                     # Images: profile photos, logos, project assets
├── fonts/                   # Font directory (currently empty)
└── documents/
    └── Heber Bermudez.pdf   # Resume/CV
```

## Tech Stack

- **HTML5** — Semantic markup, no templating engine
- **CSS3** — Custom properties for theming, media queries for responsiveness
- **Tailwind CSS** — Loaded via CDN in `index.html`
- **Vanilla JavaScript** — No frameworks
- **Font Awesome 6.5.1** — Icons (CDN)
- **Google Fonts** — Inter, JetBrains Mono (CDN)
- **AOS** — Animate On Scroll library (CDN)

## Development Workflow

**No build process.** Edit HTML/CSS/JS files directly and commit.

- All dependencies are loaded via CDN — no `npm install` or package manager needed
- No `.gitignore` exists; `.DS_Store` and `.Rhistory` are tracked
- No test suite or linter configured
- To preview locally, open `index.html` in a browser

## Key Conventions

### Design System (index.html)

CSS custom properties define the theme:
- Primary color: `--primary: #2563eb` (blue)
- Fonts: Inter (body), JetBrains Mono (code)
- Responsive breakpoint: 768px for mobile

Reusable CSS classes: `.card`, `.btn-primary`, `.btn-secondary`, `.skill-pill`, `.project-card`, `.nav-link`

### File Naming

- HTML pages use lowercase: `index.html`, `sql.html`
- CSS uses kebab-case: `style-courses.css`
- Images use underscores: `python_logo1.png`, `bash_linux_logo1.png`

### Content Language

- Site content is in **English**
- Some image filenames are in Spanish (e.g., `madre-solterea.webp`)

## Commit Message Style

- **Imperative mood**, action-first: `Add`, `Remove`, `Simplify`, `Enhance`, `Redesign`
- Mention scope explicitly: `Add project links to README`, `Reorganize hero section and projects layout`
- No ticket numbers or conventional commit prefixes
- Keep messages concise (one line)

## Important Notes

- The filename `pyhon.html` (missing "t") is intentional/established — do not rename without explicit request
- All styles for `index.html` are inlined in a `<style>` block within the file itself, not in external CSS files
- The external CSS files in `css/` are used by course pages and template experiments
- When adding new pages, follow the existing pattern: standalone HTML with CDN dependencies
