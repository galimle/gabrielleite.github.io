# Gabriel Lima Leite — Personal Profile Site

A single-page professional profile built with Jekyll and GitHub Pages.

## 🚀 Setup

### 1. Create the GitHub repository

The repo is already at `galimle/gabrielleite.github.io`.

Push the contents of this folder to the root of the **`master`** branch, replacing the existing files.

### 2. GitHub Pages settings

Go to **Settings → Pages**, confirm Source is **Deploy from a branch**, branch `master`, root `/`. The site will be served at **https://gabrielleite.dev** (your CNAME is already included).

### 4. Local development (optional)

```bash
gem install bundler
bundle install
bundle exec jekyll serve
# → open http://localhost:4000
```

## 📁 Structure

```
.
├── _config.yml          # Site config, theme, metadata
├── _layouts/
│   └── default.html     # Custom layout (overrides theme header)
├── assets/
│   └── css/
│       └── style.scss   # All custom styles (dark theme)
├── index.md             # Main page content
├── Gemfile              # Ruby dependencies
└── README.md
```

## ✏️ Customisation

- **Add a project**: Copy a `<div class="project-card">` block in `index.md` and fill in details.
- **Change colours**: Edit CSS variables in `assets/css/style.scss` (`:root` block).
- **Add a GitHub link**: Replace the `↗` LinkedIn fallback in project cards with your GitHub repo URL.
