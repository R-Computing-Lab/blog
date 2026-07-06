# Blog setup and initial content — design

## Context

The blog at `R-Computing-Lab/blog` is a blogdown/Hugo site (theme `hugo-lithium`) still in its default scaffolded state: stock demo posts, generic About page, generic site description. The site should become the public face of the R Computing Lab (S. Mason Garrison, Wake Forest University), and is intended to be submitted to [R-bloggers](https://www.r-bloggers.com/), so post content must stay substantively R-focused (packages, tutorials, reproducible workflows) rather than general lab/personal content. R-bloggers aggregates via RSS (`content/post/`), so static pages (About, Software, Publications) don't need the same R-only constraint, but posts do.

Author: S. Mason Garrison only, for now. Content mix: lab/software news, R tutorials, research notes — all framed through an R lens.

## Scope

### 1. `config.yaml`
- Keep `title: "R Computing Lab"`.
- Replace `params.description` with an R-focused one-liner (e.g. mentions R packages, statistical genetics, reproducible research).
- Add menu entries for the new Software and Publications pages, keeping existing About / GitHub / Twitter entries as-is.
- Leave a one-line comment noting `favicon.ico` / `logo.png` are referenced but not present in `static/` — out of scope for this pass (no asset provided).

### 2. Remove placeholder content
Delete the three stock blogdown demo posts under `content/post/`:
- `2015-01-01-lorem-ipsum/`
- `2016-12-30-hello-markdown/`
- `2020-12-01-r-rmarkdown/` (includes rendered `.html` and `index_files/`)

### 3. `content/about.md`
Real bio drawn from the CV (`https://smasongarrison.github.io/CV-Tex/SMasonGarrisonCV.pdf`): Associate Professor of Quantitative Psychology at Wake Forest, PhD Vanderbilt (Quantitative Methods), Director of the R Computing Lab since 2019, research interests (genetically-informed designs, pedigree/kinship models, SEM, diversity science, health inequity), links to DS4P course and personal site.

### 4. `content/software.md`
List of maintained R packages with one-line descriptions and CRAN/doi links:
- `BGmisc` — extended behavior genetics analysis
- `ggpedigree` — visualizing pedigrees with ggplot2/plotly
- `discord` — discordant kinship modeling
- `NlsyLinks` — NLSY kinship utilities
- `ACEsimFit` — ACE kin-pair simulation/fitting (contributor role, noted as such)

### 5. `content/publications.md`
Curated highlight list (~8-10 entries, not the full 27) prioritizing: the JOSS software papers (BGmisc, ggpedigree), marquee journal papers (Nature 2026, JPSP 2019, eBioMedicine 2025), and the DS4P open-source book. Ends with a link to the full CV for the complete list.

### 6. First real post
`content/post/2026-07-06-welcome/index.md` — "Welcome to the R Computing Lab Blog". Structure covers what the blog will focus on (R package news, tutorials, reproducible-research notes), explicitly framed for an R audience. Includes a clearly marked placeholder (HTML comment) where Mason writes his own 5-10 line opening paragraph, so the post's voice is his rather than AI-generated.

## Out of scope (this pass)
- Favicon/logo assets
- Theme change
- Multi-author support
- Full publications list (all 27 entries)

## Verification
Hugo isn't installed in this environment, so a full `blogdown::serve_site()` render isn't possible here. Verification for this pass: hand-check YAML validity in `config.yaml`, hand-check Markdown/front-matter validity in new content files, confirm placeholder posts are fully removed (no orphaned files). Mason will do a live visual check via `blogdown::serve_site()` in RStudio afterward.
