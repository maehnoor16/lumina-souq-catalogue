# Lumina Souq — Product Catalog 2026

Static product catalog ready for GitHub Pages.

## Folder structure

```
lumina-souq-catalog/
├── index.html          ← main catalog page (GitHub Pages entry point)
├── products/           ← product images (lowercase, no spaces)
│   ├── blue-neel.webp
│   ├── bleach.webp
│   ├── bathroom-cleaner.webp
│   ├── glass-cleaner.webp
│   ├── dishwash.webp
│   ├── toilet-cleaner.webp
│   ├── multi-surface-cleaner.webp
│   ├── vinegar.webp
│   ├── concentrate-phenyl.webp
│   └── revivify.webp
└── README.md
```

## Deploy to GitHub Pages

1. Create a new GitHub repository (e.g. `lumina-souq-catalog`).
2. Push this entire folder to the repo root.
3. On GitHub: **Settings → Pages → Build and deployment → Source** → choose **Deploy from a branch**.
4. Branch: `main`, folder: `/ (root)`.
5. Save. Your site will be live at `https://<username>.github.io/lumina-souq-catalog/`.

## Adding a new product image

1. Save the image in `products/` using a lowercase hyphenated name, e.g. `drain-buster.webp`.
2. In `index.html`, add the path to the product entry:

```js
image: 'products/drain-buster.webp'
```

3. Grid cards load images lazily (`loading="lazy"`). Detail view loads immediately (`loading="eager"`).

## Image tips

- Keep each image under **150 KB** when possible (use [squoosh.app](https://squoosh.app) to compress).
- Use `.webp` for all product images (best compression and browser support).
- Variant + size photos follow the pattern `{slug}-{variant}-{size}.webp`, e.g. `bleach-standard-300ml.webp`.
- Avoid spaces and capital letters in filenames.
