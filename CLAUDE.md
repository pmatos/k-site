# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A personal portfolio website for Kimberly Matos, a dancer and choreographer. Built with Astro, deployed to https://k.ocmatos.com.

## Commands

- `npm run dev` - Start development server at localhost:4321
- `npm run build` - Build production site to ./dist/
- `npm run preview` - Preview production build locally

## Architecture

### Tech Stack
- **Framework**: Astro 5.x (static site generator)
- **Styling**: Global CSS with custom properties (no CSS framework)
- **TypeScript**: Strict mode enabled

### Project Structure
```
src/
├── components/Layout.astro    # Main layout with header, nav, footer
├── data/
│   ├── profile.json           # Site owner info, bio, styles, achievements
│   └── competitions.json      # Past and upcoming competition data
├── pages/
│   ├── index.astro            # Homepage with hero section
│   ├── about.astro            # About page
│   └── competitions/
│       ├── past.astro         # Past competitions listing
│       └── upcoming.astro     # Upcoming competitions listing
└── styles/global.css          # All styling (CSS custom properties)

public/
├── images/                    # Hero and about photos
├── favicon.svg
└── CNAME                      # Custom domain config
```

### Data-Driven Content
- Profile data (name, bio, photo paths, dance styles, achievements) lives in `src/data/profile.json`
- Competition entries are stored in `src/data/competitions.json` with `past` and `upcoming` arrays
- Pages read from these JSON files - edit the JSON to update content

### CSS Architecture
- Single global stylesheet at `src/styles/global.css`
- Uses CSS custom properties for theming (colors, fonts, spacing)
- Color palette: cream/pink pastel theme
- Fonts: Cormorant Garamond (display) + DM Sans (body) via Google Fonts
