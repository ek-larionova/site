# Zola + Goyo personal site starter

This repository is configured to:

- Build with [Zola](https://www.getzola.org/)
- Use the [Goyo theme](https://www.getzola.org/themes/goyo/)
- Auto-deploy to GitHub Pages via GitHub Actions

## 1) Configure your site

Edit `config.toml`:

- Set `base_url` to your Pages URL
- Update title, author, and social links

For a project site:

```toml
base_url = "https://<user>.github.io/<repo>/"
```

For a user/org site:

```toml
base_url = "https://<user>.github.io/"
```

## 2) Enable GitHub Pages

In your repo settings:

1. Go to **Settings → Pages**
2. Under **Build and deployment**, choose **GitHub Actions** as the source

## 3) Deploy

Push to `main`. The workflow in `.github/workflows/deploy-zola.yml` will:

1. Install Zola
2. Clone the Goyo theme
3. Build the site
4. Deploy `public/` to GitHub Pages

## 4) Local development

Install Zola and run:

```bash
mkdir -p themes
git clone --depth 1 https://github.com/getzola/goyo.git themes/goyo
zola serve
```

Then open <http://127.0.0.1:1111>.
