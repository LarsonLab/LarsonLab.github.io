# AI Coding Agent Guide for LarsonLab.github.io

This repo is a Jekyll-based website (Mediumish theme) for the UCSF Larson Advanced Imaging Group. Agents should focus on content changes, theme/layout tweaks, and local dev with Jekyll.

## Architecture & Key Locations
- Content: `_posts/` for blog posts (Markdown), `_pages/` for site pages.
- Presentation: `_layouts/` (page/post templates) and `_includes/` (reusable HTML snippets like `pagination.html`, `search-lunr.html`, `disqus.html`, `share.html`, star rating includes).
- Styles & Assets: `_sass/` partials, `assets/css/` (`main.scss`, `screen.css`), `assets/js/` (jQuery, Lunr search, theme scripts), `assets/images/` for images.
- Config: root `_config.yml` (site metadata, authors, plugins, permalinks), `site/_config.yml` (dev-only overrides like `host: 0.0.0.0`).
- Feeds/Search: `feed.xml` for RSS; Lunr search via `assets/js/lunr.js` and `assets/js/lunrsearchengine.js` with `_includes/search-lunr.html`.

## Local Development
- Docker (recommended on Windows):
  - `docker-compose up` using `jekyll/jekyll:latest` with `jekyll serve --force_polling` mapped to port 4000.
- Native Ruby (optional):
  - `bundle install`
  - `bundle exec jekyll serve` (use `--livereload` if desired). Ensure Ruby and Bundler are installed.
- Preview: open `http://localhost:4000`.

## Content Conventions
- Post filenames: `YYYY-MM-DD-title-with-dashes.md` in `_posts/`.
- Required front matter for posts:
  ```yaml
  ---
  layout: post
  title: "Your Title"
  author: peder
  categories: [ education ]
  image: assets/images/MRI_logo-retro.png
  featured: false
  hidden: false
  ---
  ```
  - `author` must match a key in `_config.yml` under `authors` (e.g., `peder`, `jess`).
  - `categories` drive archives via `jekyll-archives`; ensure meaningful category values.
- Pages: place in `_pages/` with `layout: page` or appropriate layout.
- Images: store in `assets/images/` and reference with site-relative paths (e.g., `assets/images/...`).

## Theme & Includes Patterns
- Modify layouts in `_layouts/` to change global templates (`default.html`, `post.html`, `archive.html`).
- Use `_includes/` for shared widgets:
  - Comments: `disqus.html` uses site `disqus` shortname in `_config.yml`.
  - Search: `search-lunr.html` with Lunr scripts in `assets/js/`.
  - Social sharing: `share.html`.
  - Ratings: `star_rating.html` and `star_rating_postbox.html` with styles in `_sass/_stars.scss`.
  - Adsense: `adsense-under-header.html` (disabled unless `_config.yml` `adsense` is enabled).

## Configuration & Plugins
- `_config.yml` controls:
  - Site metadata (`name`, `title`, `description`, `logo`, `favicon`).
  - Permalinks: `/:title/` (no date in URL).
  - `include: ["_pages"]` to expose pages directory.
  - Plugins: `jekyll-paginate`, `jekyll-sitemap`, `jekyll-feed`, `jekyll-seo-tag`, `jekyll-archives`, `jekyll-twitter-plugin`.
  - Analytics/Comments: `google_analytics`, `disqus` shortname.
  - Markdown: `kramdown` with Rouge highlighting and line numbers.
- Dev-only: `site/_config.yml` sets `host: 0.0.0.0` for container access.

## Deployment
- GitHub Pages-style repo (`LarsonLab.github.io`). No CI config present; publishing likely via GitHub Pages with default Jekyll build. Avoid adding unsupported plugins for GitHub Pages unless building externally.

## Common Workflows & Tips
- Add author: edit `_config.yml` under `authors` (include `name`, `display_name`, `email`, `web`, `git_name`, `twitter`, `description`).
- New post: create file in `_posts/` with required front matter; set `featured: true` to show as featured in templates that support it.
- Categories & Tags pages: see `_pages/categories.md` and `_pages/tags.md`; ensure categories/tags used in posts to populate.
- Search indexing: Lunr searches client-side; keep post front matter and content consistent for indexing.
- Windows file watch: container uses `--force_polling` to avoid missed reloads.
- Ads/Analytics: only active if configured in `_config.yml`.

## Project-Specific Notes
- Theme is Mediumish; many defaults live in `assets/js/mediumish.js` and layouts. Match existing markup/classes when adding components.
- Avoid changing `permalink` unless prepared to update internal links.
- Future-dated posts may not render unless Jekyll `future` is enabled; publish with current or past dates if needed for visibility.

## Examples
- Example post front matter (from current repo):
  ```yaml
  ---
  layout: post
  title:  "Teaching MRI and Book"
  author: peder
  categories: [ education ]
  image: assets/images/MRI_logo-retro.png
  featured: true
  ---
  ```
- Docker dev: `docker-compose up` then browse `http://localhost:4000`.

## Agent Etiquette
- Keep changes minimal and consistent with current theme and structure.
- Do not introduce site-wide layout changes without confirming intent.
- When editing content, validate local preview to catch broken links or includes.
