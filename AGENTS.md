# AGENTS.md

Context for AI agents working on this repository.

## What this is

Personal portfolio site for Gabriel Lima Leite, Senior SDE at AWS Redshift, Berlin.
Built with Jekyll, hosted on GitHub Pages at gabrielleite.dev.
Custom dark theme (navy `#0a192f` / green `#64ffda`), no CSS framework.

## How to run locally

```bash
bundle install
bundle exec jekyll serve
# → http://localhost:4000
```

Jekyll auto-rebuilds on file changes. Refresh the browser to see updates.

## Key files

| File | Purpose |
|---|---|
| `index.md` | Entire single-page site — edit content here |
| `assets/css/style.scss` | All styles, CSS variables at the top in `:root` |
| `_layouts/default.html` | HTML shell, includes copy-to-clipboard email script |
| `education/index.md` | Full curriculum detail page at `/education` |
| `_config.yml` | Site title, author info, Jekyll plugins |

## Architecture decisions

- **All content lives in `index.md`** as raw HTML inside Jekyll front matter — not Markdown prose. This is intentional for layout control.
- **`id="about"` is the Skills section** — the nav link says "Skills" but the anchor is `#about`. Don't rename the id without updating all nav links.
- **Email links use copy-to-clipboard**, not `mailto:` — handled by a JS snippet in `_layouts/default.html` that intercepts all `mailto:` hrefs at runtime.
- **Projects are split into two grids** — "Professional" (AWS Redshift work) and "Personal" (side projects/thesis). Each grid is preceded by a `.projects-group-label`.
- **Education has two layers** — summary cards on `index.md` (linking to `/education#robotics` and `/education#bsc`) and full curriculum detail on `education/index.md`.
- **`remote_theme: pages-themes/minimal@v0.2.0`** is declared in `_config.yml` but fully overridden by the custom layout and stylesheet. The theme contributes nothing visible.

## Content guidelines

- **Don't invent or embellish achievements** — all content must be grounded in Gabriel's actual LinkedIn/CV.
- **Tech tags on project/experience cards** should reflect tools actually used, not aspirational skills.
- **Education degree tags** (on `index.md`) should reflect skills relevant to a Senior SDE career — remove curriculum topics that don't map to actual work (e.g. ML/CV if not actively used).
- **Tone**: direct, no fluff. No "passionate about" or "I love to". Achievements with numbers where possible.

## Deployment

Pushing to `master` triggers `.github/workflows/jekyll.yml` which builds and deploys to GitHub Pages automatically. The custom domain `gabrielleite.dev` is configured via `CNAME` + Route53.
