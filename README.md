# Yutong Wang — Academic Homepage

Source code for [https://emoilere.github.io](https://emoilere.github.io), the personal academic homepage of **Yutong Wang (王宇彤)**, undergraduate researcher at **Lanzhou University**.

## Structure

```
EMOILERE.github.io/
├── index.html               # the entire site (single-file HTML + inline CSS)
├── assets/
│   ├── photo.jpg            # portrait
│   ├── lanzhouuniversity.jpeg
│   └── teaser_*.svg         # per-paper teaser thumbnails (SVG, no external deps)
└── README.md
```

## Deploy to GitHub Pages

1. Create a public GitHub repository named **exactly** `EMOILERE.github.io` (the repo name must match `username.github.io`).
2. Push the contents of this folder to the `main` branch:
   ```bash
   cd EMOILERE.github.io
   git init
   git add .
   git commit -m "Initial homepage"
   git branch -M main
   git remote add origin https://github.com/EMOILERE/EMOILERE.github.io.git
   git push -u origin main
   ```
3. On GitHub, go to **Settings → Pages**. Confirm the source is `Deploy from a branch` → `main` / `/ (root)`.
4. After a few seconds your site is live at `https://emoilere.github.io`.

## Local preview

```bash
cd EMOILERE.github.io
python3 -m http.server 8000
# then open http://localhost:8000
```

## How to update content

- **News, Publications, Awards** are all plain HTML blocks inside `index.html` — edit them directly.
- To add a new paper: copy one of the `<div class="pub">…</div>` blocks, swap the teaser SVG path, title, authors, venue, and links.
- To add a new teaser image: drop a 320×200 SVG (or any 16:10 image) into `assets/` and point the `<img>` to it.

## Design

The layout follows the single-column academic-homepage convention popularised by sites such as Jiajun Deng (USTC) — left photo + right bio header, simple News table, paper cards with left thumbnail + right metadata, grey-scale palette with one blue accent for links, and Helvetica-family sans-serif typography.
