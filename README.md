# Starter kit for [Alembic](https://alembic.darn.es/)

This is a very simple starting point if you wish to use Alembic [as a Jekyll theme gem](https://alembic.darn.es/#as-a-jekyll-theme) or as a [GitHub Pages remote theme](https://github.com/daviddarnes/alembic-kit/tree/remote-theme) (see `remote-theme` branch).

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/daviddarnes/alembic-kit)

or

**[Download the GitHub Pages kit](https://github.com/daviddarnes/alembic-kit/archive/remote-theme.zip)**

# Website

This repository uses the Alembic Jekyll theme via `remote_theme: daviddarnes/alembic`.

## Local development (Ruby + Bundler)

Install Ruby and Bundler, then run:

```bash
gem install bundler
bundle install
bundle exec jekyll serve
```

Open http://127.0.0.1:4000/website.henryvuong/ (if `baseurl` is set) or http://127.0.0.1:4000/.

## Local development (Docker)

If you prefer Docker:

```bash
docker run --rm -it -p 4000:4000 -v "$(pwd)":/srv/jekyll -v "$(pwd)/vendor/bundle":/usr/local/bundle -w /srv/jekyll jekyll/jekyll:4.2.0 jekyll serve
```

## CI build

A GitHub Actions workflow `.github/workflows/jekyll-build.yml` builds the site on push and uploads the generated `_site` as an artifact. After pushing, go to Actions → the workflow run → Artifacts → `site` to download and inspect the generated HTML to see how GitHub Pages will render your site.


## Notes
- `remote_theme` is recommended for GitHub Pages. If you have local theme gem conflicts, remove the local theme gem from `Gemfile`.
