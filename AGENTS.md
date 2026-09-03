# Montacchiello.dev

Jekyll site for Montacchiello Developers, an independent software developer community in
Pisa, Italy. Built with `jekyll-theme-cayman` (no custom layouts/includes — theme defaults
are used as-is). Deployed to <https://montacchiello.dev> via GitHub Pages.

## Structure

- `index.md` — homepage: recent events, archive, contacts, sponsors, photo gallery.
- `events/` — one Markdown page per past event, front matter `layout`, `title`, `image`.
- `slides/` — PDF slide decks linked from event entries.
- `images/` — event photos and logos referenced from `index.md` and event pages.
- `_config.yml` — site title, description, theme, plugins (`jekyll-sitemap`).
- `CNAME` — custom domain for GitHub Pages.

## Working locally

Ruby version is pinned in `.ruby-version` (see that file for the exact version).

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
bundle exec jekyll build   # outputs to _site/
```

## Conventions

- Content is authored in Italian.
- Adding a past event: create `events/<slug>.md` with front matter (`layout: default`,
  `title`, optional `image`), then link it from the archive list in `index.md`.
- Slide decks go in `slides/` and are linked as `[💾 Slides](/slides/<file>.pdf)`.
- Dependency updates (Ruby gems, GitHub Actions) are managed by Dependabot
  (`.github/dependabot.yml`).
