# CLAUDE.md

This file provides guidance for AI assistants working with this codebase.

## Project Overview

Personal portfolio website for **Heber Bermudez**, a Senior Data Engineer, Statistician, and AI Specialist. This is a static website hosted on **GitHub Pages** at [hebermudezg.github.io/hebermudezg](https://hebermudezg.github.io/hebermudezg).

## Technology Stack

- **HTML5** - Static pages with semantic markup
- **Tailwind CSS** - Utility-first CSS framework (loaded via CDN)
- **Custom CSS** - Additional stylesheets in `/css/`
- **JavaScript** - Vanilla JS for interactivity
- **Font Awesome** - Icon library (CDN)
- **AOS** - Animate On Scroll library (CDN)
- **Google Fonts** - Inter and JetBrains Mono typefaces

## Directory Structure

```
hebermudezg/
├── index.html          # Main portfolio page (primary entry point)
├── sql.html            # SQL course resources page
├── pyhon.html          # Python course curriculum page
├── css/                # Stylesheet files
│   ├── style.css       # Original base styles
│   ├── style-courses.css # Course page styling
│   └── style-[1-4].css # Menu/navigation style variants
├── js/
│   └── javascript.js   # Custom JavaScript functions
├── img/                # Image assets (photos, logos)
├── documents/          # PDF documents (resume, etc.)
├── fonts/              # Custom font files
├── templates/          # HTML templates and experiments
│   ├── menus.html      # Navigation style demos
│   └── index copy.html # Template backup
├── courses/
│   └── python/         # Python course materials
├── README.md           # GitHub profile readme
└── CLAUDE.md           # This file
```

## Key Files

| File | Purpose |
|------|---------|
| `index.html` | Main portfolio with hero section, teaching, research, projects, and contact |
| `sql.html` | Links to SQL tutorials on Medium |
| `pyhon.html` | 8-week Python course curriculum outline |

## Design System

### Color Palette (CSS Variables in index.html)

- `--primary`: #2563eb (Blue)
- `--primary-light`: #3b82f6
- `--primary-dark`: #1d4ed8
- `--text-primary`: #111827
- `--text-secondary`: #4b5563
- `--bg-white`: #ffffff
- `--bg-subtle`: #f9fafb

### UI Components

- `.btn-primary` / `.btn-secondary` - Button styles
- `.card` - Card containers with hover effects
- `.skill-pill` - Tag/pill elements for skills
- `.section-card` - Section wrapper with subtle background
- `.nav-link` - Navigation links with underline animation
- `.social-icon` - Social media icon buttons

## Development Workflow

### Deployment

This is a GitHub Pages site. Changes pushed to the main branch are automatically deployed.

### Branch Naming Convention

Feature branches follow the pattern: `claude/[feature-description]-[session-id]`

### Common Tasks

**Local Preview:**
```bash
# Using Python's built-in server
python -m http.server 8000

# Or using Node's http-server
npx http-server
```

**No Build Process Required** - This is a static site with no compilation needed.

## Code Conventions

### HTML
- Use semantic HTML5 elements (`<section>`, `<nav>`, `<footer>`)
- Include `data-aos` attributes for scroll animations
- Use Tailwind utility classes combined with custom CSS
- Maintain responsive design with `sm:`, `md:`, `lg:` breakpoints

### CSS
- Custom styles use CSS variables for theming
- Follow BEM-like naming for custom classes
- Transitions should use `ease` timing with 0.2-0.3s duration

### JavaScript
- Vanilla JS only (no frameworks)
- Use `addEventListener` for event binding
- Initialize AOS library on page load

## Content Sections (index.html)

1. **Navigation** - Fixed header with responsive mobile menu
2. **Hero** - Name, title, and call-to-action buttons
3. **Teaching** - Course cards for Statistics and Data Engineering
4. **Research & Publications** - Academic papers and Medium articles
5. **Projects** - Links to Shiny apps and dashboards
6. **Contact** - Email and social media links
7. **Footer** - Copyright notice

## External Links

The site links to various external resources:
- LinkedIn: linkedin.com/in/hebermudezg
- GitHub: github.com/hebermudezg
- Medium: medium.com/@hebermudezg
- Shiny Apps: hebermudezg.shinyapps.io/*
- Power BI Dashboards

## Assets

- Profile images in `/img/` (hebermudezg.jpeg, hebermudezg2.jpeg)
- Technology logos (Python, R, AWS, SQL, Bash)
- Resume PDF in `/documents/`

## Notes for AI Assistants

1. **Prefer editing index.html** - This is the main page that gets the most updates
2. **Test responsiveness** - Always consider mobile layouts when making changes
3. **Maintain consistency** - Follow existing color scheme and spacing patterns
4. **CDN dependencies** - Tailwind, AOS, and Font Awesome are loaded via CDN
5. **No framework** - This is vanilla HTML/CSS/JS, keep it simple
6. **GitHub Pages** - No server-side code, everything must be static
