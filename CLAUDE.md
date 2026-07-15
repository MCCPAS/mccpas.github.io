# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the Physics Alumni Society website for Madras Christian College (MCC), Chennai (mccpas.github.io). A static site built with Jekyll and hosted on GitHub Pages. The site maintains records of alumni achievements, endowment lecture series, and Physics Alumni Meet events.

## Development Commands

```bash
# Install dependencies (first time setup)
script/bootstrap

# Local development server (http://localhost:4000)
bundle exec jekyll serve

# Build site
bundle exec jekyll build

# Run full CI validation (HTML validation, linting, build)
script/cibuild
```

## Architecture

**Technology Stack:** Jekyll static site generator with the jekyll-theme-minimal theme, deployed via GitHub Pages.

**Content Structure:**
- Content pages are Markdown files in the root directory (index.md, about.md, committee.md, contributions.md, events.md, gallery.md, contact.md)
- `_layouts/` contains page templates (default.html for main layout, post.html for articles)
- `_includes/` contains partial HTML components
- `_sass/` contains SCSS stylesheet modules
- `assets/` contains images, CSS, JS, and fonts

**Configuration:** `_config.yml` controls site title, logo, theme settings, and Google Analytics.

**Note:** The `/org/` subdirectory contains a duplicate site structure (likely archival) - primary development should focus on root-level files.

## Adding Content

- Add new pages as Markdown files in the root directory
- Images go in `assets/img/`
- Custom styles can be added after the `@import` line in `assets/css/style.scss`
- Navigation links are defined in `_layouts/default.html`
