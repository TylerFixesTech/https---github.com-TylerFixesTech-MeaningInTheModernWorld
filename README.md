# Humanities ePortfolio — ready for GitHub Pages

A small, responsive static site for HUM 202, generated from the six supplied Word files.
No paid account, website builder, database, npm, or build step is needed.

## Quick publishing instructions

1. Unzip `humanities-portfolio.zip` into a new folder. In VS Code choose **File > Open Folder**.
2. Open `index.html` with a browser, or use the free **Live Server** VS Code extension.
3. On GitHub, create a **public** repository, for example `humanities-portfolio`.
4. Commit and push **the contents of this folder** (including `index.html`, `assets`, `.nojekyll`) into the repository's `main` branch. Do not put an extra `humanities-portfolio` folder between the repository root and `index.html`.
5. In the repository choose **Settings > Pages > Build and deployment > Source: Deploy from a branch > Branch: main > Folder: /(root) > Save**.
6. GitHub will show a site URL, usually `https://YOUR-USERNAME.github.io/humanities-portfolio/`. Submit that live URL to the instructor once it loads.

If your repository name is **exactly** `YOUR-USERNAME.github.io`, the root URL is instead `https://YOUR-USERNAME.github.io/`.

Official help: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## What is already included

- Home / index page, with links to every essay and analysis set.
- Renaissance cultural overview + 10 artwork analyses.
- Early Modern (1600–1800) cultural overview + 7 artwork analyses + 6 musical analyses.
- Nineteenth-century cultural overview + 7 artwork analyses + 5 musical analyses.
- Three individual personal essays (Machiavelli; The Tempest; Washington and morality).
- Sources and image-credit page, with museum and research links carried over from the original documents.
- Shared CSS (`assets/css/base.css`) and small CSS files for each **page type** (home, essay, art, music, personal, credits).
- Small original SVG illustrations used on essay pages; no commercial stock photos.

## Important before handing in

- **Artworks:** Several entries already show properly sourced public-domain / CC0 reproductions. Other entries are clearly labeled image placeholders. They still need images to fully satisfy the picture requirement; the museum/reference link on each card helps you locate the exact work.
- **Image delivery:** Current artwork thumbnails are loaded from Wikimedia Commons or The Met over the internet. If you prefer to host copies locally, save appropriately licensed, resized WebP/JPEG files into `assets/images/`, and change the relevant `<img src="...">` values in the art HTML pages.
- **Instructor feedback:** This site faithfully includes the text in the six supplied documents. The instructor's separate comments/markup, if any, were not available. Incorporate required feedback before final grading.
- **Personal information:** GitHub Pages hosted from a free public repository is visible to anyone with the URL. Read your personal reflection essays before publishing and decide what you are comfortable sharing online.
- **Writing and citations:** Research/reference links are preserved, but should be reviewed against any teacher-required citation format. Links can move over time.

## Change the appearance

- Theme palette, typography, margins, navigation: `assets/css/base.css`
- Home cards: `assets/css/home.css`
- Essay formatting: `assets/css/essay.css` and `assets/css/personal.css`
- Artwork cards and placeholders: `assets/css/art.css`
- Music entries: `assets/css/music.css`

## Add missing art

Each artwork is an `<article class="art-entry">` in `renaissance-art.html`, `early-modern-art.html`, or `nineteenth-century-art.html`.
Search for `Artwork image placeholder` to find entries that still need pictures.
After finding a legally reusable image, replace the `<div class="art-image">…</div>` for that card with an `<img>` inside that same container, plus a descriptive `alt`, `loading="lazy"`, and a `figcaption` with artist/title, image source, and license.
You may prefer to keep an image at approximately **600–900 pixels wide**, JPEG/WebP quality 75–85, typically 80–250 KB. For CC BY/CC BY-SA images, include the creator, license, license link, source URL, and any edits. For photos of sculptures, check the photograph's own license.

## Structure

```text
index.html
renaissance-essay.html
renaissance-art.html
early-modern-essay.html
early-modern-art.html
early-modern-music.html
nineteenth-century-essay.html
nineteenth-century-art.html
nineteenth-century-music.html
personal-machiavelli.html
personal-tempest.html
personal-freedom.html
credits.html
assets/css/*.css
assets/images/*.svg
assets/js/site.js
.nojekyll
```

All links are relative, so the site works as a GitHub project site without changes.
