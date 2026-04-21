# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal blog for Shawn Yu, hosted on GitHub Pages at `https://shawnyu916.github.io/home`. Built with vanilla HTML and CSS — no frameworks, no build tools, no database.

## Architecture

- **Root**: `index.html` (home page — not yet created)
- **`css/style.css`**: Main stylesheet, dark theme with CSS variables
- **`posts/`**: Individual blog posts as HTML files

## Key Patterns

- CSS variables for theming (`--bg-primary`, `--accent`, `--font-sans`, etc.)
- Sticky header, single-column layout with `max-width: 800px`
- Responsive breakpoints at `600px`
- Links use `../` relative paths (posts are one level deep)
- Social links in footer (Twitter, GitHub, LinkedIn, RSS)

## GitHub Pages Deployment

- Remote: `https://github.com/shawnyu916/home.git`
- Branch: `main` (GitHub Pages serves from `main` by default)
- Content is served directly from the repository root
