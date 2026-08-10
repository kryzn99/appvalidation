# Landing page — setup

## Publish with GitHub Pages
1. Create a new repo on GitHub (public, e.g. `photo-diary-landing`).
2. Add `index.html` to the **root** of that repo (not inside a subfolder).
3. Push it — via GitHub's web "upload files" button, or:
   ```
   git init
   git add index.html
   git commit -m "landing page"
   git branch -M main
   git remote add origin https://github.com/<you>/<repo>.git
   git push -u origin main
   ```
4. In the repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main / (root)**.
5. GitHub gives you a live URL within a minute or two:
   `https://<you>.github.io/<repo>/`

## What's already wired up
- The Tally "Standard" embed is already pasted into the survey section — nothing to add there.
- Fonts (Fraunces, Karla, Space Mono) load from Google Fonts via CDN — needs an internet connection, no local font files required.
- Fully responsive, works down to small mobile widths.
- Respects `prefers-reduced-motion` for the scroll-reveal animation.

## If you want to tweak later
- All colors/fonts are CSS variables at the top of the `<style>` block (`:root { ... }`) — change once, applies everywhere.
- The date labels in the hero ("AUG 03", "SAT/SUN/TODAY") are static text, not dynamic — update manually if you keep this page live for a while.
