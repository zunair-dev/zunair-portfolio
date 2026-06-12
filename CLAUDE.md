# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a single-page static HTML portfolio site for Muhammad Zunair, deployed on GitHub Pages at `www.zunair.dev` (configured via `CNAME`). There is no build system, package manager, or framework — all source files are edited directly.

## Structure

- `index.html` — the entire site; all sections (Hero, About, Facts, Resume, Portfolio, Skills, Contact) live in this one file
- `Muhammad Zunair_files/` — all assets:
  - `style.css` — custom styles (based on BootstrapMade iPortfolio v1.5.0 template)
  - `main.js` — custom JS (jQuery-based: typed animation, smooth scroll, AOS init, Isotope portfolio filter, Owl Carousel)
  - Vendor libs bundled locally: Bootstrap, jQuery, AOS, Typed.js, Isotope, VenoBox, Owl Carousel, IcoFont, CounterUp
  - Images: `dp.png` (profile photo), `front 1.png` (about section), project screenshots (e.g. `lzrpro.png`, `swapbook.png`)

## Development

No build step required. Open `index.html` directly in a browser, or serve it locally:

```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

## Deployment

Pushing to the `master` branch on GitHub automatically deploys via GitHub Pages. The custom domain `www.zunair.dev` is set in `CNAME`.

## Key conventions

- All content edits (bio, experience, skills, project entries) are made directly in `index.html`.
- Custom styles go in `Muhammad Zunair_files/style.css`; vendor CSS files should not be modified.
- The portfolio filter uses Isotope — new portfolio items need a `data-filter` category matching an existing `#portfolio-flters` button, or a new filter button must be added.
- Scroll-activated animations use AOS (`data-aos` attributes) and waypoints (`jquery.waypoints.min.js`).
- The typed hero text is driven by `data-typed-items` on the `.typed` span in `index.html`.
