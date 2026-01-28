# Repository Guidelines

## Project Structure & Module Organization
- `src/pages/`: Route-level Astro pages (`index.astro`, `about.astro`, `posts.astro`, `post/[slug].astro`).
- `src/layouts/`: Shared page layouts (`main.astro`, `post.astro`).
- `src/components/`: Reusable UI components.
- `src/content/post/`: Markdown blog posts with frontmatter (`title`, `description`, `dateFormatted`).
- `src/content/config.js`: Content collection schema.
- `src/assets/`: Local CSS/JS assets; `public/` for static files served as-is.

## Build, Test, and Development Commands
- `pnpm dev`: Start the Astro dev server locally.
- `pnpm build`: Run `astro check` and build the production bundle.
- `pnpm preview`: Preview the production build locally.
- `pnpm check`: Run Biome linting with auto-fix.

## Coding Style & Naming Conventions
- Indentation: 2 spaces; align with existing Astro component formatting.
- Use double quotes in JS/TS files (matches `src/content/config.js`).
- Tailwind CSS is the primary styling approach; use utility classes and `@tailwindcss/typography` for prose.
- Content files: kebab-case filenames in `src/content/post/` and valid frontmatter fields.

## Testing Guidelines
- No dedicated test framework currently configured.
- Use `pnpm build` to type-check and validate the site.
- When adding new content or components, verify pages locally with `pnpm dev`.

## Commit & Pull Request Guidelines
- Commit messages largely follow Conventional Commits (`feat:`, `fix:`, `docs:`, `refactor:`). Use that format when possible.
- PRs should include a short summary, testing notes (e.g., `pnpm build`), and screenshots for UI changes.
- Link relevant issues or content references when applicable.

## Content & Configuration Notes
- Blog posts rely on `dateFormatted` in frontmatter; keep the format consistent (e.g., `Jun 6, 2024`).
- Layout supports `HEADER_INJECT` and `FOOTER_INJECT` environment variables for HTML injection.
