# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a [Hugo](https://gohugo.io/) static site project. The Go module is `github.com/C-P22/ETH`. The site is configured in `hugo.toml` with base URL `https://example.org/`.

## Common Commands

```bash
# Start local development server (with draft content)
hugo server -D

# Build the site (outputs to public/)
hugo

# Create new content
hugo new content/<section>/<filename>.md

# Build with minification
hugo --minify
```

## Project Structure

- `hugo.toml` — site configuration (baseURL, title, language, theme, etc.)
- `content/` — Markdown content files organized by section
- `layouts/` — HTML templates that override theme layouts
- `archetypes/` — templates for new content (`hugo new` uses these)
- `themes/` — Hugo themes (currently empty; add themes here)
- `assets/` — files processed by Hugo Pipes (SCSS, JS, images)
- `static/` — files copied as-is to `public/` on build
- `data/` — structured data files (YAML/TOML/JSON) accessible in templates
- `i18n/` — internationalization/translation strings
- `public/` — build output (git-ignored)

## Hugo Conventions

- Content front matter uses TOML (`+++` delimiters) by default per `archetypes/default.md`
- New content is created as drafts (`draft = true`); use `hugo server -D` to preview drafts
- Theme customization is done by mirroring the theme's file structure in `layouts/` or `assets/` — files here take precedence over theme files
