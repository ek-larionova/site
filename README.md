# Zola + Portio personal site

This repo is set up to:

- use the [portio-zola](https://github.com/quentin-rodriguez/portio-zola) template
- build with Zola on every push to `main`
- deploy the generated `public/` output to the `gh-pages` branch

## Local usage

```bash
git clone https://github.com/quentin-rodriguez/portio-zola themes/portio-zola
zola serve
```

## GitHub Pages setup

1. In GitHub repository settings, open **Pages**.
2. Set **Source** to **Deploy from a branch**.
3. Choose branch `gh-pages` and folder `/ (root)`.

The workflow is defined in `.github/workflows/deploy.yml`.
