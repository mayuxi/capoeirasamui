# Capoeira Samui — Astro Site

One-page site for Capoeira Samui in 5 languages: English, Russian, Portuguese, Hebrew, Thai.

## Stack

- [Astro](https://astro.build) — static site generator
- Cloudflare Pages — hosting (same as before)
- GitHub — source + CI/CD (same as before)

## Project structure

```
src/
  i18n/
    index.js          ← all translations (edit here to update content)
  layouts/
    Base.astro        ← HTML shell, SEO tags, global CSS, fonts
  components/
    HomePage.astro    ← single page layout used by all languages
  pages/
    index.astro       ← English (/)
    ru/index.astro    ← Russian (/ru/)
    pt/index.astro    ← Portuguese (/pt/)
    he/index.astro    ← Hebrew (/he/)
    th/index.astro    ← Thai (/th/)
public/
  images/
    logo.png          ← copy from old Hugo site
    map.png           ← copy from old Hugo site
    capoeirasamui-highres-logo.png  ← OG image
```

## Getting started

```bash
npm install
npm run dev       # http://localhost:4321
npm run build     # output in dist/
```

## Deploying to Cloudflare Pages

Same setup as Hugo — just change the build command:

| Setting | Value |
|---|---|
| Build command | `npm run build` |
| Build output directory | `dist` |
| Node.js version | 20 |

## Updating content

All text lives in `src/i18n/index.js`. Each language is a plain JS object — just edit the values, commit, and Cloudflare Pages redeploys automatically.

## Updating images

Drop new images into `public/images/` — they'll be copied as-is to `dist/images/`.
