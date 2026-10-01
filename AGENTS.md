# AGENTS.md

Guidance for AI coding agents working in this repository.

## Project

Static website for Monoid Studio, served by GitHub Pages from the `main` branch root at <https://monoid.studio>. See `README.md` for the file layout.

## Constraints

- Plain HTML and CSS only. Do not add a build step, package manager, framework, or JavaScript unless explicitly asked.
- Keep `CNAME` as `monoid.studio`. Removing or changing it breaks the custom domain.
- Use absolute paths (`/logo.svg`) for shared assets so they resolve from every page.
- All site content, code, comments, and commit messages are in English.

## Styling

- All styles live in `style.css`. Do not use inline styles or per-page stylesheets.
- Colors are CSS custom properties on `:root`, overridden under `@media (prefers-color-scheme: dark)`. Add new colors as tokens in both blocks; never hard-code colors in rules.
- Fonts: Inter for text, JetBrains Mono for labels. Both are loaded from Google Fonts in each page's `<head>`.
- Layouts must work at phone width (see the `max-width: 640px` media query) without horizontal scrolling.

## Pages

- Every page shares the same `<head>` (fonts, favicon, `apple-touch-icon`, `og:image`, `style.css`), header, and footer. When adding a page, copy them from `index.html` and use `/#section` links in the nav.
- When editing `privacy.html`, update its "Last updated" date.

## Brand assets

- `logo.svg` is the source of truth for the logo mark; `logo-square.svg` is the variant with a background, for avatars.
- If an SVG changes, regenerate the matching PNG (`logo.png`, `logo-square.png` at 1024×1024, `apple-touch-icon.png` at 180×180).

## Verification

There are no tests. Preview locally with `python3 -m http.server 8000` and check both light and dark mode at desktop and phone widths.

## Git

- Use Conventional Commits (`feat:`, `fix:`, `style:`, `docs:`, `chore:`).
- Pushing to `main` deploys the site immediately.
- Merge pull requests with a merge commit, not a squash.
