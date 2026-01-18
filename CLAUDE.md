# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

OneStop Wealth Hub - A financial services website for insurance, mutual funds, bonds, loans, and investment products.

## Development

This is a static HTML/CSS/JavaScript website with no build system or dependencies.

**To run locally:**
```bash
python -m http.server
# or
npx http-server
```

Then open http://localhost:8000 in a browser.

**No build, test, or lint commands** - edit files directly and refresh the browser.

## Architecture

Single-page static site with three files:
- `index.html` - Page structure with sections: navigation, hero, services grid, features, about, contact form, footer
- `styles.css` - Responsive CSS using Grid/Flexbox with CSS custom properties for theming
- `script.js` - Vanilla ES6 JavaScript (~200 lines) for mobile menu, smooth scroll, form validation, scroll animations

## CSS Theme Variables

Colors are defined as CSS custom properties in `:root`:
- `--primary-color: #1a365d` (dark blue)
- `--secondary-color: #2c5282` (medium blue)
- `--accent-color: #3182ce` (bright blue)
- `--gold-color: #d69e2e` (CTA accent)

## Responsive Breakpoints

- 992px - Desktop grid adjustments
- 768px - Tablet (hamburger menu, single column)
- 480px - Mobile (reduced padding/fonts)

## JavaScript Features

- Mobile hamburger menu toggle
- Smooth scroll with header offset for anchor links
- Intersection Observer for scroll-triggered animations
- Contact form validation (email regex: `/^[^\s@]+@[^\s@]+\.[^\s@]+$/`)
- Toast notification system with auto-dismiss

## Notes

- Contact form has client-side validation only (no backend configured)
- No external libraries or frameworks - pure vanilla implementation
