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
  The site's CSS lives inside a `<style>` block in `_layouts/default.html`
  (inlined on purpose, so the whole design loads in one request and can
  never go missing because a separate CSS file failed to upload).
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

## Uploading this repo

**The most reliable way is git**, not GitHub's drag-and-drop web uploader.
The `assets/` folder here contains 100+ files (PDFs, datasets, the photo)
across several subfolders, and browser-based uploads can silently drop or
truncate large, deeply-nested folders like this.

```bash
git clone https://github.com/suthakaranr/suthakaranr.github.io.git
cd suthakaranr.github.io
git rm -rf .                 # clear the old site
# copy every file from this package into the now-empty folder, including
# hidden files like .gitignore
git add -A
git commit -m "Redesign site"
git push
```

If you do use the web uploader instead, drag the **extracted folders**
(not the .zip) directly from Finder/Explorer onto the "Add file → Upload
files" page, and upload `assets/` on its own in a separate pass from the
rest, since it's by far the largest folder. Afterwards, open the repo on
github.com and confirm `assets/headshot.jpg` and `assets/SR.pdf` actually
show up in the file listing — if they're missing, the site's photo, CV
link, and publication/data links will all 404 even though the rest of the
site looks fine.

## License

Original content is licensed under [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/).
