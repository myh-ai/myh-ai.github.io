# Moustafa Yehia Hassan — AI/NLP Research Portfolio

Source repository for [myh-ai.github.io](https://myh-ai.github.io/), a Jekyll/GitHub Pages research portfolio focused on trustworthy language-model evaluation, computational mental-health NLP, distributional-fidelity auditing, and biomedical NLP reliability.

## Main content locations

- `_pages/about.md` — homepage structure and research narrative.
- `_data/publications.yml` — publication and manuscript records rendered on the homepage.
- `_config.yml` — site identity, academic profiles, social links, and SEO metadata.
- `assets/css/main.scss` — the custom **Scientific Noir** visual system.
- `_pages/writing.md` and `_pages/contact.md` — writing and contact pages.
- `files/` — CV and downloadable resources.

## Updating publications

Add or edit a record in `_data/publications.yml`. Each publication can expose publisher, PDF, DOI, BibTeX, and code links without hand-editing the publication-card HTML.

## Local preview

```bash
bundle config set --local path 'vendor/bundle'
bundle install
bundle exec jekyll serve --livereload
```

Then open `http://127.0.0.1:4000/`.

## Deployment

The production site is built by GitHub Pages from the source configured under **Settings → Pages**. When that source is `main` / `(root)`, a push to `main`—including a merged pull request—starts the Pages deployment workflow. Build and deployment status appears under **Actions** and **Settings → Pages**.

A detailed Arabic maintenance and publishing guide is available in [`SITE_MAINTENANCE_AR.md`](SITE_MAINTENANCE_AR.md).
