# tmsaurav.github.io

Personal site, built with [Quarto](https://quarto.org) and hosted on GitHub Pages.

## Layout

| Path | What it is |
|---|---|
| `index.qmd` | About page (photo, bio, links) |
| `research/` | One `.qmd` per project; `index.qmd` lists them automatically |
| `publications.qmd` | Publication list |
| `cv.qmd` | Web CV; the PDF lives in `files/` |
| `notes/` | Blog-style posts (`.qmd` or `.ipynb`); not in the navbar yet |
| `styles/` | Light and dark theme tweaks |
| `_quarto.yml` | Site title, navbar, theme |

## Edit and preview

Install Quarto from <https://quarto.org/docs/get-started/>, then:

```sh
quarto preview
```

This opens the site locally and reloads as you save.

## Publish

Push to `master`. The workflow in `.github/workflows/publish.yml` renders the
site and pushes it to the `gh-pages` branch, which GitHub Pages serves.

## Add a note

1. Copy `notes/_template.qmd` to `notes/my-post.qmd`.
2. Write it, run `quarto preview` to check.
3. If the post runs code, commit the `_freeze/` folder Quarto creates, so the
   GitHub build reuses your results instead of needing Python.
4. For the first post, uncomment the Notes entry in `_quarto.yml`.
