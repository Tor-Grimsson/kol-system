# Agent Context

## Current State

### Active Work
- Theme toggle fixed and working (light/dark)
- Styleguide loads directly, no landing page
- All UI text renders in JetBrains Mono
- Icons page added to styleguide
- Sidebar uses SVG icons with theme toggle at bottom
- Favicon set

### Recent Changes
- Fixed theme toggle: explicitly sets `data-theme="light"` / `data-theme="dark"`
- Replaced Unicode sidebar icons with SVG icons (color, type-01, component, pen)
- Added Icons styleguide page (226 icons, 16 categories)
- Set JetBrains Mono as base font on html/body
- Removed landing page, styleguide loads directly
- Added .gitignore
- Added favicon

## Project Overview

**Kolkrabbi Design System** - Typography-focused design system using JetBrains Mono

### Key Files
- `design-system/theme.css` - Master theme (imports color + typography)
- `design-system/color/simple/kol-color-simple.css` - Color tokens
- `design-system/typography/mono/kol-typography-mono.css` - Typography (v1.1)
- `design-system/components/components.css` - Component styles
- `src/pages/Styleguide.jsx` - Styleguide with 4 tabs
- `src/components/styleguide/Icons.jsx` - Icon library page
- `src/index.css` - Global styles (Tailwind + design system + base font)

### Font Files
Located in `/public/fonts/jetbrains-mono/`:
- JetBrainsMono-Regular.woff2 (400)
- JetBrainsMono-Medium.woff2 (500)
- JetBrainsMono-MediumItalic.woff2 (500 italic)
- JetBrainsMono-SemiBold.woff2 (600)

### Styleguide Tabs
1. Components (default) - 18+ components
2. Colors - Color token showcase
3. Typography - Typography classes
4. Icons - 226 SVG icons by category

## Conventions

### Typography Classes
- **Display** (`.kol-display-*`) - Hero/section headings, weight 600
- **Heading** (`.kol-heading-*`) - Content headings, weight 500
- **Text** (`.kol-text-*`) - Body copy, weight 400
- **Helper** (`.kol-helper-*`) - Labels/metadata, weight 500

### Naming
- Use consistent size scales: xl, lg, md, sm, xs, xxs, xxxs
- Avoid creating duplicate classes - use Tailwind utilities for variants

### Code Style
- Prefer editing existing files over creating new ones
- Remove unused code completely (no backwards-compatibility hacks)
- Use clamp() for responsive typography
- Document weight hierarchy in header comments

### Known Issues
- `WorkshopSidebar.jsx:370` references `--kol-font-family-rgrot-tight` (unused)
- `TypeSample.jsx` references Right Grotesk/Inter Tight font families (unused)
- Legacy typography CSS files (full/, lean/) still in repo
