# gabrielleite.dev

Personal portfolio site for Gabriel Lima Leite — Senior Software Development Engineer at Amazon Web Services (Redshift), Berlin.

Live at **[gabrielleite.dev](https://gabrielleite.dev)**

## Stack

- **Jekyll** — static site generator
- **GitHub Pages** — hosting via `galimle/gabrielleite.github.io`
- **GitHub Actions** — CI/CD, auto-deploys on push to `master`
- **Custom dark theme** — navy/green palette, no external CSS framework
- **Custom domain** — `gabrielleite.dev` via CNAME + Route53

## Local development

Requires Ruby 3.2+ and Bundler.

```bash
bundle install
bundle exec jekyll serve
# → http://localhost:4000
```

## Structure

```
.
├── _config.yml              # Site settings, author info, plugins
├── _layouts/
│   └── default.html         # Base HTML layout, copy-to-clipboard email script
├── assets/
│   └── css/
│       └── style.scss       # All styles — variables, layout, components
├── education/
│   └── index.md             # Full curriculum page (/education)
├── index.md                 # Main single-page site
├── Gemfile                  # Ruby dependencies (github-pages, jekyll-remote-theme)
└── .github/
    └── workflows/
        └── jekyll.yml       # Build + deploy workflow
```

## Sections

| Section | id | Notes |
|---|---|---|
| Hero | `#hero` | Name, title, summary, CTA buttons |
| Skills | `#about` | 4 skill cards |
| Experience | `#experience` | 5 roles with highlights and tech tags |
| Projects | `#projects` | Split: Professional / Personal |
| Education | `#education` | Summary cards linking to `/education` |
| Languages | `#languages` | Portuguese, English, Spanish, German |
| Contact | `#contact` | Copy-to-clipboard email |

## Common edits

**Add a project** — copy a `<div class="project-card">` block in `index.md`.

**Update experience** — edit the relevant `<div class="exp-item">` in `index.md`.

**Change colours** — edit CSS variables in `assets/css/style.scss` (`:root` block).

**Update curriculum** — edit `education/index.md`.
