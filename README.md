# The Lexicon of Restorative Agrisolar Design

A shared design language for agrisolar photovoltaic landscapes.

Published at <https://msuhydrogeology.github.io/agrisolar_lexicon/>

Built with [Quarto](https://quarto.org) as a book, rendered to a browsable HTML site and a
downloadable PDF from a single source.

## Publishing

Deployment is automatic. The GitHub Action in `.github/workflows/publish.yml` renders the book
(HTML + PDF) and deploys it to GitHub Pages on every push to `main`; pull requests are
render-checked but not deployed.

One-time repository setting: **Settings → Pages → Build and deployment → Source: GitHub Actions**.

## Local preview

Requires [Quarto](https://quarto.org/docs/get-started/) and `rsvg-convert` (from `librsvg`, for
embedding the SVG figures in the PDF). PDF output additionally needs a LaTeX install
(`quarto install tinytex`).

```bash
quarto preview        # live-reloading local site
quarto render         # build _site/ (HTML + PDF)
quarto render --to html   # HTML only (no LaTeX needed)
```

## Structure

| Path | Contents |
|---|---|
| `index.qmd` | Landing page |
| `preface.qmd` … `sources.qmd` | Document chapters, one page each |
| `index-alphabetical.qmd` | Alphabetical index of defined terms (appendix) |
| `figures/` | Standalone SVG figures, reusable independently |
| `references.bib` | Bibliography; cited inline with `@key`, formatted in the Sources chapter |
| `_quarto.yml` | Book, format (HTML + PDF), and cross-reference configuration |

Cross-references between chapters use Quarto syntax: `@fig-transect` for figures and
`[text](file.qmd#sec-id)` for sections, with explicit `{#sec-…}` / `{#term-…}` heading ids so the
links stay stable. Sources are cited inline as `@key` against `references.bib`; the Sources chapter
keeps the curated, annotated Verified / Unverified lists alongside the generated reference list.

## Contributing

See `CONTRIBUTING.md`. Proposed terms, corrections, and counterexamples are all in scope —
particularly counterexamples to the claim in §2.2 that sparing is largely unavailable at A5.

## Citation

See `CITATION.cff`. For a stable citable version, connect the repository to Zenodo and cut a
release; Zenodo will mint a DOI and archive the snapshot.

## License

Content is licensed CC BY 4.0. See `LICENSE.md`.
