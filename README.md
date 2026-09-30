# DSA GRIND — 100 Day Java + DSA (PWA)
Static site, no build step. Files: index.html, manifest.json, sw.js, icon-*.png, vercel.json.

## Deploy on Vercel
1. Put this folder in a GitHub repo (or run `npx vercel` inside the folder).
2. vercel.com → Add New → Project → import the repo → Framework: "Other" → Deploy.
3. Open https://<your-name>.vercel.app in Chrome → ⋮ → Add to Home screen / Install app.

## Deploy on GitHub Pages
1. Create a repo, upload all files to the root (index.html at top level).
2. Settings → Pages → Source: "Deploy from a branch" → main / (root) → Save.
3. Open https://<username>.github.io/<repo>/ → Chrome ⋮ → Install app.

## Notes
- Progress is stored in the browser (localStorage) per device and per URL. Keep using ONE URL.
- Use Settings → Export Progress once a week; hourly auto-backups are kept in the browser too.
- Certificate verification link: `<your-url>/#verify/CERT-XXXXXXX/Name/YYYY-MM-DD`.
