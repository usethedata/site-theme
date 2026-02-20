# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the shared Jekyll remote theme for the usethedata web presence. The GitHub repository is `usethedata/site-theme`. It provides consistent styling, header, and footer across:
- `usethedata/profile-site` → [usethedata.me](https://usethedata.me)
- `usethedata/personal-website` → [usethedata.net](https://usethedata.net)

Both sites pull this theme via `jekyll-remote-theme` in their `_config.yml`.

## Branching and Deployment

**IMPORTANT:** Always work on the `dev` branch. If the repo is checked out to `main`, ask the user before making any file changes — working on `main` directly is an exception, not the norm.

When theme changes are pushed to `main`, both sites pick them up on their next GitHub Pages build. To force a rebuild, push a commit to each site or trigger their workflows manually.

## Project Structure

- `_layouts/default.html` - Base HTML template (used by both sites)
- `_includes/header.html` - Configurable nav header (reads `site.header_links`)
- `_includes/footer.html` - Configurable footer (reads `site.footer_links` and `site.author`)
- `assets/css/style.css` - Shared styles

## Design System

- **Typography:** Roboto font family (Google Fonts)
- **Color scheme:** Navy blue (#1a365d primary, #2c5282 accent), light gray (#f7fafc) background
- **Layout:** Responsive, mobile-friendly without a framework

## Configuration

Sites configure their navigation by setting `header_links` and `footer_links` in their own `_config.yml`. The theme reads these to render nav elements.
