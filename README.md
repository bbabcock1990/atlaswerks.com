# atlaswerks.com

Source for [www.atlaswerks.com](https://www.atlaswerks.com) — the public site
for **Atlas Werks LLC**, the independent Azure consulting and Microsoft CSP
practice of [Brandon Babcock](https://www.linkedin.com/in/brandonbabcock1990).

Built with [Jekyll](https://jekyllrb.com) and deployed by [GitHub Pages](https://pages.github.com).

## Local development

```bash
bundle install
bundle exec jekyll serve
# open http://127.0.0.1:4000
```

## Project layout

```
_config.yml          # site identity, plugins, defaults
_data/               # services, skills, certs, experience, projects, now, social
_includes/           # head, nav, footer, social-icons
_layouts/            # default, page, post, home
_posts/              # blog posts
_sass/               # SCSS partials
assets/
  css/main.scss      # entry SCSS (must keep front-matter so Jekyll compiles it)
  js/main.js         # nav toggle, theme toggle, scroll reveal
  images/            # profile + post images + favicons
  files/             # resume PDF
index.html           # home
about.md services.md projects.md experience.md now.md contact.md
blog/index.html      # blog index
404.html             # custom 404
CNAME                # custom domain
robots.txt
.github/workflows/   # CI build check (no deploy — Pages handles deploy)
```

## Deploy

The site is published from the `gh-pages` branch by GitHub Pages' legacy build.
The CI workflow at `.github/workflows/build.yml` runs `bundle exec jekyll
build --safe --trace` on pull requests so a broken build can't be merged.

## Editing tips

- **Add a service / skill / cert / project / experience entry** — edit the
  matching YAML file under `_data/`. No template changes needed.
- **Add a blog post** — drop a markdown file under `_posts/` named
  `YYYY-MM-DD-title.md` with `layout: post`, `title`, `date`, `category: blog`.
- **Update the "Now" page** — edit `_data/now.yml` and bump `updated:`.
- **Tweak colors / spacing** — edit `_sass/_variables.scss` and
  `_sass/_base.scss` (the `:root` and `[data-theme="light"]` blocks).

## Disclaimer

Atlas Werks LLC is independent and is not affiliated with, endorsed by, or
sponsored by Microsoft.
