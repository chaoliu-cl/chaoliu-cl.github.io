# liu-chao.site

Personal website of Chao Liu, Associate Professor of Psychology at Cedarville University.

Built with [Hugo](https://gohugo.io/) using the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme.

## Deployment

The site is built and deployed by the GitHub Actions workflow in
[`.github/workflows/hugo.yml`](.github/workflows/hugo.yml) on every push to `main`.

> **Important:** GitHub Pages must be configured to deploy from GitHub Actions,
> not from a branch. In **Settings → Pages → Build and deployment**, set
> **Source** to **GitHub Actions**. If it is set to "Deploy from a branch",
> Pages runs Jekyll on the repo root and only renders this README instead of
> the Hugo site.

## Local development

```sh
# Hugo extended is required (matches the pinned CI version in hugo.yml).
hugo server
```

Then open http://localhost:1313.

To produce a production build:

```sh
hugo --minify --baseURL "https://liu-chao.site/"
```

The generated `public/` directory is not committed — the workflow regenerates it
on each deploy.

## Structure

- `content/` — pages and posts (Markdown)
- `layouts/` — project-level template overrides
- `themes/PaperMod/` — the theme
- `static/` — files copied verbatim to the site root (images, CV, favicons)
- `config.yml` — site configuration
