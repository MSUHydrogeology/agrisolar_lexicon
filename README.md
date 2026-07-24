# The Lexicon of Restorative Agroenergy Design

A shared design language for agrisolar photovoltaic landscapes.

Published at <https://msuhydrogeology.github.io/agrisolar_lexicon/>

## Publishing

Create the repository at `MSUHydrogeology/agrisolar_lexicon`, **public**, with no README or
license (these files supply both). Then from this directory:

```bash
git init -b main
git add .
git commit -m "Initial lexicon draft"
git remote add origin https://github.com/MSUHydrogeology/agrisolar_lexicon.git
git push -u origin main
```

Then **Settings → Pages** on the repo: set Source to *Deploy from a branch*, branch `main`,
folder `/ (root)`, and Save. First build takes one to two minutes.

No build workflow is required — the theme loads via `remote_theme`, which GitHub Pages supports
natively.

### If Pages does not appear in Settings

Organization owners control this at **Organization settings → Member privileges → Pages
creation**. If Pages is restricted, an owner needs to enable it or perform the step above.
On GitHub Free, Pages requires the repository to be public.

### Local preview (optional)

```
gem install bundler jekyll
bundle init && bundle add jekyll just-the-docs jekyll-remote-theme
bundle exec jekyll serve
```

## Structure

| Path | Contents |
|---|---|
| `index.md` | Landing page |
| `preface.md` … `sources.md` | Document sections, one page each |
| `figures/` | Standalone SVG figures, reusable independently |
| `_config.yml` | Site and theme configuration |

Figures are referenced with `relative_url` so they resolve correctly under the
`/agrisolar_lexicon` baseurl. Do not change `baseurl` unless the repository is renamed — plain
relative image paths break silently on project sites, resolving against the page URL rather than
the site root.

## Contributing

See `CONTRIBUTING.md`. Proposed terms, corrections, and counterexamples are all in scope —
particularly counterexamples to the claim in §2.2 that sparing is largely unavailable at A5.

## Citation

See `CITATION.cff`. For a stable citable version, connect the repository to Zenodo and cut a
release; Zenodo will mint a DOI and archive the snapshot.

## License

Content is licensed CC BY 4.0. See `LICENSE.md`.
