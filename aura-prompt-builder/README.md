# Mikuláš Linhart — Portfolio

Static, self-contained portfolio site (Apple "liquid glass" style). No backend, no build step — just static files, ready for GitHub Pages.

```
portfolio-site/
├── index.html        # the whole site
├── assets/           # lenis smooth-scroll + tool logos
└── .nojekyll         # tells GitHub Pages to skip Jekyll
```

## Deploy to GitHub Pages

1. Create a new repo on GitHub (e.g. `portfolio`).
2. From this folder:
   ```bash
   git init
   git add .
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo>.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, pick `main` / `/ (root)`, Save.
4. Live in ~1 min at `https://<your-username>.github.io/<repo>/`.

### Want the cleaner URL `https://<your-username>.github.io/`?
Name the repo exactly `<your-username>.github.io` and push the same files — it serves from the root domain.

## Notes
- Relative asset paths, so it works whether served from a sub-path (`/repo/`) or the root domain.
- Google Fonts load from Google's CDN (needs internet, no setup).
- **Edit mode:** press `E` (or the pencil button, bottom-left) to upload/drag project photos. Images are saved in the browser's localStorage on the device you're using — they are *not* committed to the repo, so visitors won't see them. To make photos permanent, drop them in `assets/` and hard-code them into `index.html`.
