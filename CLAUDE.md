# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal blog for Shawn Yu, hosted on GitHub Pages at `https://shawnyu916.github.io/home`. Built with vanilla HTML, CSS, and JavaScript — no frameworks, no build tools, no database.

## Architecture

- **Single-page application (SPA)**: All content lives in `index.html` with hash-based routing. No page reloads between sections.
- **`css/style.css`**: Main stylesheet, dark cosmic theme with CSS variables
- **`statics/`**: Static assets (profile photo, WeChat QR code)
- **`music/`**: Audio files (background music)
- **`images/`**: Gallery photos (hardcoded in `index.html` gallery section)
- **`posts/`**: Blog post HTML files (legacy, content now embedded inline in `index.html`)

## Routes

- `#home` — Blog home
- `#gallery` — Photo gallery (lazy-loaded from `images/` folder)
- `#favorites` — Resource bookmarks
- `#post/{slug}` — Blog post content

## Key Patterns

- CSS variables for theming (`--bg-primary`, `--accent`, `--font-sans`, etc.)
- Sticky header with SPA navigation
- Responsive breakpoints at `700px`
- Social links in footer (GitHub, LinkedIn, WeChat modal)
- Background music player with toggle button
- Hash-based client-side routing: `#home`, `#favorites`, `#post/{slug}`

## SPA Routing

Navigation uses hashchange events. Each section is a `<main>` element with class `spa-section`. The router shows/hides sections based on `window.location.hash`.

## GitHub Pages Deployment

- Remote: `https://github.com/shawnyu916/home.git`
- Branch: `main` (GitHub Pages serves from `main` by default)
- Content is served directly from the repository root
