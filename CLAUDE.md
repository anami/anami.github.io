# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
pnpm dev          # Start development server
pnpm build        # Type-check and build for production
pnpm preview      # Preview production build
pnpm check        # Run Biome linter with auto-fix
```

## Architecture

This is an Astro-based personal blog/portfolio site using the Aria template.

### Key Directories

- `src/pages/` - Page routes (index, about, posts, projects, post/[slug])
- `src/layouts/` - Page layouts (main.astro wraps all pages, post.astro extends main for blog posts)
- `src/components/` - Reusable Astro components
- `src/content/post/` - Markdown blog posts with frontmatter (title, description, dateFormatted)
- `src/assets/` - CSS and JS files

### Content System

Blog posts are defined in `src/content/config.js` using Astro's content collections. Each post requires:
- `title: string`
- `description: string`
- `dateFormatted: string` (human-readable date like "Jun 6, 2024")

Posts use `layout: ../../layouts/post.astro` in frontmatter.

### Styling

- Tailwind CSS with class-based dark mode (`dark:` prefix)
- `@tailwindcss/typography` plugin for prose styling in blog posts
- Dark mode state persisted in localStorage (`dark_mode`)

### Environment Variables

The main layout supports HTML injection via:
- `HEADER_INJECT` - Injected into `<head>`
- `FOOTER_INJECT` - Injected before `</body>`
