# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Personal portfolio site for Mara Di Ciolli, built with Jekyll and hosted on GitHub Pages. No custom plugins — GitHub Pages builds it automatically on push to `main`.

## Development

Preview locally (requires Ruby + Bundler):

```
bundle exec jekyll serve
```

Or just push to `main` — GitHub Pages builds and deploys automatically since the repo name is `MaraDiCiolli.github.io`.

## Architecture

Jekyll site with Liquid templates. No JavaScript.

- **`_layouts/default.html`** — Base HTML shell (head, CSS link, header/footer includes)
- **`_layouts/home.html`** — Homepage layout: renders About section content + auto-generated blog listing from `site.posts`
- **`_layouts/post.html`** — Blog post layout: title, meta, post body, sidebar
- **`_includes/`** — Shared partials: `header.html` (nav with conditional active states), `footer.html`, `sidebar.html` (auto-generated post list)
- **`_posts/`** — Blog posts as Markdown with front matter (`layout`, `title`, `date`, `tag`, `excerpt_text`)
- **`assets/css/style.css`** — Single stylesheet, linked from `default.html`
- **`index.html`** — Homepage content (About section HTML) with `layout: home` front matter
- **`_config.yml`** — Site config; permalink is `/blog/:slug/`

### Adding a new blog post

1. Create `_posts/YYYY-MM-DD-slug.md`
2. Add front matter: `layout: post`, `title`, `date`, `tag`, `excerpt_text`
3. Write the body in Markdown
4. Push — the post automatically appears on the homepage listing and all sidebars

### Design system

CSS custom properties in `:root`: colors (`--ink`, `--paper`, `--accent`, `--muted`, `--rule`), fonts (`--font-display` Playfair Display, `--font-body` Source Sans 3, `--font-mono` JetBrains Mono). All loaded from Google Fonts.

Homepage uses `.site-wrapper` (720px max-width); blog post pages use `.site-wrapper.wide` (960px).
