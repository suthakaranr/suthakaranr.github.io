# suthakaranr.github.io

Source for [suthakaranr.github.io](https://suthakaranr.github.io), built with
[Jekyll](https://jekyllrb.com/) and served by GitHub Pages.

## Structure

* `index.md` &mdash; homepage (bio + contact card). Contact details, the CV
  link, and the photo are set as front matter at the top of the file, so you
  can update them without touching any HTML.
* `pages/` &mdash; all inner pages (Education, Research, Teaching, Software,
  and the individual course/data-set pages), written in Markdown.
* `_layouts/` &mdash; the three page templates (`default`, `home`, `page`).
* `assets/css/style.css` &mdash; the site's stylesheet.
* `assets/` &mdash; PDFs, datasets, and the headshot photo.
* `_config.yml` &mdash; site title, contact info used in the footer, and the
  `nav:` list that controls the top navigation bar.

## Editing content

* **Add a publication:** open `pages/Research.md` and add a new numbered
  entry at the top of the list, following the existing format.
* **Update the CV:** replace `assets/SR.pdf` with a new file of the same
  name, or update `cv_url` in `_config.yml` / `index.md`.
* **Add a nav link:** edit the `nav:` list in `_config.yml`.
* **Change contact info or photo:** edit the front matter (the block between
  `---` lines) at the top of `index.md`.

## Running locally (optional)

```bash
bundle install
bundle exec jekyll serve
```

Then visit `http://localhost:4000`. This step is optional &mdash; GitHub
Pages will build and publish the site automatically on every push to the
default branch.

## License

Original content is licensed under [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/).
